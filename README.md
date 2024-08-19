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
## CONCLUSION-
learnt basics of pointers
