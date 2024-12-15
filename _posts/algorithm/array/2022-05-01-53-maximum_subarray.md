---
layout: single
title: "[Array] Leetcode #53 Maximum Subarray"
categories: ["array"]
tag: [algorithm, array, leetcode]
toc: true
toc_label: "Table of Contents"
toc_icon: "align-justify" # corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true
---

> # Problem description 

This is Maximum Subarray question from the Leetcode.

> # Code

```python
class Solution:
    def maxSubArray(self, nums: List[int]) -> int:
            curr_sum = 0
            max_sum = nums[0]
            for i in range(len(nums)):
                curr_sum = max(curr_sum+nums[i],nums[i])
                max_sum = max(curr_sum,max_sum)
            return max_sum
```
        
