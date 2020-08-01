# newcoder io exercise

## 1. 计算A+B

输入描述：输入包括两个正整数a, b(1 <= a, b<=10^9) ，输入数据包括多组。

输出描述：输出a+b的结果

```C++
#include <iostream>

int main(){
    int a, b;
    
    while(std::cin >> a >> b){
        std::cout<<a+b<<std::endl;
    }
    
    return 0;
}
```