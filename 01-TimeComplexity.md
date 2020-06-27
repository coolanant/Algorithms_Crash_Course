## Time Complexity

1. 
```c++
int sum(int n){
  if(n<=0){
    return 0;
  }
  return n+sum(n-1);
}
```
> Time - O(n)
> Space - O(n)
