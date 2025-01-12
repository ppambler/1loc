---
title: Repeat an array
category: Array
tags:
  - posts
layout: layouts/post.njk
---

```js
// `arr` is an array
const repeat = (arr, n) => [].concat(...Array(n).fill(arr));

// Or
const repeat = (arr, n) => Array(n).fill(arr).flat();

// Or
const repeat = (arr, n) => Array(arr.length * n).fill(0).map((_, i) => arr[i % arr.length]);

// Or
const repeat = (arr, n) => Array.from({ length: arr.length * n }, (_, i) => arr[i % arr.length]);

// Examples
repeat([1, 2, 3], 3);       // [1, 2, 3, 1, 2, 3, 1, 2, 3]
```