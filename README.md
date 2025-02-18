# Lua Nested Table Iteration Bug

This repository demonstrates a potential issue when iterating over nested tables in Lua using the `pairs` function.  The `pairs` iterator does not guarantee any particular order, which can lead to unexpected results if you modify the table during iteration, especially in nested structures.

The `bug.lua` file contains code that exhibits this problem. The `bugSolution.lua` file provides a corrected approach.

## Bug
The `pairs` iterator is used to traverse a nested table.  However, because the order of iteration is not defined, modifications made to the table within the loop might not behave as expected, potentially leading to skipped elements or incorrect updates.