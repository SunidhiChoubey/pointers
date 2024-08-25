# Experiment 9 
## Aim: -To study and implement C++ Pointer basics
To learn about pointers, how to implemnent pointers for different data types, how to make and print an array using pointers.
## Theory:-
Pointers are symbolic representations of addresses. They enable programs to simulate call-by-reference as well as to create and manipulate dynamic data structures. Iterating over elements in arrays or other data structures is one of the main use of pointers. The address of the variable you’re working with is assigned to the pointer variable that points to the same data type (such as an int or string).

Advantages of pointers
Dynamic memory allocation
Return multiple values from a function
Alter original data
Passing data between functions efficently
Optimzing data memory
Efficient data structures
Enables call by reference
Disadvantages of pointers
Pointers are a bit difficult to understand.
Pointers can cause several errors, such as segmentation errors or unrequired memory access.
If a pointer has an incorrect value, it may corrupt the memory.
Pointers may also cause memory leakage.
Applications of pointers
to allocate new objects on the heap,
to pass functions to other functions
to iterate over elements in arrays or other data structures.
Code: -
~~~

#include <iostream>
using namespace std;

int main()
{
    int a = 10;
    int *aptr = &a;
    cout<<"dereferencing the pointer of a: "<<*aptr<<endl;
    *aptr = 20;
    cout<<"updating value using pointer: "<<a<<endl;

    float f = 100.009;
    float *fptr = &f;
    cout<<"value off f"<<f<<endl;
    cout<<"pointer of f"<<fptr<<endl;
    cout<<"dereferencing f "<<*fptr<<endl;
    cout<<"referencing f"<<&f<<endl;

    char ch = 'c';
    char *chptr = &ch;
    cout<<"character: "<<ch<<endl;
    cout<<"pointer of character"<<chptr<<endl;
    cout<<"referncing character: "<<&ch<<endl;
    cout<<"dereferencing"<<*chptr<<endl;

    int arr[] = {5,90,30};
    int *arr_ptr = &arr[3];
    cout<<arr_ptr<<endl;
    cout<<"printing an array by dereferencing its pointers: "<<endl;
    for(int i = 0;i<3;i++)
    {
        cout<<(*(arr+i))<<endl; // printing the array using pointers 
    }

    cout<< "Creating an arrray using pointers: "<<endl;
    int *p = new int[5];
    for(int i = 0;i<5;i++)
    {
        p[i] = 10*(i+1);
    }
    // printing the values 
    cout<< *p<<endl;
    cout<< *p+1<<endl;
    cout<< *(p+1)<<endl;
    cout<<2[p]<<endl;
    cout<<p[2]<<endl;
    *p++;
    cout<<*p;

    return 0;
}
~~~
## OUTPUT-
![](https://github.com/SunidhiChoubey/pointers/commit/7db144e2418295179099ec9dbc59db687dfaeb58)
## CONCLUSION-
Learnt basics of pointers

#EXPERIMENT-10
## AIM-To study and implement Pointer Operations (call by value and call by reference)

## Theory:
Call by Value:
What It Does: Passes a copy of the variable’s value to the function.
Effect: Changes made inside the function do not affect the original variable.
Usage: Safe for cases where you don't want the original data to be altered.
Call by Reference:
What It Does: Passes the reference (or address) of the variable to the function.
Effect: Changes made inside the function directly affect the original variable.
Usage: Useful when you need to modify the original data or when working with large data structures to avoid copying.
There are two ways to call a variable to a function for various operations.
Difference
|Call by Value | Call by Reference| |
|----------|----------|----------|
| A method of passing arguments to a function where the actual value is passed |A method of passing arguments where the address of the variable is passed is called call by reference | 
|Does not affect the original variable | Does affect the original variable| 
| More memory is used because a copy of the actual value is made | Less memory is used because only the address is passed. | 
 |Used when the function does not need to modify the original data. | Used when the function needs to modify the original data or when passing large objects. |
## Code:
~~~

a.

#include <iostream>
using namespace std;

//call by value
int a,b;
void swap (int a, int b)
{
    int sw;
    sw = a;
    a = b;
    b = sw;
    cout<<"Swapped Values: "<<endl;
    cout<<"a: "<<a<<endl;
    cout<<"b: "<<b<<endl;
}

int main()
{
    int a,b;
    cout<<"Using call by value: "<<endl;
    cout<<"Enter a number: ";
    cin>>a;
    cout<<"Enter another number: ";
    cin>>b;
    cout<<"User Values: "<<endl;
    cout<<"a: "<<a<<endl;
    cout<<"b: "<<b<<endl;
    swap(a,b);
    
}
~~~
B.
~~~
#include <iostream>
using namespace std;

//call by value
int a,b;
int *pa, *pb;
void swapr (int *pa, int *pb)
{
    int *psw;
    int sw;
    psw = &sw;
    *psw = *pa;
    *pa = *pb;
    *pb = *psw;
    cout<<"Swapped Values: "<<endl;
    cout<<"a: "<<*pa<<endl;
    cout<<"b: "<<*pb<<endl;
}

int main()
{
    int a,b;
    int *pa, *pb;
    cout<<"Using call by value: "<<endl;
    cout<<"Enter a number: ";
    cin>>a;
    pa = &a;
    cout<<"Enter another number: ";
    cin>>b;
    pb = &b;
    cout<<"User Values: "<<endl;
    cout<<"a: "<<a<<endl;
    cout<<"b: "<<b<<endl;
    swapr(pa,pb);
    
}
~~~

Outputs:
![](https://github.com/SunidhiChoubey/pointers/blob/main/Screenshot%202024-08-26%20013326.png)
![](https://github.com/SunidhiChoubey/pointers/blob/main/Screenshot%202024-08-26%20013413.png)



Conclusion:
→ We learnt about call by value and call by reference in C++.
→ We learnt the use case of each in C++.


