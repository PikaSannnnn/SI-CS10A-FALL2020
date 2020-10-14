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
   What is a syntax error?
   
   What is a logic error?
   
   What's the difference between a compile error and a runtime error?
   
   What is a warning?
   
   <br>
   
Identify the errors.  
1.
  ```c++
     string name = "Justin";
     int age;
     cout << "My name is " << age << endl;
  ```



2.
  ```c++
     int count = 300
     cout << "I have " << count << " cakes" << endl;
  ```



3.
  ```c++
     int years = 1;
     cout << "There  is " << year << " year within a year" << endl;
  ```
  
  
  
4.
  ```c++
     int sum;
     sum = 3 * 10;
     cout << "3 + 10 = " << sum << endl;
  ```



5.
  ```c++
     #include <iostream>
     
     usin namespace std;
     
     int main() {
        int numErrors;
        cin >> numErrors
        
        cout << "Enter the number of errors within this code: ";
     
  ```
  
  
  
6.
  ```c++
     #include <iostream>
     
     usin namespace std;
     
     int main() {
        cout << "I am pretty sure there's nothing wrong with this set of code. 
           I believe there's no errors here and that you should believe me when I 
           say so;" cout << "KeepInMindThatBadWhiteSpacingDoesNotGiveYou
           AnErrorOrWarning,ButItWillAnnoyPeople" endl;
     }
  ```



7.
   ```c++
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



8.
   ```c++
      #include <iostream>

      using namespace;

      int main() {
         const int divisor = 30;

         int sampleExpr = 3.0 % divisor;
         cout << sampleExpr;
         return 0;
      }
   ```

9. Fix this code given this error
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


