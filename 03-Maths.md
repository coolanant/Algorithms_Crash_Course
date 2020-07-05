```c++
#include <iostream>
using namespace std;

// 2. GCD - Euclid's Algo
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
        return gcd2(a-b,b);
    }
    else{
        return gcd2(a,b-a);
    }
}

// 3. IsPrime
int isPrime(int n){
       for(int i=2;i*i<n;i++){
        if(n%i==0){
            return -1;
        }
    }
    return 1;
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
