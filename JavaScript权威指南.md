# 《JavaScript权威指南》（第六版）学习笔记

## 第一章 JavaScript概述
## 第二章 词法结构
 
> **保留字**
>> 关键字
>>>break delete function return typeof 
>>>case do if switch var 
>>>catch else in this void 
>>>continue false instanceof throw while
>>>debugger finally new true with
>>>default for null


>>严格模式
>>>implements let private public yield
>>>interface package protected static

>>不是保留字，但严格模式下不能作为变量名、函数名、参数名
>>>arguments eval

>>若代码有可能运行在ECMAScript 3，则应当避免使用

>>> abstract double goto native static
>>> boolean enum implements package super 
>>> byte export import private synchronized
>>> char extends int protected throws
>>> class final interface public transient
>>> const float long short volatile

>> 全局变量和函数

>>> arguments encodeURI Infinity Nuber RegExp
>>> Array encodeURIComponent isFinite Object String 
>>> Boolean Error isNaN parseFloat SyntaxError
>>> Date eval JSON parseInt TypeError
>>> decodeURI EvalError Math RangeError undefined
>>> decodeURIComponent Function NaN ReferenceError URIError

* 为避免一些意想不到的情形，还是老实多敲分号，并借助EsLint进行检查；

## 第三章 类型、值和变量

> **数据类型**

>>原始类型（number、string、boolean、undefined、null) VS 对象（属性的集合，每个属性都是由“名/值对”构成)

>>拥有方法 VS 没有方法（undefined、null）

>>可变 VS 不可变   



> **数字**

>>不区分整数值和浮点数，所有数字均用浮点数值表示

  
>>能够表示的整数范围为 ±2<sup>53<sup/>

>> Math



>>>Math.pow() Math.round Math.ceil Math.floor() Math.abs() 
>>>Math.max() Math.min() Math.random() Math.PI Math.E 
>>>Math.sqrt() Math.pow() Math.sin/cos/atan() 


>>Js中的算术运算在溢出、下溢出或被零整除时不会报错，以 Infinity 或 -Infinity表示，基于它们的加减乘除运算结果是正负无穷大

>>NaN（not-a-number）

>>>零除以零返回NaN

>>>无穷大除以无穷大返回NaN

>>>给任意负数作开方运算返回NaN

>>>算术运算符与不是数字或无法转换为数字的操作数已使用时返回NaN

>>>NaN和任何值不相等，包括自身

>>>isNaN()，在参数为NaN或一个非数字值，返回true

>>>isFinite(),在参数不是NaN、INfinity、-Infinity时返回true 


> **日期和时间**

>>new DateO() getFullYear() getMonth() getDate() getDay() getHours() getMinutes()

> **文本**

>>字符串是一个组由16位值组成的不可变的有序序列，length是其所含16位值得个数，索引从零开始

>>在es5中，字符串直接量可以拆分成数行，每行必须以反斜线（\)结束，反斜线和行结束符都不算是字符串直接量的内容。

>>如果希望在字符串直接量中另起一行，可以使用转义字符\n

>>反斜线（\)有着特殊的用途，反斜线符号后加一个字符，就不再是表示它们的字面含义了

>>>\n \xA9(©️) \u03c0(π) \xXX（由两位十六进制数XX指定的Latin-字符）\uXXXX（由四位十六进制数XXXX制定的Unicode字符）

>>字符串的使用

>>> 如果将 + 运算符用于字符串，则表示字符串连接，将第二个字符串拼接在第一个之后 

>>>在Js中字符串是固定不变的，相应的方法都返回的是新字符串，原字符串本身并没有发生变化

>>>在es5中，字符串可以当做只读数组，即可以使用方括号[]来访问字符串中的单个字符（16位值）

>**模式匹配**

>>js使用Perl中的正则表达式语法，String和RegExp对象中军定义了利用正则表达式进行模式匹配和查找与替换的函数

>>RegExp是一种强大和常用的文本处理工具，在两条斜线之间的文本构成了一个正则表达式直接量，第二条斜线后也可以跟随一个或多个字母（i、g等），用来修饰匹配模式的含义

>>字符串同样具有可以接受RegExp参数的方法

> **布尔值**

>>true、false

>>Js程序中的比较的结果通常都是布尔值

>>通常将一个创建布尔值的比较与使用这个比较的语句结合在一起 

>>六种假值：undefined、null、NaN、0(±0)、“”，false

>>所有对象都会被转换为true

>>三个布尔值运算

>>>&&运算符执行了逻辑与（AND)操作，同真则为真，一假则为假

>>>||运算符是布尔或（OR)操作，一真则为真，同假方为假

>>>！运算符执行了布尔非操作，假为真，真作假

> **null和undefined**

>>null

>>>用来描述“空值”，typeof运算返回“object”,，可以将null认为是一个特殊的对象值，含义是“非对象”

>>>null是它自有类型的唯一一个成员，它可以表示数字、字符串和对象是“无值”的

>>undefined

>>>用来表示值得空缺，它是变量的一种取值，表示变量没有初始化，如果要查询对象属性或数组元素的值时返回undefined则说明这个属性或元素不存在；

>>>如果函数没有返回任何值，则返回undefined

>>>引用没有提供实参的函数形参的值也只会得到undefined

>>>undefined是预定义的全局变量，它和null不一样，并不是关键字，它的值就是“未定义”

>>>undefined在es3中可读/写，es5做了修正，变为只读

>>>它是undefined类型的唯一成员

>>>尽管null 和undefined是不同的，但它们都表示“值得空缺”,两者往往可以互换，判断相等运算符“==”认为两者是相等的

>>>undefined和null都不包含属性和方法，使用“."和“[]"来存取这两个值得成员或方法都会产生一个类型错误

>>>如果想将它们赋值给变量或者属性，或者将它们作为参数传入函数，最佳选择是使用null

> 全局对象

> 








































