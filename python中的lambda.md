# 匿名函数lambda的用法：
Python中，lambda函数也叫匿名函数，及即没有具体名称的函数，它允许快速定义单行函数，类似于C语言的宏，可以用在任何需要函数的地方。这区别于def定义的函数。
lambda与def的区别：
1）def创建的方法是有名称的，而lambda没有。
2）lambda会返回一个函数对象，但这个对象不会赋给一个标识符，而def则会把函数对象赋值给一个变量（函数名）。
3）lambda只是一个表达式，而def则是一个语句。
4）lambda表达式” : “后面，只能有一个表达式，def则可以有多个。
5）像if或for或print等语句不能用于lambda中，def可以。
6）lambda一般用来定义简单的函数，而def可以定义复杂的函数。
6）lambda函数不能共享给别的程序调用，def可以。
lambda语法格式：
lambda 变量 : 要执行的语句

lambda [arg1 [, agr2,.....argn]] : expression

1、单个参数的：
>>> g = lambda x : x ** 2
>>> print g(3)
9
2、多个参数的：
>>> g = lambda x, y, z : (x + y) ** z
>>> print g(1,2,2)
9

>>> list_a = [lambda a: a**3, lambda b: b**3]
>>> list_a[0]
<function <lambda> at 0x0259B8B0>
>>> g = list_a[0]
>>> g(2)
8

这里就没法用def语句代替了，语句是不能嵌套在里面的。lambda表达式中，冒号前面是参数，可以有多个，用逗号分隔，冒号右边是返回值。
lambda具体用不用，视情况而定吧，有时候使用lambda可以简化代码。
