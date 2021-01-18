
## C++ Internship paper 2
##Table of contents
*Question 1
*Question 2

## Question 1
1. Write a program to print all the LEADERS in the array. An element is leader if it is greater than all the elements to its right side. And the rightmost element is always a leader. 
For example int the array {16, 17, 4, 3, 5, 2}, leaders are 17, 5 and 2.

## Approach
So,the approach is to use a stack and loop from right of the array and push the right most element into stack(as it is leader).Now go to next element and compare it with top element of stack if it is greater than the top element push it in stack else continue.
<pre>
<b>Time complexity: Same as stack operations  ie.., O(n)</b>
</pre>
Below is the implementation of above approach
```c++
#include<bits/stdc++.h>
using namespace std;
int main(){
    //take input
    int n; //no of elements
    cin>>n;
    int arr[n];
    for(int i=0;i<n;i++)cin>>arr[i];
    stack<int>s;
    for(int i=n-1;i>=0;i--){ //looping from backwards
        if(s.empty())s.push(arr[i]);
        else if(arr[i]>s.top())s.push(arr[i]);
        else continue;
        }
    while(!s.empty()){   //loop till stack size is not 0
        cout<<s.top()<<" ";
        s.pop();
        }
    return 0;
 }
 ```
 ## Question 2:
 2. Program to print following pattern:

Input:- 5

Output:- 
```
*                  *
* *              * *
* * *          * * *
* * * *      * * * *
* * * * *  * * * * *
* * * * *  * * * * *
* * * *      * * * *
* * *          * * *
* *              * *
*                  *
```
##Code:
```c++
#include<bits/stdc++.h>
using namespace std;
int main(){
    int n;
    cin>>n;
    int l,r,space;
    //printing left half
    for(l=n;l>0;l--){
        for(r=n;r>=l;r--){
             cout<<"*";}
        space=l*2-2;
        while(space>=0){
            cout<<" ";
            space--;
        }
        for(r=l;r<=n;r++){
          cout<<"*";
          }
         cout<<endl;
    }
    //printing middle line 
    for(l=n;l>=0;l--){
        cout<<"*";}
    for(l=1;l<n;l++){
        cout<<"*";
        }
    cout<<endl;
    //printing right half
    for(l=1;l<n;l++){
        for(r=n;r>=l;r--){
             cout<<"*";}
        space=l*2-2;
        while(space>=0){
            cout<<" ";
            space--;
        }
        for(r=l;r<=n;r++){
          cout<<"*";
          }
         cout<<endl;
    }
    return 0;
    }
    ```
    
    
     
