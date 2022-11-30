---
title: Integrating SDT into Version Control Workflows
date: November 30, 2022
---

# Checking for seman changes within a GitHub Action

You may wish to have a semantic analysis of changes performed along with
every PR.  This can be accomplished using a GitHub Action, or in an
analogous way on other repository management services such as GitLab or
BitBucket.  The workflow shown below adds the analysis performed by SDT as a
comment to every submitted pull request.

A GitHub Action could look like the below (and such is used in the
repository for SDT itself; note you only need the middle steps of building
the internal tools if your project includes JSON or Go). The "Analyze
semantic changes" step will always be needed.  If you want to use
tree-sitter grammars and/or custom versions of SDT-supported programming
languages, you will need to install those within the workflow.

Since this is a GH Action for the `sdt` repo itself, we build the underlying
tool(s) in the workflow. For an unrelated repository, you should simply
follow the installation instructions, as you would for installation to a
local development workstation, and include those steps in the YAML file.

```yaml
name: Semantic Diff Tool analysis in PR comment

on:
  pull_request:

jobs:
  pr:
    runs-on: ubuntu-latest
    permissions:
      pull-requests: write
    steps:
      - uses: actions/checkout@v3
        with:
          fetch-depth: 2

      - name: Set up Go
        uses: actions/setup-go@v3
        with:
          go-version: 1.19

      - name: Build jsonformat tool
        run: |
          go build -o "$GITHUB_WORKSPACE/jsonformat" cmd/jsonformat/main.go &&
          echo "$GITHUB_WORKSPACE/" >> $GITHUB_PATH

      - name: Build gotree tool
        run: |
          go build -o "$GITHUB_WORKSPACE/gotree" cmd/gotree/main.go &&
          echo "$GITHUB_WORKSPACE/" >> $GITHUB_PATH

      - name: Analyze semantic changes
        id: pr
        run: |
          new=$(git log | grep 'Merge.*into.*' | head -1 | sed 's/ into .*$//;s/^ *Merge //')
          old=$(git log | grep 'Merge.*into.*' | head -1 | sed 's/^.* into //')
          status=$(go run cmd/sdt/main.go semantic -A "${old}:" -B "${new}:" -m -d)
          echo "Comparing revision $old to $new" >> SDT.analysis
          echo "<pre>" >> SDT.analysis
          echo "$status" >> SDT.analysis
          echo "</pre>" >> SDT.analysis
          echo "$status" # Workflow sees the report also
          
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

      - name: Add a comment to the PR
        uses: mshick/add-pr-comment@v2
        with:
          message-path: SDT.analysis
```

## Supporting other programming languages

A number of programming languages are supported "out of the box" by Semantic
Diff Tool.  However, a larger number of programming languages are supported
if [tree-sitter](https://github.com/tree-sitter) and tree-sitter grammars
are also installed.  Within the [SDT
repository](https://github.com/atlantistechnology/sdt) some workflows
install some such grammars.

For example, the CI/CD test for the package `treesitter`, which is a
component of `sdt` looks like the following.  You can easily include those
steps related to installing tree-sitter and tree-sitter grammars (and
building the supporting `treesit` utility) within your workflows.

```
name: SDT unit tests for tree-sitter diffs

on: [pull_request]

jobs:
  test:
    strategy:
      fail-fast: false
      matrix:
        os: [ ubuntu-latest, macos-latest ]
    runs-on: ${{ matrix.os }}
    steps:
      - uses: actions/checkout@v3

      - name: Set up Go
        uses: actions/setup-go@v3
        with:
          go-version: 1.19

      - name: Build treesit tool
        run: |
          go build -o "$GITHUB_WORKSPACE/treesit" cmd/treesit/main.go &&
          echo "$GITHUB_WORKSPACE/" >> $GITHUB_PATH

      - name: Install tree-sitter CLI
        run: |
          npm install -g tree-sitter-cli &&
          tree-sitter init-config

      - name: Check included languages (expecting none)
        run: tree-sitter dump-languages

      - name: Install C grammar for tree-sitter
        run: |
          export C="https://github.com/tree-sitter/tree-sitter-c.git" &&
          if [ "$RUNNER_OS" == "Linux" ]; then
              git clone $C /home/runner/src/tree-sitter-c &&
              cd /home/runner/src/tree-sitter-c &&
              tree-sitter generate
          elif [ "$RUNNER_OS" == "macOS" ]; then
              git clone $C /Users/runner/src/tree-sitter-c &&
              cd /Users/runner/src/tree-sitter-c &&
              tree-sitter generate
          else
              echo "$RUNNER_OS not supported"
              exit 1
          fi

      - name: Install Julia grammar for tree-sitter
        run: |
          export JULIA="https://github.com/tree-sitter/tree-sitter-julia.git" &&
          if [ "$RUNNER_OS" == "Linux" ]; then
              git clone $JULIA /home/runner/src/tree-sitter-julia &&
              cd /home/runner/src/tree-sitter-julia &&
              tree-sitter generate
          elif [ "$RUNNER_OS" == "macOS" ]; then
              git clone $JULIA /Users/runner/src/tree-sitter-julia &&
              cd /Users/runner/src/tree-sitter-julia &&
              tree-sitter generate
          else
              echo "$RUNNER_OS not supported"
              exit 1
          fi

      - name: Check included languages (expecting Julia and C; but not Haskell)
        run: tree-sitter dump-languages

      - name: Test
        run: go test -v pkg/treesitter/treesitter_test.go -v
