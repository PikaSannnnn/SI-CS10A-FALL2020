# Week 5

### Loops
---
* What are Loops?
* What are `while` loops?
* What are `for` loops?

### While Loops
<details>
    <summary>1.</summary>

```c++
const int passScore = 70;
int score = 0;
bool isPassing;

while (!isPassing) {
    cout << "You! Shall! Not! Pass!" << endl;
    if (score >= 70) { isPassing = true; }

    score += 5;
}
```
</details>
<details>
    <summary>2.</summary>

```c++
int userNum = 0;
char userChar;

cout << "Enter a number: ";
cin >> userNum;
cout << "Enter a character: ";
cin >> userChar;

while (userNum != userChar) {
    cout << userNum << " != " << userChar << endl;
    
    cout << "Enter a number: ";
    cin >> userNum;
    cout << "Enter a character: ";
    cin >> userChar;
}

cout << userNum << " == " << userChar << endl;
```
</details>
<details>
    <summary>3.</summary>

```c++
srand(123456789); 
/*  Assume that the order of numbers is this:
    12423, 5501239, 49507, 93852, 6802058, 9433049, 81208392, 345836, 7, 23093280, 23249823, 10
*/
bool isTen = false;
int currNum = 0;

while (!isTen) {
    currNum = rand() % 10;
    if (currNum == 0) { isTen = true; }
    else {
        cout << currNum << endl;
    }
}
```
</details>
<details>
    <summary>4.</summary>

```c++
int i = 0;
int j = 0;
int k = 0;
int l = 0;

while (i < 2) {
    while (j < 3) {
        while (k < 1) {
            while (l < 5) {
                cout << i << "-" << j << "-" << k << "-" << l << endl;
            }
        }
    }
}
```
</details>
<details>
    <summary>5.</summary>

</details>
<details>
    <summary>6.</summary>

</details>
<details>
    <summary>7.</summary>

</details>
<details>
    <summary>8.</summary>

</details>

#### Coding:
* Broken Calculator: You will create a calculator, a little more simplified than last week's challenge activity, that will give an unexpected answer. It will:
    - Ask the user for __an operator__ (+/-) 
        - If the user inputted an operator that is __not__ + or -, it should output *"Invalid Operation"* and continue to ask the user for an operator.
    - Ask the user for __2 numbers__ (x/y)
    - Compute the **opposite** operation between the two numbers (x with y)
    - Output its **opposite** sign (e.g. 9 will become -9)

### For Loops
<details>
    <summary>1.</summary>

```c++
cout << "Enter a 6 letter word: ";
for (int i = 0; i < 6; i++) {
    cin >> letters[i];
}
```
</details>

<details>
    <summary>2.</summary>

```c++
for (int i = 0; i < 100; i++) {
    for (int j = i; j < 100; j++) {
        cout << i << "-" << j << endl;
    }
}
```
</details>
<details>
    <summary>3.</summary>

</details><details>
    <summary>4.</summary>

</details><details>
    <summary>5.</summary>

</details><details>
    <summary>6.</summary>

</details><details>
    <summary>7.</summary>

</details><details>
    <summary>8.</summary>

</details>