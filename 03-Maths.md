```c++
#include <iostream>
using namespace std;

// 2. GCD
//O(log(a+b))
int gcd(int a,int b){
     return b==0? a : gcd(b,a%b);
}
//O(a+b)
int gcd2(int a, int b){
    if(a==b){
        return a;
    }
    if(a>b){
        return gcd(a-b,b);
    }
    else{
        return gcd(a,b-a);
    }
}

int main() {
    // 1. Birthday Paradox
    float prob=1;
    int people=0;
    float num=365;
    while(prob>0.5){
        prob*=(num/365);
        num--;
        people++;
    }
    cout<<people;
}
```
