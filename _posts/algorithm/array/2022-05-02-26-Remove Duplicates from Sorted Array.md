---
layout: single
title: "[Array] Leetcode #26 Remove Duplicates from Sorted Array"
categories: ["array"]
tag: [algorithm, array, leetcode]
toc: true
toc_label: "Table of Contents"
toc_icon: "align-justify" # corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true
---
> # Problem description 

This problem is poping off duplicated content in the list


> # Logic

By using the `two pointer`, I could solve this problem.
This algorithm could deal with this problem, recording `two pointer's` location. 





 
> # Code

```python
class Solution:
    def removeDuplicates(self, nums: List[int]) -> int:
        j = 0
        for i in range(1,len(nums)):
            if nums[i] != nums[j]:
                j += 1
                nums[j] = nums[i]
        return j+1
```
        
