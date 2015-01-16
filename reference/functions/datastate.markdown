---
layout: default
title: datastate
published: true
tags: [reference, data functions, functions, json, datastate, evaluation, vars, classes, container]
---

[%CFEngine_function_prototype()%]

**Description:** Returns the current evaluation data state.

The returned data container will have the keys ```classes``` and ```vars```.

Under ```classes``` you'll find a map with the class name as the key and
`true` as the value.  Namespaced classes will be prefixed as usual.

Under ```vars``` you'll find a map with the bundle name as the key
(namespaced if necessary).  Under the bundle name you'll find another
map with the variable name as the key.  The value is converted to a
data container (JSON format) if necessary.  The example should make it
clearer.

Mustache templates (see `template_method`), if not given a
`template_data`, will use the output of `datastate()` as their input.

[%CFEngine_function_attributes()%]

**Example:**

[%CFEngine_include_snippet(datastate.cf, #\+begin_src cfengine3, .*end_src)%]

Output:

[%CFEngine_include_snippet(datastate.cf, #\+begin_src\s+example_output\s*, .*end_src)%]

**See also:** `getindices()`, `classesmatching()`, `variablesmatching()`, `mergedata()`, `template_method`, `mustache`, `bundlestate()`
