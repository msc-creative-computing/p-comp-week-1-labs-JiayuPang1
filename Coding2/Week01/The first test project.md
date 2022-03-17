
# **Coding 02-Week 01 Notebook**
# **C++ & IDE**
----------
## IDE:iterative development environment

## C++:  
1)  text editor
2)	hinting/linting 提示/检查
3)	preprocessor 预处理器
4)	compiler 编译器
5)	debugging tools 调试工具

· main.cpp 对初学者来说在项目里非常重要，first be reading
· #include
· namespace 命名空间
· print to the console
  e.g. “count” --> standard namespace. 否则 “std”+ “count”
  
![图片 1](https://user-images.githubusercontent.com/92034503/158789731-8af44a45-780d-4b40-8318-5a7c425ca87f.jpg)

· w3c 学校的 C++ 教程:
https ://www.w3schools.com/cpp/


## Xcode

1)
#include <iostream>

int myInt = 0;

float myPI = 3.1415926;   float 后面定义的数值是可以有小数点的 int只能是整数

int main(int argc, const char * argv[ ]) {
   
    std::cout << "Hey everyone";
   
    return 0;
}
![图片 2](https://user-images.githubusercontent.com/92034503/158790675-7c647162-9837-4697-9283-183976720514.jpg)

2)
#include <iostream>

int myInt = 0;

float myPI = 3.1415926;
const char myChar[10] = "Hey there";  const 需要【】里的数值大于输入文字占用的字符数

int main(int argc, const char * argv[ ]) {
   
    std::cout << myChar;
   
    return 0;
}

3)
#include <iostream>

int myInt = 0;

int myPI = 3.1415926;
std::string myString = "Hey there";  string 则 不需要输入文字占用的字符数 


int main(int argc, const char * argv[ ]) {
   
    std::cout << myString; /  std::cout << myString << ""; / std::cout << myString << std::endl;
   
    return 0;
}
![图片 3](https://user-images.githubusercontent.com/92034503/158790813-b31fb9d9-bd28-48ed-8fb2-d1623273b527.jpg)
## endl 文字回车
endl只是一个函数模板。
其主要搭配iostream对象来使用,如cout、cerr等，
其作用是：
1.将换行符写入输出流，其中Unix/Linux换行符是\n，Windows中是\r\n，MAC中是\r；
2.清空输出缓冲区。
在 c++中如何使用输入\输出符endl。
比如在语句 ：
cout<<"the id is"<<endl <<2；
cout<<"the id is"<<i << endl；
那么意思是：
endl就相当于输出的时候回车。
第一句的输出是:
the id is
2
第二句的输出是:
the id is i
然后光标到了第二行。
额外的，还可以这样使用endl：
std::endl(cout); // 等于 std::endl(std::cout);
std::endl(cout << "this id is" << i); // 等于 std::endl(std::cout << "this id is" << i);
（注：这是由于Koenig looup法则）
其中第一句等同于:std::cout << std::endl; // 不能写成std::cout << endl;
第二句等于：std::cout << "this id is" << i << std::endl; // 如上所述
————————————————
##### 版权声明：本文为CSDN博主「luckyone906」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/u011555996/article/details/51168710
_
<img width="407" alt="图片 4" src="https://user-images.githubusercontent.com/92034503/158791278-405eb3f9-d928-4dd5-8bfa-19697ad581f6.png">
4)
#include <iostream>
using namespace std;（开头使用命名空间定义标准，之后就不需“std：： ”
int myInt = 0;

float myPI = 3.1415926;
string myString = "Hey there";

int main(int argc, const char * argv[]) {
   
    cout << myString <<endl;
   
    return 0;
}


5)
加入其他内定方程式：可直接Google搜索
#include <iostream>
#include<math.h>恢复所有三角函数
#include<stdlib.h>
#include<time.h>


using namespace std;
int myInt= 2;

float myPI = 3.14159;
string myString = "Hey there";

int main(int argc, const char * argv[ ]) {
    
    srand((int)time(NULL));
    myInt=rand();
    
    float myOut =sin(myPI)/ round(myPI)四舍五入/ ceil(myPI)数值+1/ sin(myPI/2)2分之一;cos/tan
   
    cout << myOut <<endl;
   
    return 0;
}


6)
#include <iostream>
#include<math.h>
#include<stdlib.h>
#include<time.h>


using namespace std;
int myInt= 2;

float myPI = 3.14159;
string myString = "Hey there";

int main(int argc, const char * argv[]) {
    
    for (int i = 0; i < 11; i++){
        cout << i << endl;
    }
        
    cout << "Dog" <<endl;
    
    return 0;
}
<img width="432" alt="图片 5" src="https://user-images.githubusercontent.com/92034503/158791552-3c8d6acb-173e-42f5-8ea2-d5913265680e.png">
7)
using namespace std;
int myInt= 2;

float myPI = 3.14159;
string myString = "Hey there";
void myFunc(){. //     void 语句 不用return
    cout << "Dog" <<endl;
}

int main(int argc, const char * argv[ ]) {
    
 
    for (int i = 0; i < 11; i++){   i++语句。
        cout << i* myPI << endl;
    }
        
   
    myFunc();
    return 0;
}

## void & int 区别
             ![图片 6](https://user-images.githubusercontent.com/92034503/158791785-af8ec8b9-cdde-42ca-8c1e-53159c829503.png)
         <img width="419" alt="图片 7" src="https://user-images.githubusercontent.com/92034503/158791795-b590ede5-1a0f-4be8-aff0-c39d60cf1f6d.png">

  8)
using namespace std;
int myInt= 2;

float myPI = 3.14159;
string myString = "Hey there";
float myFunc(float x,float y){
    cout << "Dog" <<endl;    ??????????
    
    return x * y;
}

int main(int argc, const char * argv[]) {
    
   
    for (int i = 0; i < 11; i++){
        float yeah =  i* myPI;
        cout << yeah << endl;      ???????
    }
        
    float anotherFloat = myFunc(myInt,myPI);
    cout << anotherFloat << endl;
    return 0;
}

<img width="432" alt="图片 8" src="https://user-images.githubusercontent.com/92034503/158791966-20077d24-8c17-4821-a81b-5e6e0625e37c.png">
9）
objects

add “class”一定要记得在{ }中的“ } ”后加“ ； ”
<img width="226" alt="图片 9" src="https://user-images.githubusercontent.com/92034503/158792023-c3540880-4d28-4eb3-ae9f-8a2c1905ce84.png">
!注意：函数func 与对象object是完全不同的东西，所以我们甚至可以为他们命名相同的名字，因为他们互不影响。

 “babydog has a public variable called c and it contain the following value: 128
!注意：只有objects是public才会被print，如果不在，则不能print因为是private。
<img width="419" alt="图片 10" src="https://user-images.githubusercontent.com/92034503/158792571-325aaeff-76c1-4dce-a46f-759bdb81117f.png">

myClass babydog1; 
myClass babydog2;
.
.
. 
我们可以根据需求无限扩建，并创造出更丰富的算法
float anotherFloat = babydog2.myFunc(2, 2)*babydog1.myFunc(3, 10);
cout << anotherFloat << endl;

头文件和源文件 (.h）& (.c/.cpp)
* declear your object in your head file-.hpp   （declare声明before define）
* define your object in your head file-.cpp
![图片 11](https://user-images.githubusercontent.com/92034503/158792650-c9400e7f-9003-4a85-acc8-2bd0be93bc38.png)
## declear & define
!注意：永远不要在文件中多次使用相同的对象名字

!注意：如果declare里需要用到函数等，就在最上面的
include列里 加上
#include <math.h>   其他同理。
![image](https://user-images.githubusercontent.com/92034503/158792847-107837be-2a91-4219-8c4d-c2136d2ef2af.png)



