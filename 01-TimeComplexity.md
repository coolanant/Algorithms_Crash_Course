## Time Complexity

```c++
int sum(int n){
    if(n<=0){
        return 0;
    }
    return n+sum(n-1);
}
```
> Time - O(n)<br/>
> Space - O(n)


```c++
for(int a:A){
        ...
}
for(int b:B){
    ...
}
```
> Time - O(A+B)

```c++
for(int a:A){
  for(int b:B){
    ...
  }
}
```
> Time - O(A*B)




