```c++
#include <iostream>
using namespace std;

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
