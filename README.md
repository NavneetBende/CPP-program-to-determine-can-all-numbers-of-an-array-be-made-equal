Check if all the numbers of array can be made equal in C+++
Here we will discuss the program to Check if all the numbers of array can be made equal in C++.

We need to check if all the numbers of an array can be  made equal to a particular number. In a single operation, any element of the array can be either multiplied by 2 or by 3. If it’s possible to make all the array elements equal with the given operation then print Yes else print No.

Can all number of an array be made equalin C++
While loop in C
Example
Input: n=3   arr[] =[50, 75, 100]
Output: Yes
Explanation : [50 * 2 * 3, 75 * 2 * 2, 100 * 3] = [300, 300, 300]
Algorithm
Start iterating over the array.
Run a loop till arr[i]%2=0, and inside that loop divide the arr[i] by 2.
Run a loop till arr[i]%3=0, and inside that loop divide the arr[i] by 3.
Check if arr[i] != arr[0], then return 0.
Otherwise, return 1.
Related Pages
Finding Arrays are disjoint or not

Determine Array is a subset of another array or not

Finding Minimum sum of absolute difference of given array

Sort an array according to the order defined by another array 

Replace each element of the array by its rank in the array

Code in C++
//Write a program to check can all number of an array be made equal in C++

#include <bits/stdc++.h>
using namespace std;

int EqualNumbers(int arr[], int n)
{
    for (int i = 0; i < n; i++) {
 
        // Divide number by 2
        while (arr[i] % 2 == 0)
            arr[i] /= 2;
 
        // Divide number by 3
        while (arr[i] % 3 == 0)
            arr[i] /= 3;
 
        if (arr[i] != arr[0]) {
            return 0;
        }
    }
 
    return 1;
}
 
// Driver code
int main()
{
    int arr[] = { 50, 75, 100 };
 
    int n = sizeof(arr) / sizeof(arr[0]);
 
    if (EqualNumbers(arr, n))
        cout<<"Yes";
    else
        cout<<"No";
 
    return 0;
}
Output :
Yes
