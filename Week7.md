# Week 7

* What is a function?
* What are the benefits of a function?
* How do I define a function?
    * Parameters - What are they? Is there a max/min # of parameters?
    * Return type - What are the return types we can have?
* How do I call a function?
    * Arguments - What are they? How do we determine how many arguments we need?    
* Function scope?
* Defining a function before `main()` vs defining a function after `main()`

#### More About Scope
---
Note: Remember scope! Variables declared within a function cannot be used outside of that function.  
This is also the case for branches, loops, etc. Anything you create within {braces} can only be used within the braces.  
BUT, unlike functions, things like loops, branches, etc. can use variables created outside of it, as long as it resides in the same overall function.  
Global variables can be accessed by everything, as long as it was declared before the function.

ex: 
```c++

void foo1(int num) {
    int z = 3;
    for (int i = 0; i < num; i++) {
        int y = i;
        if (i % 2 == 0) {
            int x = i;
            cout << x << endl;
        }
        cout << x << endl; // this will give error because x was not declared in this scope.
        for (int j = 0; j < num; j++) {
            cout << i << " " << j << endl; // We can use both i and j here because both exist in scope.
        }
    }
    cout << z << innum << endl; // z can be used, b/c in scope. innum will give an error because it was not declared prior to this function, thus it cannot see it.
}

int innum = 10;

int main() {
    cout << z << num << i << x << endl; 
    // This will give an error for every variable because they were not declared in scope; they were all variables declared outside of main
    cout << outnum << innum << endl;
    // This will give an error for outnum, because we have not yet declared the variable yet. innum will work because it was declared at the beginning/before this function
}

int outnum = 1;
```


#### Identify It
---
###### Rules
For each function: 
* Is it a function?
* Identify its functionality
* Identify the return type
* Identify the parameters that exists/should have
* Identify the arguments when calling the function

<br>

1. isupper()
2. tolower()
3. GetName()
4. for()
5. pow()
6. at()
7. CalcAverage()
8. PrintArea()
9. push_back()
10. getline()

#### Function Competition
* [Repl.it](https://repl.it/@PikaSannnnn/Functions#main.cpp)
    * [Solutions w/ Explanations](https://repl.it/@PikaSannnnn/Functions-Solutions#main.cpp)'
        * Press the `Run` button to see the code work. you can also test different inputs by going to the *inputs.txt* file and typing your own inputs
            * first line - number
            * second line - number
            * third line - one word string
