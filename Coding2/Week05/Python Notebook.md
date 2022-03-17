## Notebook
# Coding02-Week05
# Python
## 注意 ：在Jupyter上输入代码让其run的快捷键是（shift+回车）
![图片 32](https://user-images.githubusercontent.com/92034503/158812855-b9bc8525-57fb-487c-b8bf-e7faba742282.png)
### 在python里不需要声明数据类型，直接写就好
这句话的意思是：我们不需要在敲代码前先向计算机声明我们输入的类型是什么，只需要记清不同类型的表达式，机器会自动判断
当不同类型的方程拥有同样的表达式时，机器会自动筛查，所以有时候也会出现写错但不报错的情况，因为它虽然不满足你想写的表达式，但却满足了另一函数的语法。
We don't need to declare to the computer what type we are typing, just remember the different types of expressions, and the machine will decide
When different types of equations have the same expression, the machine will automatically screen, so sometimes there will be no error, because it does not satisfy the expression you want to write, but it does satisfy the syntax of another function.

## print(type(data具体你写入的数据))
相应的如果你不清楚你写入的data属于什么类型，你可以通过print(type(data具体你写入的数据))
运行它 它将会告诉你
<img width="413" alt="图片 33" src="https://user-images.githubusercontent.com/92034503/158813207-1613166c-54ec-4f16-9c97-40836e9fd02a.png">
### int：整数  str：字符串

## Python的数据类型：

<img width="432" alt="图片 34" src="https://user-images.githubusercontent.com/92034503/158813309-206caab3-cf2d-4b9b-b2b7-4f8ff3070783.png">

## python Arrays

<img width="433" alt="图片 35" src="https://user-images.githubusercontent.com/92034503/158813593-5ae88a8c-33b1-45c9-b3d2-75a009cfff16.png">

## 1. List

##### 列表（list）是最常用的Python数据类型，它可以作为一个方括号内的逗号分割值出现。

##### List中的数据项不需要具有相同的类型，可以进行的操作包括索引（第一个索引是0，第二个索引是1，以此类推）、切片、加、乘、检查成员等。


##### 创建一个列表，只要把逗号分割的不同的数据项使用方括号括起来即可，如下所示：

##### list1 = [‘physics', ‘chemistry', 1997, 2000]（，数字直接写，字符用“”） ??????

##### list2 = [1,2,3,4,5]

##### list3 = ["a", "b", "c", "d"]

### 与字符串的索引一样，List索引从0开始，可以进行截取、组合等操作

### 访问列表中的值

### 使用下标索引来访问列表中的值，同样你也可以使用方括号的形式截取字符，如下所示：

##### list1[0]   取第一个元素

##### list1[-1]  取最后一个元素

##### list1[ : ] / list1[ : len(list1)] 取所有列表元素

##### list1[0 : n] # 从第0号取到n-1号元素

### 输出如下：
 <img width="202" alt="图片 36" src="https://user-images.githubusercontent.com/92034503/158815021-6793b0af-d670-426b-b55f-36c7793c1879.png">
 
更新列表
可以对列表的数据项进行修改或更新，也可以使用append()方法来添加列表项，如下所示：

list1[0] = ‘D'       # 修改元素值
list1.append(‘E')    # 列表添加元素
list1.insert(0 , 'F')   # 在某处插入元素

具体示例：

![图片 37](https://user-images.githubusercontent.com/92034503/158815635-b63d00e1-054d-4a8e-af68-9329e0c9fb0e.png)

删除列表元素
可以使用del语句来删除列表的元素。

del list1[0]       　　　　　　　　    # 删除元素  
list1.remove(‘1') 　　　　　　　　　 # 移除第一次出现的元素
所以下面的例子最后一个1没有被移除
![图片 38](https://user-images.githubusercontent.com/92034503/158815953-29f3aac2-8cdb-403d-b293-badf02a252ed.png)

list1.pop()   　　　　　　　　　　　　# 移出元素，默认从最后移出，返回该元素值；
括号中可加入元素索引值来移除

## 2.	Tuple


tuple也是一个class，是不可变的list类型，不可以增删改

①、Tuple 与 list 的相同之处

定义 tuple 与定义 list 的方式相同, 除了整个元素集是用小括号（）包围的而不是方括号[ ]。
Tuple 的元素与 list 一样按定义的次序进行排序。 Tuples 的索引与 list 一样从 0 开始, 所以一个非空 tuple 的第一个元素总是 t[0]。
负数索引与 list 一样从 tuple 的尾部开始计数。
与 list 一样分片 (slice) 也可以使用。注意当分割一个 list 时, 会得到一个新的 list ；当分割一个 tuple 时, 会得到一个新的 tuple。

②、Tuple 不存在的方法

您不能向 tuple 增加元素。Tuple 没有 append 或 extend 方法。
您不能从 tuple 删除元素。Tuple 没有 remove 或 pop 方法。
然而, 您可以使用 in 来查看一个元素是否存在于 tuple 中。

③、用 Tuple 的好处

Tuple 比 list 操作速度快。如果您定义了一个值的常量集，并且唯一要用它做的是不断地遍历它，请使用 tuple 代替 list。
如果对不需要修改的数据进行 “写保护”，可以使代码更安全。使用 tuple 而不是 list 如同拥有一个隐含的 assert 语句，说明这一数据是常量。如果必须要改变这些值，则需要执行 tuple 到 list 的转换。

④、Tuple 与 list 的转换

Tuple 可以转换成 list，反之亦然。内置的 tuple 函数接收一个 list，并返回一个有着相同元素的 tuple。而 list 函数接收一个 tuple 返回一个 list。从效果上看，tuple 冻结一个 list，而 list 解冻一个 tuple。


————————————————
版权声明：本文为CSDN博主「A叶子叶」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/yezonggang/article/details/50976664


## 3.	Dictionary

字典是另一种可变容器模型，且可存储任意类型对象。

字典的每个键值(key=>value)对用冒号(:)分割，每个对之间用逗号(,)分割，整个字典包括在花括号({})中 ,格式如下所示：

d = {key1 : value1, key2 : value2 }


键必须唯一
值    不必

值可以取任何数据类型，键必须是不可变的，如字符串，数字或元组。
注意：dict 作为 Python 的关键字和内置函数，变量名不建议命名为 dict。


一个简单的字典实例：
dict = {‘Alice': ‘2341', ‘Beth': ‘9102', ‘Cecil': ‘3258'}

也可如此创建字典：
dict1 = { ‘abc': 456 };
dict2 = { ‘abc': 123, 98.6: 37 };
![图片 39](https://user-images.githubusercontent.com/92034503/158816273-66d1bbe9-a956-4185-b738-ad61cbfe9b07.png)
________________________________________________________________
myFunction
先定义，之后就可以直接拿来用了
def myFunc（x）：
for box in range（0，8，2）：expected an indented block
box = box * x           expected an indented block again
print  x
myFunc（2）

输出：
0
4
8
12
![图片 40](https://user-images.githubusercontent.com/92034503/158816395-097339ff-6ccf-40da-866b-9d65dda19fc5.png)

Keywords:
https://www.w3schools.com/python/python_ref_keywords.asp
注意在命名时不要起这些内置keywords



4.	Set
无序不重复元素集
>>>x = set('spam')
>>>y = set(['h','a','m'])
>>>x, y
(set(['a', 'p', 's', 'm']), set(['a', 'h', 'm']))





# python内置函数：


（1）	range

range()函数功能:

用于创建一个整数列表

range函数语法:

range(start, stop[, step])

-------参数说明------

start:计数从 start 开始。默认是从 0 开始。如range(8)等价于range(0,8)

stop:计数到 stop 结束，但不包括 stop。如：range(0,8) 是[0,1,2,3,4,5,6,7]没有8

step步长，默认为1。例如：range(0,8)等价于 range(0,8,1)

-------返回值------
Python range函数示例分享

>>> print (list(range(8)))

[0, 1, 2, 3, 4, 5, 6, 7]

>>> print (list(range(0,8)))

[0, 1, 2, 3, 4, 5, 6, 7]

>>> print (list(range(0,8,2)))

[0, 2, 4, 6]

>>> print (list(range(0)))

[]

>>> print (list(range(2,0)))

[]

>>> print (list(range(2,0)))

[]

>>> print (list(range(0,-10)))

[]

>>> print (list(range(0,-10,-1)))

[0, -1, -2, -3, -4, -5, -6, -7, -8, -9]
>>> print (list(range(0,-10,-2)))

[0, -2, -4, -6, -8]

//range结合for循环遍历字符串

>>> t ="maomao365.com"

>>> for i in range(len(t)):（for i in range（）代表给i赋值，赋值的范围及括号里的内容）

... print(t[i])

...

m

a

o

m

a

o

3

6

5

.

c

o

m

————————————————
版权声明：本文为CSDN博主「慈老湿」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/weixin_29619251/article/details/113501063


（2）	len
语法：len(str)
参数：
str：要计算的字符串、列表、字典、元组等
返回值：字符串、列表、字典、元组等元素的长度
实例
1.计算字符串的长度：
>>> s = "hello good boy doiido"
>>> len(s)
21
2、计算列表的元素个数：
>>> l = ['h','e','l','l','o']
>>> len(l)
5
3、计算字典的总长度(即键值对总数)：
>>> d = {'num':123,'name':"doiido"}
>>> len(d)
2
4、计算元组元素个数：
>>> t = ('G','o','o','d')
>>> len(t)
4
3.	输出字符串的最佳连接方式是：
print (“ hello world {}”.format())
e,g, 
x= “100”
y= “5”
z= “i am Jiayu”
print (“hello world {}{},{}”.format(x,y,z))
输出结果为：
<img width="432" alt="图片 41" src="https://user-images.githubusercontent.com/92034503/158816557-6054e699-5cf5-4048-bed6-749a6806b662.png">
<img width="235" alt="图片 42" src="https://user-images.githubusercontent.com/92034503/158816570-ed603570-9b9d-48b4-a7b4-0ac52228adb6.png">
虽然python可以直接在print的（）里通过“+”来进行输入内容的连接，但是有时会因为类型导致不run的情况，因此  如上图mick的文字总结。

import numpy as np 和 import pandas as pd

（3）import
import()是python的一个内置函数，用于动态加载 类和函数。

（4）numpy
NumPy(Numerical Python) 是 Python 语言的一个扩展程序库，支持大量的维度数组与矩阵运算，此外也针对数组运算提供大量的数学函数库。

通常读音【num pai】

（5）pandas
Pandas是python的一个数据分析包，提供了大量能使我们快速便捷地处理数据的函数和方法。

（6）as
导入模块时对模块进行重命名，也就是给模块起一个别名。
————————————————
版权声明：本文为CSDN博主「sylbiubiubiu」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/sylbiubiubiu/article/details/114956075


## 4. help & dir

但是如何获得关于特定python对象或命令的更多信息呢? 主要有两种方式:

### 方法一：help(… )
![图片 43](https://user-images.githubusercontent.com/92034503/158816767-3b5b92a1-dc9a-4d1e-bb06-fa1f1c6d6391.png)

### example
![图片 44](https://user-images.githubusercontent.com/92034503/158816840-5fbb0dd7-470c-4bfb-9ce6-40c8cc730efa.png)
### 方法二：dir(… )

![图片 45](https://user-images.githubusercontent.com/92034503/158816990-4dfd465c-d4c1-4f35-804d-6adb0b36eba6.png)

### example
![图片 46](https://user-images.githubusercontent.com/92034503/158817022-4c081126-3594-485c-9465-114c2335c727.png)
## · Matplotlib

https://matplotlib.org/  

(在这个网站上你可以找到一些具体的例子 各种图表类型2D/3D/动图…)

matplotlib is a library for plotting data using an approach similar to that which can be found in the popular research software Matlab. It is designed to allow you to create plots that are publication quality, but in general, it's just a great tool for seeing what you are doing.

matplotlib是一个用于绘制数据的库，使用的方法类似于在流行的研究软件Matlab中找到的方法。它的设计目的是让你创建具有出版质量的情节，但总的来说，它只是一个很好的工具，可以看到你在做什么。



e.g.

import matplotlib.pyplot as plt
import math

x = range(100) 
y = []

for value in x:
    y.append(math.tan(value*0.1))

plt.plot(y)
![图片 47](https://user-images.githubusercontent.com/92034503/158817133-a6a7e837-9ca6-47c7-a1f4-68e70f833159.png)

## · Numpy

https://numpy.org/

Numpy是最强大、最重要的Python包之一。它非常适合处理多维数组(例如大块数据)，并具有一些令人印象深刻的内建函数，用于做向量处理和线性代数。一般来说，如果你想处理大量的数字，你应该使用Numpy。Numpy数组比Python列表要强大得多。它们允许您创建和操作信息数组，比如大块的图像数据，并快速处理它。
![图片 48](https://user-images.githubusercontent.com/92034503/158817470-bffada24-b45c-4ac8-80dd-837f4c72e343.png)

## ·Pandas

老实说，人们使用pandas的主要原因是它可以读取微软的excel文件和cv文件。这使得那些自然使用excel收集和组织数据的人更加方便。

这里有一个很好的教程，教你如何将excel文档导入和使用到Python中

https://www.dataquest.io/blog/excel-and-pandas/

And this cheatsheet is pretty great.

https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf

https://pandas.pydata.org/docs/index.html
![图片 49](https://user-images.githubusercontent.com/92034503/158817698-2b0528b0-dfa9-4813-81e8-9235682b0484.jpg)
![图片 50](https://user-images.githubusercontent.com/92034503/158817717-dec0218a-8848-47e1-9db4-1986dc799780.jpg)

## ·Urllib

https://pythonspot.com/urllib-tutorial-python-3/

这是一个非常重要的Python库，你们会经常用到。您可以做很多很酷的事情，使抓取数据变得更容易，包括指定用户代理，这基本上意味着假装成任何您喜欢的浏览器。

It's super easy to use urllib to grab a webpage:
![图片 51](https://user-images.githubusercontent.com/92034503/158817856-b5011962-e021-40bb-b777-6233c41d70c1.png)
## · Bs4

bs4，或称“Beautiful Soup”，是一个很棒的html解析器，也是大量web抓取软件的基础。如果您正在构建一个scraper，您应该从bs4开始。下面是一个脚本的例子，它抓取一些网页数据，并使用bs4对其进行迭代。
![图片 52](https://user-images.githubusercontent.com/92034503/158817998-4337f74d-3406-4ec0-89db-8f66ce0ab41a.png)
<img width="432" alt="图片 53" src="https://user-images.githubusercontent.com/92034503/158818011-77b70ed4-fa81-419d-9011-a9ef4821e1bd.png">
## · Bokeh

是创建交互式绘图的好方法
让您可以非常轻松地制作可以在网页上与之交互的情节。

matplotlib 不是为交互式绘图生成而设计的——它是为书籍和学术论文生成绘图的。

from bokeh.plotting import figure, output_file, show

# prepare some data
x = [1, 2, 3, 4, 5]
y = [6, 7, 2, 4, 5]

# output to static HTML file
output_file("lines.html")

# create a new plot with a title and axis labels
p = figure(title="simple line example", x_axis_label='x', y_axis_label='y')

# add a line renderer with legend and line thickness
p.line(x, y, legend="Temp.", line_width=2)

# show the results
show(p)
<img width="432" alt="图片 54" src="https://user-images.githubusercontent.com/92034503/158818159-cb65ee66-d618-4d2c-ad14-bef152fba039.png">
![图片 55](https://user-images.githubusercontent.com/92034503/158818179-6c1dbc4d-d3af-48a3-9eb9-82ec370858fc.png)

## ·Genism

如果您对数据挖掘感兴趣，有兴趣了解如何使用机器学习从文本中提取意义。
genism是一个很棒的工具。这就是你应该开始的地方。好的。

