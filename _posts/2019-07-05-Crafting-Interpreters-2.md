---
layout:     post                    # 使用的布局（不需要改）
title:      Crafting Interpreters 读书笔记(2)               # 标题 
date:       2019-07-05              # 时间
author:     twhhome                      # 作者
header-img: img/post-bg-crafting-interpreters-2.png    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - Java
    - C++
    - Interpreter

---

「Crafting Interpreters」本书地址：[Crafting Interpreters](http://www.craftinginterpreters.com)

# Lox 语言

## 数据类型

* **布尔(Booleans)**
  ```
  true; // Not false
  false; // Not *not* false
  ```
* **数值(Numbers)** - Lox只有一种数值类型：双精度浮点数。
  ```
  1234; // An integer
  12.34 // A decimal number
  ```
* **字符串(Strings)** - 用双引号表示
  ```
  "I am a string";
  ""; // an empty string
  "123"; // this is a string, not a number
  ```
* **空值(Nil)** - 在Lox语言里用`nil`来表示空值。

## 表达式(Expression)

### *算术(Arithmetic)*
```
add + me;
subtract - me;
multiply * me;
divide / me;
```

### *比较(Comparison)和相等(Equality)*
```
less < than;
lessThan <= orEqual;
greater > than;
greaterThan >= orEqual;
```
```
1 == 2; // false
"cat" != "dog"; // true
```

### *逻辑运算符(Logical operators)*
```
!true; // false
!false; // true
```
```
true and false; // false
true and true; // true
```
```
false or false; // false
true or false; // true
```

### *优先顺序(Precedence)和分组(Grouping)*
所有的操作符的优先顺序(precedence)和关联(associativity)都和C语言一样。如果优先级不是你想要的，你可以使用()对内容进行分组：
```
var average = (min + max) / 2;
```

## 声明(Statements)
```
print "Hello, world!";
"some expression";
{
	print "One statement.";
    print "Two statements.";
}
```

## 变量(Variables)
你可以用`var`来声明变量。如果你省略初始化，变量的值就会默认设为`nil`:
```
var imAVariable = "here is my value";
var iAmNil;
```

## 控制流(Control Flow)
```
if(condition) {
	print "yes";
} else {
	print "no";
}
```
```
var a = 1;
while(a < 10) {
	print a;
    a = a + 1;
}
```
```
for(var a = 1; a < 10; a = a + 1) {
	print a;
}
```

## 函数(Functions)
```
makeBreakfast(bacon, eggs, toast);
```
```
makeBreakfast();
```
在Lox语言里，用`fun`来定义一个函数：
```
fun printSum(a, b) {
	print a + b;
}
```
你可以用`return`来返回一个值：
```
fun returnSum(a, b) {
	return a + b;
}
```
如果没有`return`语句，函数隐性返回`nil`。