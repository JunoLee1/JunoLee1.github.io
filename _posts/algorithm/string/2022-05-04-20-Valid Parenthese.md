---
layout: single
title: "[string] Leetcode #20 valid parenthese"
categories: ["string"]
tag: [algorithm, string, leetcode]
toc: true
toc_label: "Table of Contents"
toc_icon: "align-justify" # corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true
---

># description of the problem

finding right mate of parenthese

># logic 

using the stack method which means `Last in, first out`.

```Python
class Solution:
    def isValid(self, s: str) -> bool:
        cha ={"(":")","[":"]","{":"}"}
        stack = []
        for i in range(len(s)):
            parenthese = s[i]
            if parenthese in cha.keys():
                stack.append(parenthese)
            else :
                if stack == []:
                    return False
                else:
                    pop = stack.pop()
                    if parenthese != cha[pop]:
                        return False
        if stack == []:
            return True
            


```