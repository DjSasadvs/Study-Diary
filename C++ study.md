08-10-2016
----------------
实现一个 malloc
* [跳转链接](http://blog.codinglabs.org/articles/a-malloc-tutorial.html)

08-09-2016
----------------
内存泄漏和野指针
* 内存分配后应进行回收
 * vector<T>:
 ```
  vector<T> v;
  for(int i = 0; i < 10000; i++)
  {
     v.clear(); vector<T>(v).swap(v);
  }
 ```
* 野指针需要置为空指针
```
char *memory = (char *)malloc(1024);
memset(memory, 0, 1024);
memset(memory, 0, 1024 - 1);
free(memory); memory = NULL;
```

03-01-2016
----------------
类型升级
* unsigned int是最大的了，所以类型无法提升，而unsigned short型，如果出现上面那种情况，就会向容量更大类型提升，即提升为int
```
#include <iostream>
using namespace std;
 
int main(int argc, char* argv[])
{
    unsigned short us1 = 2, us2 = 3;
    cout << (us1 - us2) << endl;                        // 输出 -1
    cout << typeid((us1 - us2)).name() << endl;        // 类型提升为int
    int i1 = ((us1 - us2) > 0);
    cout << i1 << endl;
 
    unsigned int ui1 = 2, ui2 = 3;
    cout << (ui1 - ui2) << endl;                        // 输出一个很大的int
    cout << typeid((ui1 - ui2)).name() << endl;        // 类型仍然是unsigned int
    int i2 = ((ui1 - ui2) > 0);
    cout << i2 << endl;
    return 0;
}
```

10-24-2015
-----------------
```
#include <stdlib.h>
atoi(char *str)
#include<math.h>
double pow(double,double);
```

11-20-2015
----------------
c++ map的使用
```
1 iter = m.find(key);
2 if(iter!=m.end())
3 {
4     return iter->second;
5 }
6 return null;
```
11-23-2015
-------------

1.计算char *str的长度，strlen(str)
<br>
2.char *str类型
```
3.
#include<vector>;  
vector<int> restlt; 
result.push_back(int x); 
result.size(); 
result[i];   
reverse(stk.begin(),stk.end());//反转
4.
#include<stack>;   
stack<int> tree;  
tree.push(int a); 
tree.empty();  
tree.pop();
```
12-16-2015
-------------------

1.resize和reserve<br/>

capacity
  * 指容器在分配新的存储空间之前能存储的元素总数
size
  * 指当前容器所存储的元素个数

2.resize和reserve的区别<br/>
  * reserve表示容器预留空间，但并不是真正的创建对象，需要通过insert（）或push_back（）等创建对象;resize既分配了空间，也创建了对象<br/>
  * reserve只修改capacity大小，不修改size大小;resize既修改capacity大小，也修改size大小

12-21-2015
--------------------------
1.assert()断言

 ```
 void assert(   
   int expression   
);  
```
2.重载
 * c++中规定，重载运算符必须和用户定义的自定义类型的对象一起使用。
