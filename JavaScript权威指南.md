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

>>**NaN（not-a-number）**

>>>零除以零返回NaN

>>>无穷大除以无穷大返回NaN

>>>给任意负数作开方运算返回NaN

>>>算术运算符与不是数字或无法转换为数字的操作数已使用时返回NaN

>>>NaN和任何值不相等，包括自身

>>>isNaN()，在参数为NaN或一个非数字值，返回true

>>>isFinite(),在参数不是NaN、INfinity、-Infinity时返回true 











































