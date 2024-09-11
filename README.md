# EXPERIMENT 15
# AIM
To study and implement recursion
# THEORY
A function can call itself to fix smaller instances of the same problem, which is a powerful programming technique known as recursion. Recursion is a technique used in C++ when an issue can be divided into smaller, more manageable subproblems of the same kind that can all be resolved with the same function. <BR>

1. Key Components of Recursion
* Base Case: The condition needed for ending the recurrence. The function would call itself endlessly in the absence of a base case, resulting in infinite recursion. <BR>
* Recursive Case: the part of the function where it calls within itself to address a more manageable issue. <BR>

2. How Recursion Works  <BR>
When a recursive function is called, the following happens: <BR>
* In the point where it executes the recursive call, the function pauses. <BR>
* It makes a new call to the same function but with different (usually smaller) arguments. <BR>
* Every paused call takes resume where it left off when the base case is satisfied, and the function provides a result. <BR>

# CODE & OUTPUT

1. CODE A:
```
//SARA KANYAL
//23070123115
// Factorial 
# include <iostream>
using namespace std;
// Creating a function
int fact (int n){
    if (n<=1){
        // Terminating statement (base condition)
        return 1;
    }
    else {
        return (n*fact(n-1));    // Recursion
    }
}
int main (){
    int X,n;
    cout<< "Enter number : ";
    cin>>n;
    X= fact(n);      // Function calling
    cout<<n<<"!="<<X;
    return 0;
}
```
* OUTPUT A :
![EXP15A](https://github.com/sarakanyal03/CDS_Experiment15/blob/main/15A.png)

2. CODE B:
```
//SARA KANYAL
//23070123115
// Sum of integers
# include <iostream>
using namespace std;
// Creating a function
int add (int n){
    if (n<=1){
        // Terminating statement (base condition)
        return 1;
    }
    else {
        return (n+add(n-1));    // Recursion
    }
}
int main (){
    int X,n;
    cout<< "Enter number : ";
    cin>>n;
    X= add(n);      // Function calling
    cout<<X;
    return 0;
}
```
* OUTPUT B :
![EXP15B](https://github.com/sarakanyal03/CDS_Experiment15/blob/main/15B.png)

3. CODE C:
```
//SARA KANYAL
//23070123115
// Reversing a String
# include <iostream>
#include <string.h>
using namespace std;
// Creating function
void reverse(char *str){
    if (*str)                      //Base codition
    {
        reverse(str+1);            //Recursion
        cout<<("%c",*str);

    }
}
int main (){
    char a[50];
    cout<<" Enter a string : ";
    cin>>a;
    reverse(a);                   // Function calling
    return 0 ;
}
```
* OUTPUT C :
![EXP15C](https://github.com/sarakanyal03/CDS_Experiment15/blob/main/15C.png)

4. CODE D:
```
//SARA KANYAL
//23070123115
// Reversing an integer
# include <iostream>
using namespace std;
// Creating function
void print_reverse(int i){
    if (i>0)                      //Base codition
    {         
        cout<<(i%10);
        print_reverse(i/10);     //Recursion

    }
}
int main (){
    int i;
    cout<<" Enter the number : ";
    cin>>i;
    print_reverse(i);                   // Function calling
    return 0 ;
}
```
* OUTPUT D:
![EXP15D](https://github.com/sarakanyal03/CDS_Experiment15/blob/main/15D.png)

# CONCLUSION
