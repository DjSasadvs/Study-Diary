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
