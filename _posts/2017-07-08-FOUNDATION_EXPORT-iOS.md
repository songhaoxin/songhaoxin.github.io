---
layout: post
title: FOUNDATION_EXPORT 与 #define
categories: 技术
description: 
keywords: FOUNDATION_EXPORT
---


FOUNDATION_EXPORT 与 #define 都可以用来定义常量  
.h文件  

```
FOUNDATION_EXPORT  NSString *const kMyConstantString;
```

.m 文件是这样定义的

```
NSString *const kMyConstantString = @"hello world";
```

另一种就是常用的 #define 方法定义常量了

```
#define kMyConstantString @"Hello"
```

那么他们有什么区别呢?
使用FOUNDATION_EXPORT方法在检测字符串的值是否相等的时候效率更快.
可以直接使用(myString == MyFirstConstant)来比较, 而define则使用的是([myString isEqualToString:MyFirstContant])
哪个效率更高,显而易见了

#####第一种是直接比较指针地址
#####第二种则是一一比较字符串的每一个字符是否相等.

