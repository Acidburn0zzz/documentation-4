---
layout: default
title: join
categories: [Reference, Functions, join]
published: true
alias: reference-functions-join.html
tags: [reference, data functions, functions, join]
---

[%CFEngine_function_prototype(glue, list)%]

**Description:** Join the items of `list` into a string, using the conjunction in `glue`.

Converts a string of type list into a scalar variable using the join
string in first argument.

[%CFEngine_function_attributes(glue, list)%]

**Example:**

[%CFEngine_include_snippet(join.cf, #\+begin_src cfengine3, .*end_src)%]

Output:

[%CFEngine_include_snippet(join.cf, #\+begin_src\s+example_output\s*, .*end_src)%]
