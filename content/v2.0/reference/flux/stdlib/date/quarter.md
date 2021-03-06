---
title: date.quarter() function
description: >
  The `date.quarter()` function returns the quarter of the year for a specified time.
  Results range from `[1-4]`.
aliases:
  - /v2.0/reference/flux/functions/date/quarter/
menu:
  v2_0_ref:
    name: date.quarter
    parent: Date
weight: 301
---

The `date.quarter()` function returns the quarter of the year for a specified time.
Results range from `[1-4]`.

_**Function type:** Transformation_  

```js
import "date"

date.quarter(t: 2019-07-17T12:05:21.012Z)

// Returns 3
```

## Parameters

### t
The time to operate on.

_**Data type:** Time_
