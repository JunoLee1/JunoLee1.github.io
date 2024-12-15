---
layout: single
title: "[Array] Leetcode #70 Climbing Stairs"
categories: ["array"]
tag: [algorithm, array, leetcode]
toc: true
toc_label: "Table of Contents"
toc_icon: "align-justify" # corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true
---


># description of the problem

The problem is how to count the way of climbing stairs.

># logic 

f(n) =f(n-1) +f(n-2)
f(1) = 1
f(2) = 2
f(3) = 3 
f(4) = 5 (f(3)+f(2))
.
.
. 
f(n) = f(n-1) +f(n-2)





```python
class Solution:
    def climbStairs(self, n: int) -> int:
        if n == 1:
            return 1
        if n == 2:
            return 2
        else :
            return self.climbStairs(n-1)+ self.climbStairs(n-2)
```






