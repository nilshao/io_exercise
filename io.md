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

## 2. 计算a+b

输入描述：

输入第一行包括一个数据组数t(1 <= t <= 100)

接下来每行包括两个正整数a,b(1 <= a, b <= 10^9)

输出描述：

输出a+b的结果

```C++
#include <iostream>

int main(){
    int a,b,total;
    std::cin >> total;
    while(std::cin >> a >> b){
        std::cout<<a+b<<std::endl;
    }
    return 0;
}
```

## 3. 计算a+b

输入描述:

输入包括两个正整数a,b(1 <= a, b <= 10^9),输入数据有多组, 如果输入为0 0则结束输入

输出描述:

输出a+b的结果

```C++
#include <iostream>

int main(){
    int a,b;
    while(std::cin >> a >> b){
        if(a || b)
            std::cout<<a+b<<std::endl;
        else 
            break;
    }
    return 0;
}
```

## 4.计算一系列数的和

输入描述:

输入数据包括多组。

每组数据一行,每行的第一个整数为整数的个数n(1 <= n <= 100), n为0的时候结束输入。

接下来n个正整数,即需要求和的每个正整数。

输出描述:

每组数据输出求和的结果

```C++
#include <iostream>

int main(){
    int num, sum=0,a;
    
    while(std::cin>>num){
        if(num==0)
            break;
        sum = 0;
        while(num){
            std::cin >> a;
            sum += a;
            num--;
        }
            
        std::cout<<sum<<std::endl;
    }
    
    return 0;
```