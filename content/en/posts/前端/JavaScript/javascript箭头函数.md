---
title: "Javascript箭头函数"
date: 2023-12-02T10:40:16+08:00
categories: ["前端"]
tags: ["Javascript"]
draft: false
---

# 概述

## 箭头函数与常规函数对比

{{< codes 常规函数 箭头函数 带有块语法的箭头函数>}}
    {{< code >}}
```javascript
function funcName(params) {
    return params + 2;
}
funcName(2);
// 4
```
    {{< /code >}}
    {{< code >}}
```JavaScript
var funcName = (params) => params + 2
funcName(2);
// 4
```
    {{< /code >}}
    {{< code >}}
```javascript
// 如果使用块语法,需要指定 return 关键字.
var funcName = (params) => { return params + 2 }
funcName(2);
```
    {{< /code >}}
{{< /codes >}}

## 箭头函数不会绑定this,即箭头函数不会改变 this 本来的绑定.
1. 每个函数都会有自身的this，但是this并不是在函数声明完就绑定到某个对象上的，只有在函数调用时，this才会被绑定.
2. 常见的 this 指向
   1. 全局作用域中或者普通函数中 this 指向全局对象 window.
   2. 立即执行函数 this 指向全局对象 window.
   3. 定时器的 this 指向全局对象 window.
   4. 事件中的 this 指向事件源对象.
   5. 方法中的 this 谁调用就指向谁.
   6. 构造函数中的 this 指向对象实例.

{{< codes 常规函数 箭头函数 带有块语法的箭头函数>}}
    {{< code >}}
```javascript
function funcName(params) {
    return params + 2;
}
funcName(2);
// 4
```
    {{< /code >}}
    {{< code >}}
```JavaScript
var funcName = (params) => params + 2
funcName(2);
// 4
```
    {{< /code >}}
    {{< code >}}
```javascript
// 如果使用块语法,需要指定 return 关键字.
var funcName = (params) => { return params + 2 }
funcName(2);
```
    {{< /code >}}
{{< /codes >}}

## 参考链接
1. [this讲解1](https://juejin.cn/post/7035257186565488670)
2. [this讲解2](https://zhuanlan.zhihu.com/p/27108622)