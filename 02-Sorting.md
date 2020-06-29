```c++
#include<iostream>
#include<algorithm>

using namespace std;

void bubblesort(int arr[],int n){
    for(int i=0;i<n-1;i++){
        for(int j=0;j<n-i-1;j++){
            if(arr[j]>arr[j+1]){
                swap(arr[j],arr[j+1]);
            }
        }
    }
}

void selectionsort(int arr[],int n){
    int pos;
    int small;
    for(int i=0;i<n-1;i++){
        pos=i;
        small=arr[i];
        for(int j=i+1;j<n;j++){
            if(arr[j]<small){
                small=arr[j];
                pos=j;
            }
        }
        swap(arr[i],arr[pos]);
    }
}


void insertionsort(int arr[],int n){
    int temp;
    int j;
    for(int i=1;i<n;i++){
        j=i-1;
        temp=arr[i];
        while(j>=0 && temp<arr[j]){
            swap(arr[j],arr[j+1]);
            j--;
        }
        swap(temp,arr[j+1]);
    }
}


int main() {
    int arr[]={6,9,1,0,5,3,4,2,0,8,7};
    int size=sizeof(arr)/sizeof(arr[0]);
    
    //1.
    //sort(arr,arr+size);
    
    //bubblesort(arr,size);
    
    //insertionsort(arr,size); 
    
    //selectionsort(arr,size);
    
    
    //2.
    // mergesort(arr,n);
    
    // quicksort(arr,n);
    
    // heapsort(arr,n);
    
    //3.
    
    
    for(int i=0;i<sizeof(arr)/sizeof(arr[0]);i++){
        cout<<arr[i];
    }
}
```
