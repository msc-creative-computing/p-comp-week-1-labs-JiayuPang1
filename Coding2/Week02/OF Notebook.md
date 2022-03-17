## Notebook
# Coding02-Week02
# OpenFrameworks
shop4ducks.co.uk
安装和使用教程：https://openframeworks.cc/setup/xcode/
![图片 14](https://user-images.githubusercontent.com/92034503/158804684-d344c4cc-006f-4ad5-a3bf-546ee510d6fc.png)
![图片 15](https://user-images.githubusercontent.com/92034503/158804697-21ced6e7-19d1-46c1-8460-27dcc7343534.png)
![图片 16](https://user-images.githubusercontent.com/92034503/158804714-c8621d15-f7cf-4bc4-8222-0d3a310e24d1.png)

## 从其他GitHub分享者那里下载文件:
![图片 17](https://user-images.githubusercontent.com/92034503/158804865-065a2ce1-8c3f-42d6-8ec3-e1d5737cacbd.png)

### 复制链接

<img width="432" alt="图片 18" src="https://user-images.githubusercontent.com/92034503/158805007-924e709b-4cc0-4639-81db-9e5388c10c29.png">

### 打开终端
### 输入：git clone + 复制的链接 +按回车键
<img width="432" alt="图片 19" src="https://user-images.githubusercontent.com/92034503/158805134-755a4be6-fea6-4285-925a-881ac716b236.png">
### 复制的东西成功被加载

## Part3
![图片 20](https://user-images.githubusercontent.com/92034503/158805257-4905c67d-352a-47ad-b2fb-990bbea447cb.png)
### & 可用这个符号获得变量地址（如上图解析）

![图片 21](https://user-images.githubusercontent.com/92034503/158805335-1f92794b-ff19-4047-bf09-02cb16b8b182.png)
### * 可用此符号创建一个指针，指针指向数据的地址
![图片22](https://user-images.githubusercontent.com/92034503/158805418-562fb8c6-c811-489f-8a57-813f99177a59.png)
### 当myPointer=X;此时指针以指向x，所以相应打印myPointer出的也是x的地址。

![图片 23](https://user-images.githubusercontent.com/92034503/158805562-bbb7bf89-527f-44e8-9c42-168c5ff0ad9e.png)
### 同样我们也可以通过“指针”得到存储在“内存位置”的数据
### 用解参考运算子（dereference operator）“*”
### cout*myPointer 可打印出赋予变量x的值

![图片 24](https://user-images.githubusercontent.com/92034503/158805648-c9563f68-6f6b-46c8-9098-390b90166df1.png)

### 只要你用pointer分配了一部分内存，一定要记得之后去释放或者删除它。

### 两种方式-上下对应（一一对应 不能换！！）
### malloc—free
### new—delete
![图片 25](https://user-images.githubusercontent.com/92034503/158805806-43ef063e-9227-42db-8efe-26ad8d19e60c.png)
![图片 26](https://user-images.githubusercontent.com/92034503/158805819-59c2d8d9-74ef-49df-9f8b-40d46b5659a6.png)

### 用delete时不要忘记“[]”哦！
![图片 27](https://user-images.githubusercontent.com/92034503/158805940-cd6c56e7-20a4-4e42-8a51-b0e1fba496dc.png)
![图片 28](https://user-images.githubusercontent.com/92034503/158805954-d8f361f1-a968-4bbb-b193-6f505afaaf6b.png)
### 每创建一个new int
### 一定要在最后加一个delete
### （The lecture notes will go into more detail next week）

![图片 29](https://user-images.githubusercontent.com/92034503/158806183-819b96fd-1a00-4a1e-a753-3f700a4954e3.png)
### 这两种方式可以在stack里进行也可以在heap里进行
### stack更稳固
### heap是动态的，当你要创建大量数据：处理/转换/移动它时非常有用
### 比如当你要改变数据的大小，你应该在heap里进行，而不是stack。
![图片 30](https://user-images.githubusercontent.com/92034503/158806341-9fa79724-3927-4ef3-94fc-2d30bb212773.png)
![图片 31](https://user-images.githubusercontent.com/92034503/158806349-5c499a38-c98e-4c74-bb78-f39be6292d3d.png)

