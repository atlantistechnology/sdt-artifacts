---
title: VS Code extension for Semantic Diff Tool
date: December 3, 2022
---

# VS Code extension

In the current version 0.1.0, the [VS Code
extension](semantic-diff-tool-0.1.0.vsix) has only basic functionality.
Specifically, the command "Semantic Diff Tool" (shortcut "sdt") will simply
make a call to `sdt semantic -m -d` and display the results in a new window
(annotated by timestamp of the operation).  If `sdt` is not installed, a
friendly error message should provide a reminder.

Currently, this extension must use the "Install from VSIX" approach.  If or
when we add significant functionality, we will publish to the VS Code
Extension Marketplace.  However, since installation of `sdt` itself cannot
easily be integrated into a VS Code extension, publication is less pressing.

The default key-binding for the "Semantic Diff Tool" extension is 
*ctrl+alt+d*, or on MacOS, *ctrl+cmd+d*.
