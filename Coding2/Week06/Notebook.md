## Notebook
# Coding02-Week06
# Basic Python Libraries

## import
import()是python的一个内置函数，用于动态加载 类和函数。

## numpy
NumPy(Numerical Python) 是 Python 语言的一个扩展程序库，支持大量的维度数组与矩阵运算，此外也针对数组运算提供大量的数学函数库。

通常读音【num pai】

## pandas
Pandas是python的一个数据分析包，提供了大量能使我们快速便捷地处理数据的函数和方法。

## as
导入模块时对模块进行重命名，也就是给模块起一个别名。
————————————————

版权声明：本文为CSDN博主「sylbiubiubiu」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/sylbiubiubiu/article/details/114956075


## help & dir

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

