# newcoder io exercise

## 1. 计算A+B

+ 输入描述：
  
输入包括两个正整数a, b(1 <= a, b<=10^9) ，输入数据包括多组。

+ 输出描述：
  
输出a+b的结果

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

## 2. 计算A+B

+ 输入描述：

输入第一行包括一个数据组数t(1 <= t <= 100)。
接下来每行包括两个正整数a,b(1 <= a, b <= 10^9)

+ 输出描述：

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

## 3. 计算A+B

+ 输入描述:

输入包括两个正整数a,b(1 <= a, b <= 10^9),输入数据有多组, 如果输入为0 0则结束输入

+ 输出描述:

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

+ 输入描述:

输入数据包括多组。
每组数据一行,每行的第一个整数为整数的个数n(1 <= n <= 100), n为0的时候结束输入。
接下来n个正整数,即需要求和的每个正整数。

+ 输出描述:

每组数据输出求和的结果

```C++
#include <iostream>

int main(){
    int num, a;
    
    while(std::cin>>num){
        if(num==0)
            break;
        int sum = 0;
        while(num){
            std::cin >> a;
            sum += a;
            num--;
        }
            
        std::cout<<sum<<std::endl;
    }
    
    return 0;
```

## 5. 计算一系列数的和

+ 输入描述:

输入的第一行包括一个正整数t(1 <= t <= 100), 表示数据组数。
接下来t行, 每行一组数据。

每行的第一个整数为整数的个数n(1 <= n <= 100)。
接下来n个正整数, 即需要求和的每个正整数。

+ 输出描述:

每组数据输出求和的结果。

```C++
#include <iostream>

int main(){
    int group,n;
    std::cin >> group;
    
    while(group--){
        int num;
        std::cin >> num;
        int sum = 0;
        while(num--){
            std::cin >> n;
            sum += n;
        }
        std::cout << sum << std::endl;
    }
    
    return 0;
}
```

## 6. 计算一系列数的和


+ 输入描述:

输入数据有多组, 每行表示一组输入数据。
每行的第一个整数为整数的个数n(1 <= n <= 100)。
接下来n个正整数, 即需要求和的每个正整数。

+ 输出描述:

每组数据输出求和的结果

```C++
#include <iostream>

int main(){
    int a,num;
    while(std::cin >> num){
        int sum = 0;
        while(num--){
            std::cin >> a;
            sum += a;
        }
        std::cout<< sum << std::endl;
    }
    return 0;
}
```


### 7. 计算一系列数的和

+ 输入描述:

输入数据有多组, 每行表示一组输入数据。
每行不定有n个整数，空格隔开。(1 <= n <= 100)。

+ 输出描述:

每组数据输出求和的结果

```C++
#include <iostream>

int main(){
    int t;
    int sum=0;
    while(std::cin >> t){
         sum += t;
        if(std::cin.get()=='\n'){
             
            std::cout << sum << std::endl;
            sum = 0;
        }
         
    }
    return 0;
}

``` 

### 8. 字符串排序输出

+ 输入描述:

输入有两行，第一行n。
第二行是n个空格隔开的字符串

+ 输出描述:

输出一行排序后的字符串，空格隔开，无结尾空格

```C++
#include <iostream>
#include <vector>
#include<string>
#include<algorithm>

int main(){
    int num;
    std::cin >> num;
    std::string str;
    std::vector<std::string> bucket;
    
    while(num--){
        std::cin >> str;
        bucket.push_back(str);
    }
    
    sort(bucket.begin(), bucket.end());
    
    for(int i = 0; i< bucket.size(); i++){
        if(i==0){
            std::cout<<bucket[0];
        }
        else
            std::cout<<' '<<bucket[i];
    }
    
    return 0;
}
```

### 9. 字符串排序输出

+ 输入描述:

多个测试用例，每个测试用例一行。

每行通过空格隔开，有n个字符，n＜100

+ 输出描述:

对于每组测试用例，输出一行排序过的字符串，每个字符串通过空格隔开

```C++
#include <iostream>
#include <set>
#include <string>

int main(){
    std::set<std::string> line;
    std::string str;
    
    while (std::cin >> str) {
        line.insert(str);
        if (std::cin.get() == '\n') {
            for (auto iter = line.begin(); iter != line.end(); ++iter) {
                std::cout << *iter << " ";
            }
            std::cout << std::endl;
            line.clear();
        }
    }
    
    return 0;
}
```

### 10. 字符串排序输出

+ 输入描述:

多个测试用例，每个测试用例一行。
每行通过','隔开，有n个字符，n＜100

+ 输出描述:

对于每组用例输出一行排序后的字符串，用','隔开，无结尾空格

```C++
#include<bits/stdc++.h>

int main(){
    std::vector<std::string> res;
    std::string a,b;
    while(getline(std::cin,a)){
        std::stringstream x(a);
        while(getline(x,b,','))
            res.push_back(b);
        sort(res.begin(),res.end());
        for(int i=0;i<res.size()-1;++i)
            std::cout<<res[i]<<',';
        std::cout<<res.back()<<std::endl;
        res.clear();
    }
}
```