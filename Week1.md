# Week 1 #

Input and Output  

Write down the output of the code.  
1. ```c++
     cout << "Hello world!" << endl;
   ```
<details>
    <summary>Ans</summary>

Hello world!
</details>
  
2. ```c++
     cout << "CS10A " << "will " << "be " << "fun!" << endl;
   ```
<details>
    <summary>Ans</summary>

CS10A will be fun!
</details>
  
3. ```c++
     int sum;
     sum = 10 + 3;
  
     cout << "The sum is: " << sum << endl;
   ```
<details>
    <summary>Ans</summary>

The sum is: 13
</details>
  
4. ```c++
     string name = "Bob"; int age = 20; cout << name; cout << " is "; cout << age; cout << " years old"; cout << endl;
     // Please... Don't ever code like this
   ```
<details>
    <summary>Ans</summary>

Bob is 20 years old
</details>
  
5. ```c++
     cout << "It's";
     cout << "okay";
     cout << "to";
     cout << "make ";
     cout << "mistakes";
     cout << endl;
   ```
<details>
    <summary>Ans</summary>

It'sokaytomake mistakes
</details>

6. ```c++
     int id;
     cout << "Please enter an id: ";
     cin >> id;
     cout << "Thank you!" << endl;
   ```
<details>
    <summary>Ans</summary>

Please enter an id: *124123*
Thank you!
</details>

7. ```c++
      string firstName = "Kris ";
      string lastName = "Miller";
      int courseId = 10;
      int sectionId = 3;

      cout << "The professor for CS" << courseId << " is " << firstName + lastName << endl;
      cout << "\tMy section is " << sectionId << endl;
   ```
<details>
    <summary>Ans</summary>

The professor for CS 10 is Kris Miller
   My section is 3
</details>

8. ```c++
      #include <iostream>

      using namespace std;

      int main() {
         cout << "10\n9\n8\n7\n6\n5\n4\n3\n2\n1\n0" << endl;
         cout << "\"BLAST OFF!\"" << endl; 

         return 0;
      }
   ```
<details>
    <summary>Ans</summary>

10
9
8
7
6
5
4
3
2
1
0
"BLAST OFF!"
</details>

9. ```c++
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
<details>
    <summary>Ans</summary>

*Chicken*
*Ididntcrosstheroad*
Hello Chicken!
Your id is 9740917

**NOTE: id was never initialized or written into... it contains garbage value**
</details>

Write code to create the given output.
1. I can print out a full line of text!
<details>
    <summary>Ans</summary>

```c++
cout << "I can print out a full line of text!" << endl;
```
</details>

2. This store has 30 bottles of water in stock
   ```c++
      int bottles = 30;
   ```
<details>
    <summary>Ans</summary>

```c++
cout << "This store has " << bottles << " of water in stock" << endl;
```
</details>

3. I need 5 notebooks for school.  
   But the notebooks at school cost $20 each.
   ```c++
      int numNotbooks = 5;
      int pricePerBook = 20;
   ```
<details>
    <summary>Ans</summary>

```c++
cout << "I need " << numNotbooks << " for school." << endl;
cout << "But the notebooks at school cost $" << pricePerBook << " each." << endl;
```
</details>
   
4. Please enter your name: *Jason*  
   Hello *Jason*, enjoy your stay!
   ```c++
      string name;
   ```
<details>
    <summary>Ans</summary>

```c++
cout << "Please enter your name: ";
cin >> name;
cout << "Hello " << name << ", enjoy your stay!" << endl;
```
</details>

5. Welcome to SI. Please sign in with your Username and SID.  
   Username: *foo1*  
   SID: *123456789*
   ```c++
      // Create your own variables for this problem
   ```
<details>
    <summary>Ans</summary>

```c++
string username;
int sid = 0;

cout << "Welcome to SI. Please sign in with your Username and SID." << endl;
cout << "Username: "; 
cin >> username;
cout << "SID: "; 
cin >> sid;
```
</details>

6. Enter the name of your school: *UCR*  
   Please rate *UCR* out of 10.  
   *8*  
   You rated *UCR* a *8*/10.
   ```c++
      // Create your own variables for this problem
   ```
<details>
    <summary>Ans</summary>

```c++
string school;
int rating;

cout << "Enter the name of your school: ";
cin >> school;
cout << "Please rate " << school << " out of 10." << endl;
cin >> rating;
cout << "You rated " << school << " a " << rating << "/10." << endl;
```

</details>