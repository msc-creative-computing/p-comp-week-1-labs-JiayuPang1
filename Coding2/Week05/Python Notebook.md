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

## List

### 列表（list）是最常用的Python数据类型，它可以作为一个方括号内的逗号分割值出现。

### List中的数据项不需要具有相同的类型，可以进行的操作包括索引（第一个索引是0，第二个索引是1，以此类推）、切片、加、乘、检查成员等。


### 创建一个列表，只要把逗号分割的不同的数据项使用方括号括起来即可，如下所示：

### list1 = [‘physics', ‘chemistry', 1997, 2000]（，数字直接写，字符用“”） ??????

### list2 = [1,2,3,4,5]

### list3 = ["a", "b", "c", "d"]

### 与字符串的索引一样，List索引从0开始，可以进行截取、组合等操作

### 访问列表中的值

### 使用下标索引来访问列表中的值，同样你也可以使用方括号的形式截取字符，如下所示：

### list1[0]   #取第一个元素

### list1[-1]  # 取最后一个元素

### list1[ : ] / list1[ : len(list1)]  # 取所有列表元素

### list1[0 : n] # 从第0号取到n-1号元素

### 输出如下：
 
![image](https://user-images.githubusercontent.com/92034503/158813683-09ac7da0-0cf3-43f4-b4a3-e18d36762124.png)
