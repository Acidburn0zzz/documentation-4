---
layout: default
title: mapdata
published: true
tags: [reference, data functions, functions, mapdata]
---

[%CFEngine_function_prototype(interpretation, pattern, array_or_container)%]

**Description:** Returns a data container holding a JSON array. The
array is a map across each element of `array_or_container`, modified by
a `pattern`. The map is either collected literally when `interpretation`
is `none` or parsed as JSON when `interpretation` is `json`.

`array_or_container` can be a data container.

The `$(this.k)` and `$(this.v)` variables expand to the key and value
of the current element, similar to the way `this` is available for
`maplist`.

If the array or data container has two levels, you'll also be able to
use the `$(this.k[1])` variable for the key at the second level. See
the example below for an illustration.

The order of the keys is not guaranteed. Use the `sort` function if
you need order in the resulting output.

[%CFEngine_function_attributes(interpretation, pattern, array_or_container)%]

**Example:**

[%CFEngine_include_snippet(mapdata.cf, #\+begin_src cfengine3, .*end_src)%]

Output:

[%CFEngine_include_snippet(mapdata.cf, #\+begin_src\s+example_output\s*, .*end_src)%]

**See also:** `maplist()`, `maparray()`, and `data` documentation.

**History:** Was introduced in 3.7.0
