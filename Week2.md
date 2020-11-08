# Week 2

Comments examples:
   ```c++
      // Here we have a simple "Hello World" output
      cout << "Hello World" << endl;
   ```
   ```c++
      /*
         The code written
         will print out "Hi"
      */
      cout << "Hi" << endl;
   ```
   ```c++
      /* These lines of code are commented out
         for testing purposes
      */
      // cout << "Hello ";
      // cout << "World";
   ```
   
   
   
Warnings and Errors:  
   * What is a syntax error?  
      Syntax error is any error within the code that may infringe on the rules of the programming language. This includes maybe missing a semicolon, or mispelling a function, or using a variable that does not exist yet. This will prevent the code from running until it is fixed.
   * What is a logic error?  
      Logic error, or a bug, is an error that occurs while the code is running where something doesn't mwatch what you had expected. This often does not cause the program to crash, but it does not mean it's not possible.  
   * What's the difference between a compile error and a runtime error?  
      Runtime error is any error that occurs while the program is running and can sometimes lead to the program to crash. This includes any bugs, logic errors, etc. Compile errors are any errors that occur before or while compiling the code and will always prevent the code from running. This can include syntax errors, etc.  
   * What is a warning?  
      A warninig is anytime there is a problem with either the code while writing it that won't stop the code from running (unless specified), but will be there to say that something can't be done, but is allowed. Although warnings don't cause the program to stop, they can sometimes warn you about potential logic or runtime errors that may or may not cause the program to crash. Additionally, sometimes warnings can develop into errors.  

   <br>
   
Identify the errors.  
1. ```c++
     string name = "Justin";
     int age;
     cout << "My name is " << age << endl;
  ```
<details>
    <summary>Ans</summary>

Logic/Runtime error: age is used instead of age; age has not been set (garbage value)
</details>

2. ```c++
     int count = 300
     cout << "I have " << count << " cakes" << endl;
  ```
<details>
    <summary>Ans</summary>

Syntax/Compile error: `ing count = 300` is missing a semicolon
</details>

3. ```c++
     int years = 1;
     cout << "There  is " << year << " year within a year" << endl;
  ```
<details>
    <summary>Ans</summary>

Syntax/Compile error: the cout uses `year`, but it is not a variable. It should use `years` instead
</details>
  
4. ```c++
     int sum;
     sum = 3 * 10;
     cout << "3 + 10 = " << sum << endl;
  ```
<details>
    <summary>Ans</summary>

Logic/Runtime error: `sum` is computing the product of 3 and 10 rather than adding
</details>

5. ```c++
     #include <iostream>
     
     usin namespace std;
     
     int main() {
        int numErrors;
        cin >> numErrors
        
        cout << "Enter the number of errors within this code: ";
     
  ```
<details>
    <summary>Ans</summary>

Syntax/Compile error: `using` is mispelled; missing semicolon after `cin >> numErrors`
Logic/Runtime error: input is asked before the prompt
</details>
  
6. ```c++
     #include <iostream>
     
     usin namespace std;
     
     int main() {
        cout << "I am pretty sure there's nothing wrong with this set of code. 
           I believe there's no errors here and that you should believe me when I 
           say so;" cout << "KeepInMindThatBadWhiteSpacingDoesNotGiveYou
           AnErrorOrWarning,ButItWillAnnoyPeople" endl;
     }
  ```
<details>
    <summary>Ans</summary>

Syntax/Compiler error: Missing semicolon before `cout <<`; Missing `<<` before `endl`
</details>

7. ```c++
      #include <iostream>
      
      using namespace std;

      int main() {
         const int pi = 3.14;
         const int radius;

         cin >> radius;
         cout << "Area of a circle: " << pi * pow(radius,2) << endl;

         return 1;
      } 
   ```
<details>
    <summary>Ans</summary>

Compiler error: Attempting to write into (`cin`) into a constant
</details>

8. ```c++
      #include <iostream>

      using namespace;

      int main() {
         const int divisor = 30;

         int sampleExpr = 3.0 % divisor;
         cout << sampleExpr;
         return 0;
      }
   ```
<details>
    <summary>Ans</summary>

Syntax/Compiler error: missing the `std` in `using namespace`; `%` cannot be used with a decimal
</details>

9. Fix the code given this error
 ```
    main.cpp:6:45: error: expected ';' after expression
    cout << "Today was my first SI Session!"
                                            ^
                                            ;
 ```


 ```c++
      #include <iostream>
      
      using namespace std;
      
      int main() {
         cout << "Today was my first SI Session!"
      }
 ```
<details>
    <summary>Ans</summary>

```c++
   cout << "Today was my first SI Session!";
```
</details>

10. Fix this code given this error
 ```
   main.cpp: In function ‘int main()’:
    main.cpp:8:3: error: expected ‘,’ or ‘;’ before ‘cout’
    cout << nums << endl;
    ^~~~
 ```
   
   
 ```c++
      #include <iostream>
      
      using namespace std;
      
      int main() {
         int nums = 0
         
         cout << nums << endl;
      }
 ```
<details>
    <summary>Ans</summary>

```c++
int nums = 0;
```
</details>

 11. Fix this code given this error
  ```
   main.cpp: In function ‘int main()’:
   main.cpp:13:5: error: ‘cout’ was not declared in this scope
      cout << num2 * num3 << endl;
      ^~~~
   main.cpp:13:5: note: suggested alternative:
   In file included from main.cpp:1:0:
   /usr/include/c++/7/iostream:61:18: note:   ‘std::cout’
      extern ostream cout;  /// Linked to standard output
                     ^~~~
   main.cpp:13:28: error: ‘endl’ was not declared in this scope
      cout << num2 * num3 << endl;
                              ^~~~
   main.cpp:13:28: note: suggested alternative:
   In file included from /usr/include/c++/7/iostream:39:0,
                  from main.cpp:1:
   /usr/include/c++/7/ostream:590:5: note:   ‘std::endl’
      endl(basic_ostream<_CharT, _Traits>& __os)
      ^~~~
  ```

  ```c++
      #include <iostream>

      int main()
      {
         int num1;
         int num2 = 0;
         int num3 = 0;
         int numValues = 0;
         int threeProds;
         
         cout << num2 * num3 << endl;
         numValues += 2;
         cout >> num1;
         threeProds *= num1;
         numValues++;
         
         cout << "Product of num1, num2, num3: " << numValues << endl;
         

         return 0;
      }

  ```
<details>
    <summary>Ans</summary>

Add `using namespace std;`
</details>


Variables:  
What is a variable?  

Determine wether the following variables are valid.

 ```c++
   int nums;
   int 1;
   int var1;
   int _var1_;
   int char;
   int enum;
   char int one;
   const = 3;
   3 = int three;
 ```

What is division?  

What is modulo?  

Precedence Order  
   1. parentheses  
   2. unary  
   3. mult/div/mod  
   4. add/sub  
   5. left-right  


Precedence Practice:  
1. 10 + 30/10*2  
2. (10 + -30)/20*2  
3. (6 + 2 * 3)% 2  
4. ((6 + 3 + pow(2,3)) - (10 + 3 * 1 / 6)) / 100


* [Informal Quiz](https://docs.google.com/document/d/19HImOku2Z7rVlenNCCq_r4nv7TY5werul_3h5XbGBBM/edit)
   - [Answers](https://docs.google.com/document/d/1Aj6isTXl9RggrgKhexCUQLxFDJKyHWdJJaFKMgFtsNY/edit?usp=sharing)