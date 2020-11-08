# Week 3

### Review: Write code to fulfill the requests. (Include the appropriate headers)
---
1. Ask the user for their first and last name. Then output their name in the following format (lastname, firstname)

<details>
    <summary>Ans</summary>

```c++
#include <iostream>
#include <string>

using namespace std;

int main() {
    string first;
    string last;

    cout << "Enter first and last name: ";
    cin >> first >> last;

    cout << "(" << last << ", " << first << ")" << endl;
    
}
```
</details>

2. Ask the user to input two **integers**, and output the product of the two

<details>
    <summary>Ans</summary>

```c++
#include <iostream>

using namespace std;

int main() {
    int num1 = 0;
    int num2 = 0;

    cout << "Enter two integers: ";
    cin >> num1 >> num2;

    cout << "Product: " << num1 * num2 << endl;
}

```
</details>

3. Ask the user for any **integer**, then display the square root of that number. 

<details>
    <summary>Ans</summary>

```c++
#include <iostream>
#include <cmath>

using namespace std;

int main() {
    int x = 0;

    cout << "Enter an integer: ";
    cin >> x;
    
    cout << "sqrt: " << sqrt(x) << endl;
}

```
</details>

4. Ask the user for two **integers**, and output the first to the power of the second. 

<details>
    <summary>Ans</summary>

```c++
#include <iostream>
#include <cmath>

using namespace std;

int main() {
    int x = 0;
    int y = 0;

    cout << "Enter two integers: ";
    cin >> x >> y;

    cout << "Pow: " << pow(x, y) << endl;
}

```
</details>

5. Ask the user to input two **integers**, and output the first divided by the second as a decimal.

<details>
    <summary>Ans</summary>

```c++
#include <iostream>

using namespace std;

int main() {
    int x = 0;
    int y = 0;

    cout << "Enter two integers: ";
    cin >> x >> y;

    cout << static_cast<double>(x) / static_cast<double>(y) << endl;    
}

```
</details>

6. Ask the user to input two **integers**, and output, with 2 decimal places, the second subtracted by the first.

<details>
    <summary>Ans</summary>

```c++
#include <iostream>
#include <iomanip>

using namespace std;

int main() {
    int x, y;
    
    cout << "Enter two integers: ";
    cin >> x >> y;

    cout << fixed << setprecision(2) << x - y << endl;    
}

```
</details>

7. Ask the user to input two **integers**, and output the first divided by the second and the remainder.

<details>
    <summary>Ans</summary>

```c++
#include <iostream>

using namespace std;

int main() {
    int x, y;

    cout << "Enter two integers: ";
    cin >> x >> y;

    cout << x/y << "rem" << x%y << endl;
}

```
</details>

8. Write a code that asks the user for the length, width, and height of a cube. Then, output the area and perimeter of one of the sides, and the volume of the cube

<<details>
    <summary>Ans</summary>

```c++
#include <iostream>

using namespace std;

int main() {
    double l, w, h;

    cout << "Enter the length, width, height with spaces in between: ";
    cin >> l >> w >> h;

    cout << "Perimeter: " << l * 4 << endl;
    cout << "Area: " << l * w << endl;
    cout << "Volume: " << l * w * h << endl;
}

```
</details>

9. Ask the user to input a 6 digit number. Shift the decimal 2 places to the left and output the value.

<details>
    <summary>Ans</summary>

```c++
#include <iostream>

using namespace std;

int main() {
    double x = 0;
    
    cout << "Enter a 6 digit number: ";
    cin >> x;

    x /= 100;
    cout << x << endl;
}

```
</details>


### Branches ###
---
What are branches?  

How do you set up a simple branch?  

How do you set up nested branches?  


Example:  
```c++
    if (3 == 3) {
        std::cout << "3 is equal to itself" << std::endl;
    }
    else {
        std::cout << "3 is not equal to itself" << std::endl;
    }
    if (age >= 10 ){
        if (age >= 18) {
            std::cout << "You're an adult, in the U.S." << std::endl;
        }
        else {
            std::cout << "You're an adolescent" << std::endl;
        }
    }
    else if (age >= 1) {
        std::cout << "You are a child right now" << std::endl;
    }
    else {
        std::cout << "You are not yet born" << std::endl;
    }
```

##### Practice  
<br>
1. Ask the user for an **integer** and output the number as a negative.

<details>
    <summary>Ans</summary>

```c++
int x = 0;
cin >> x;

if (x > 0) {
    x *= -1;
}

cout << x << endl;
```
</details>

2. Ask the user for a positive **integer** and output the equivalent character with the number if and only if the character is a letter.

<details>
    <summary>Ans</summary>

```c++
int x = 0;
char y;
cin >> x;

if (x > 0) { y = x; }

if ((y >= 'A' && y <= 'Z') || (y >= 'a' && y <= 'z')) {
    cout << y << " - " << x << endl;
}
```
</details>

3. Ask the user to input 10 **integers** and output all the even numbers.

<details>
    <summary>Ans</summary>

```c++
int a,b,c,d,e,f,g,h,i,j;
cin >> a >> b >> c >> d >> e >> f >> g >> h >> i >> j;

if (a % 2 == 0) { cout << a << endl; }
if (b % 2 == 0) { cout << b << endl; }
if (c % 2 == 0) { cout << c << endl; }
if (d % 2 == 0) { cout << d << endl; }
if (e % 2 == 0) { cout << e << endl; }
if (f % 2 == 0) { cout << f << endl; }
if (g % 2 == 0) { cout << g << endl; }
if (h % 2 == 0) { cout << h << endl; }
if (i % 2 == 0) { cout << i << endl; }
if (j % 2 == 0) { cout << j << endl; }
```
</details>

4. Ask the user for a 6 letter word and store each letter in a **char**. Output only the consonants.

<details>
    <summary>Ans</summary>

This one will take a long time to code without loops; thus, we shall use a loop here. (Also, I'm lazy to code all of it)  
We will also be using an array here (denoted by the variable declaration with a `[]`). Arrays are lists. You can view it as similar to a string:  
Each spot in the list is its own index and can be accessed and written in, but unlike strings, we can only use `[]`, there is not .at()  
```c++
char letters[6]; // creating an array of size 6 for the 6 characters

for (int i = 0; i < 6; i++) {
    cin >> letters[i];
}

for (int i = 0; i < 6; i++) {
    if (letters[i] != 'a' && letters[i] != 'A' && letters[i] != 'e' && letters[i] != 'E' && letters[i] != 'i' && letters[i] != 'I' && letters[i] != 'o' && letters[i] != 'O' && letters[i] != 'u' && letters[i] != 'U') {
        cout << letters[i];
    }
}
```
</details>

5. Ask the user for a 5 letter word and store each letter in a **char**. Output the *integer* sum of each vowel in the word.

<details>
    <summary>Ans</summary>

This will follow the same format as #4  
```c++
char letters[5];
int sum = 0;

for (int i = 0; i < 5; i++) {
    cin >> letters[i];
}

for (int i = 0; i < 5; i++) {
    sum += letters[i];
}

cout << sum << endl;
```
</details>

6. Ask the user for an **integer** and output "__ is within range" if and only if the number is in between 10 and 20

<details>
    <summary>Ans</summary>

```c++
int x = 0;

cin >> x;

if (x > 0 && x < 20) {
    cout << x << " is within range" << endl;
}
```
</details>

7. Ask the user for a number and output "__ is equal" iff the number is equal to 50.0.

<details>
    <summary>Ans</summary>

```c++
double x = 0.0;
cin >> x;

if (x == 50.0) {    // NOTE: if you're comparing with decimals, if the decimal has been modified, make sure you account for an error margin, i.e. as long as the error margin is under 0.0001, they are equal 
    cout << x << " is equal" << endl;
}
```
</details>

8. Ask the user for 3 numbers and output the highest and lowest number.

<details>
    <summary>Ans</summary>

```c++
int x, y, z;
cin >> x >> y >> z;

cout << "Lowest: ";
if (x <= y && x <= z) {
    cout << x << endl;
}
else if (y <= z && y <= x) {
    cout << y << endl;
}
else {
    cout << z << endl;
}

cout << "Highest: ";
if (x >= y && x >= z) {
    cout << x << endl;
}
else if (y >= z && y >= x) {
    cout << y << endl;
}
else {
    cout << z << endl;
}
```
</details>

##### Branch Matching
* [Branch Matching](https://docs.google.com/document/d/1Dq7ayMhDSc_vmPu0N83ilkn_4HNFAltS4-pRoCeJTQY/edit)