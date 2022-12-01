---
title: Announcing Semantic Diff Tool
author: David Mertz, Ph.D.
date: December 1, 2022
---

Welcome to [Atlantis Techology](https://www.atlantistech.com/)'s [Semantic Diff
Tool](https://www.sdt.dev).  This tool is Free Libre Open Source Software
(FLOSS), under a BSD license, which we hope will prove useful to software
developers.

The command-line tool `sdt` compares source files to identify which changes
create semantic differences in the program operation, and specifically to
exclude many changes which cannot be *functionally important* to the
operation of a program or library.  Numerous programming languages are
supported "out of the box", and even more are supported if you install the
widely used tree-sitter parser generator.

Use of `sdt` will allow code reviewers or submitters to assure that
modifications made to improve stylistic formatting of the code—whether made
by hand or using code-formatting tools—does not modify the underlying
*meaning* of the code.

As designed, the tool is much more likely to produce false positives for the
presence of semantic changes than false negatives.  That is to say, `sdt`
might indicate that a certain segment of the diff between versions is
*likely* to contain a semantic difference in code, but upon human
examination, a developer might decide that no actual behavior will change
(or, of course, she might decide that the change in code behavior is a
desired change).

It is unlikely that `sdt` will identify an overall file change, or any
change to a particular segment of a diff as semantically irrelevant where
that change actually does change behavior.  SDT will ease the work of your
human developers and your CI/CD process to make final decisions on whether
to accept code changes.

A quick example of usage shows an overview of capabilities (the switches
added simply minimize the output context and remove reliance on colorized
output).  The comparison shown compares what is currently on disk to the
HEAD of the working git branch (many other combinations are enabled with
command flags).

```
% sdt semantic --dumbterm --minimal 2>/dev/null
Changes to be committed:
    modified:   .github/workflows/test-treesit.yaml
| No available semantic analyzer for this format
    new file:   pkg/types/types_test.go
Changes not staged for commit:
    modified:   samples/filter.rb
| Segments with likely semantic changes
| @@ -3,4 +3,4 @@ def mod5?(items)
| -puts mod5? 1..100
| +puts mod5? 1..50
    modified:   samples/funcs.py
| No semantic differences detected
    modified:   samples/running-total.sql
|        count(DISTINCT co.order_id) AS {{-num_}}order{{-s}}{{+_count}},
```

Integration with version control workflows, programming editors, and git
subcommands is straightforward, and largely discussed in the [tool
documentation](https://www.sdt.dev).
