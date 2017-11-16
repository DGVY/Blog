---
title: C++-数组
date: 2017-11-15 20:38:30
tags:
- C++
- 数组
categories:
- C++
---

```cpp
    int *ptrs[10];              // ptrs是含有10个整形指针的数组
    int &refs[10] = /* ?*/;     // 错误，不存在的引用数组
    int (*Parray)[10] = &arr;   // Parray指向一个含有10个整数的数组
    int (&arrRef)[10] = arr;    // arrRrf引用一个含有10个整数的数组
    int *(&arry)[10]  = ptrs;   // arry是数组的引用，该数组含有10个指针
```

* *想要理解数组声明的含义，最好的办法是从数组的名字开始，按照由内向外的顺序阅读。*
