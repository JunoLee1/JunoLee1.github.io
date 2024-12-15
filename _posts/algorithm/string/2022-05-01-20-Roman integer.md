---
layout: single
title: "[Array] Leetcode #13 Roman Integer"
categories: ["string"]
tag: [algorithm, string, leetcode]
toc: true
toc_label: "Table of Contents"
toc_icon: "align-justify" # corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true
---
> # Problem description 

This is Roman Integer question from the Leetcode.

> # Logic

The logic was far more interesting because of `i < len(s)-1`.
Limiting scope `i < len(s)-1`, it could stop being over scope(or index).
Comparing the `val` which is the present value of the romanDict with the next value, if the `val` is smaller than the next value, `subtract` val from the next one. However, if the val bigger than the new one, `add` them 


> # Code

```python
class Solution:
    def romanToInt(self, s: str) -> int:
        romanDict = {'M':1000, 'D':500, 'C':100, 'L':50, 'X':10, 'V':5, 'I':1}
        arabic = 0
        
        for i in range(len(s)):
            val = romanDict[s[i]]
            if (i < len(s)-1) and val < romanDict[s[i+1]]:
                arabic -= val
            else :
                arabic += val
        return arabic
```
        