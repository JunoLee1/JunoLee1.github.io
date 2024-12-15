---
layout: single
title: "[Python] Recursive Function"
categories: ["skill"]
tag: [algorithm, python,skill]
toc: true
toc_label: "Table of Contents"
toc_icon: "align-justify" # corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true
---

># What is recursion??

In general, when explained `recursion`, it initiates from fundamental principle whenever call information `push`, `end` and, `stop`, `pop` at the stack.

It is easier to understand a factory process. It is a process that various defunction(`workers`) find the answer by inputting information(`Inputed ingredients`). Followed 

># Charateristic of Recursion

1. Recursive is calling functions that do the same thing in different states.
2. It is unnecessary what recursive defunction do, although it is important to bring "return value" 
3. In case, the recursive defunction does not content under case, it could bring the unlimited loop

># Warning 

There is no a cycle. One easy way to determine if there is no cycle is to make sure that the factors or global variables used to determine the base case are only moving in the direction of getting closer to the base case.

