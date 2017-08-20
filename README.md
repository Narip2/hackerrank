# hackerrank
两个知识点：输出的格式问题和cin在读取字符串的时候不是很方便的问题。  
首先是第一知识点。  
#include<iostream>  
using namespace;  
int main{  
double a=4.0;  
double b=3.0;  
cout<<a+b;  
}  
最后的输出结果是7而不是7.0，即使是这样：  
cout<<(double)(a+b);  
也不对。  
应该这样。  
cout<<setiosflags(ios::fixed)<<setprecision(1)<<a+b;  
才行，而且这样子的话应该在最前面多一个声明：  
#include<iomanip>  
第二个是应该用getline(cin,变量名)解决。但是getline(cin,变量名)会单独读进去一个回车键，所以应该有两个。  
#include<iostream>  
using namespace;  
int mian{  
int a;  
string b;  
string c;  
cin>>a;  
getline(cin,b);  
getline(cin,c);  
}  
就像上面一样，c才有真的东西，b里面只是读入了一个回车。
