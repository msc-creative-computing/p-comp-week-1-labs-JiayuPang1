## Notebook
# Coding02-Week06
# Build a simple webscraper

## .html ( hypertext markup language) 超文本标记语言
这样的文件往往是纯文本的，但是被浏览器解析或者说是“渲染”后，形成了有图标有文字，有颜色的网页。


html 有很多标记模式 这些标记其实就是网页显示内容的属性
比如

<img width="255" alt="图片 57" src="https://user-images.githubusercontent.com/92034503/158820140-824b4bff-d6c2-45cd-88d2-db90cce92b50.png">

HTML链接是通过<a>标签进行定义的：
<a href=“ ...”> 
href abbr. 超文本引用（hypertext reference）；超链接
e.g. 
<a href= “一个网址链接”> this is a link</a>

HTML图像是通过<img>标签进行定义的：
e.g.
<img src=“本地或网图都可” width= “200” alt=“图像不存在”/>
 width图片宽度200

<img width="432" alt="图片 58" src="https://user-images.githubusercontent.com/92034503/158820251-3cfa061c-80d6-41a5-be43-763f6f95f5f3.png">
 
如何查看网页源代码：
单击右键+“查看源代码”
单击右键+“检查”！推荐 结构更清晰
 
![图片 59](https://user-images.githubusercontent.com/92034503/158820336-5cc97bd2-e42f-44a5-8631-8229f580e922.png)

## Requests
  
python中原生的一款基于网络请求的模块，功能强大，简单高效
作用：模拟浏览器发送请求

如何使用：（编码流程）
  - 指定url（网址）
  - 发起请求
  - 获取响应数据
  - 持久化存储

import requests
url = https://
response= requests.get(url=url)
#step 3:获取响应数据.text返回的是字符串形式的响应数据
page_ response.text
print(page_text)


解析数据-聚焦爬虫

聚焦爬虫：爬取页面中指定的页面内容

如何使用：（编码流程）
  - 指定url（网址）
  - 发起请求
  - 获取响应数据
  - 数据解析
  - 持久化存储
  

数据解析原理概括：
  - 解析的局部的文本内容都会在1.标签之间           进行存储
                          2.标签对应的属性中
  
  ![图片 60](https://user-images.githubusercontent.com/92034503/158820771-b957e722-4076-42a5-a367-78d0c1c58dda.png)
 
 - 进行指定标签的定位
  - 标签或标签对应的属性中存储的数据进行提取（解析）
                                                               
## ·bs4进行数据解析

原理：
  - 1.实例化一个BeautifulSoup对象，并且将页面源码数据加载到该对象中
  - 2.通过调用BeautifulSoup对象中相关的属性或者方法进行标签定位和数据提取

如何实例化一个BeautifulSoup对象：
  - from bs4 import BeautifulSoup
  - 对象的实例化：
- 1.将本地的html文档中的数据加载到该对象中
    fp = open (‘./命名 ’, ‘r’, encoding = ‘utf-8’)
    soup = BeautifulSoup (fp, ‘lxml’)
- 2.将互联网上获取的页面源码加载到该对象中
    page_text = response.text
    soup = BeautifulSoup(page_text, ‘lxml’)
- soup.tagName:返回的是文档中第一次出现的tagName对应的标签
- soup.find():
       - find(“tagName”) = soup.tagName
       - 属性定位：
             - soup.find(“div”,class_/id/attr…= “…”
- soup.find_all(“tagName”):返回符合要求的所有标签（list）
- slect("某种选择器（id，class，标签...选择器)"),返回的是一个列表。
       2.层级选择器：
                 1.soup.select(".tang > ul > li > a "):   " >"表示一个层级
                 2.soup.select(".tang > ul a "):   "空格"表示多个层级
- 获取标签之间的文本数据：
       - soup.a.text/string/get_text()
       - text/get_text():可以获取某一个标签中所有的文本内容
       - string：只可以获取该标签下的直系的文本内容
