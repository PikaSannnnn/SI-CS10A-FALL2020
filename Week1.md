# Week 1 #

Input and Output

What is the output?
1.
  ```c++
     cout << "Hello world!" << endl;
  ```
  
  
  
2.
  ```c++
     cout << "CS10A " << "will " << "be " << "fun!" << endl;
  ```
  
  
  
3.
  ```c++
     int sum;
     sum = 10 + 3;
  
     cout << "The sum is: " << sum << endl;
  ```
  
  
  
4.
  ```c++
     string name = "Bob"; int age = 20; cout << name; cout << " is "; cout << age; cout << " years old"; cout << endl;
  ```
  
  
  
5.
  ```c++
     cout << "It's";
     cout << "okay";
     cout << "to";
     cout << "make ";
     cout << "mistakes";
     cout << endl;
  ```
  


6.
  ```c++
     int id;
     cout << "Please enter an id: ";
     cin >> id;
     cout << "Thank you!" << endl;
  ```





Write code to create these lines of text.
1. I can print out a full line of text!



2. This store has 30 bottles of water in stock
   ```c++
      int bottles = 30;
   ```
   
   
   
3. I need 5 notebooks for school.  
   But the notebooks at school cost $20 each.
   ```c++
      int numNotbooks = 5;
      int pricePerBook = 20;
   ```
   
   
   
4. Please enter your name: *Jason*  
   Hello *Jason*, enjoy your stay!
   ```c++
      string name;
   ```
   
   
   
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
      // cout << "Hello ";
      // cout << "World";
   ```
   
   
   
Warnings and Errors:
   What is a syntax error?
   
   What is a logic error?
   
   What's the difference between a compile error and a runtime error?
   
   What is a warning?
   
   
   
   
1.
  ```c++
     string name = "Justin";
     int age = 3;
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
     
     using namespace std;
     
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


7. Fix this code given this error
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

   


8. Fix this code given this error
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
