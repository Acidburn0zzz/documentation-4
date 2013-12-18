---
layout: default
title: intersection
categories: [Reference, Functions, intersection]
published: true
alias: reference-functions-intersection.html
tags: [reference, data functions, functions, intersection]
---

[%CFEngine_function_prototype(list1, list2)%]

**Description:** Returns the unique elements in list1 that are also in list2.

[%CFEngine_function_attributes(list1, list2)%]

**Example:**

[%CFEngine_include_snippet(intersection.cf, #\+begin_src cfengine3, .*end_src)%]

Output:

[%CFEngine_include_snippet(intersection.cf, #\+begin_src\s+example_output\s*, .*end_src)%]

**See also:** [`difference()`][difference].
