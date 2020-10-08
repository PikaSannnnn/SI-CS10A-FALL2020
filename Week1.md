# Week 1 #

Input and Output  

Write down the output of the code.
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



7.
   ```c++
      string firstName = "Kris ";
      string lastName = "Miller";
      int courseId = 10;
      int sectionId = 3;

      cout << "The professor for CS" << courseId << " is " << firstName + lastName << endl;
      cout << "\tMy section is " << sectionId << endl;
   ```



8.
   ```c++
      #include <iostream>

      using namespace std;

      int main() {
         cout << "10\n9\n8\n7\n6\n5\n4\n3\n2\n1\n0" << endl;
         cout << "\"BLAST OFF!\"" << endl; 

         return 0;
      }
   ```



9.
   ```c++
      #include <iostream>

      using namespace std;

      int main() {
         string username;
         int id;

         cin >> username;
         cin >> password;

         cout << "Hello " + username + "!" << endl;
         cout << "Your id is: " << id << endl;

         return 0;
      }
   ```



Write code to create the given output.
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



5. Welcome to SI. Please sign in with your Username and SID.  
   Username: *foo1*  
   SID: *123456789*
   ```c++
      // Create your own variables for this problem
   ```



6. Enter the name of your school: *UCR*  
   Please rate *UCR* out of 10.  
   *8*  
   You rated *UCR* a *8*/10.
   ```c++
      // Create your own variables for this problem
   ```