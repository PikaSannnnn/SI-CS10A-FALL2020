# Week 5

### Loops
---
* What are Loops?
* What are `while` loops?
* What are `for` loops?

###### Session 28:
![S028 Loops](https://github.com/PikaSannnnn/SI-CS10A-FALL2020/blob/main/Images/Session028%20W5S1.png)
###### Session 29:
![S029 Loops](https://github.com/PikaSannnnn/SI-CS10A-FALL2020/blob/main/Images/Session029%20W5S1.jpg)

### While Loops

1. ```c++
    const int passScore = 70;
    int score = 0;
    bool isPassing;

    while (!isPassing) {
        cout << "You! Shall! Not! Pass!" << endl;
        if (score >= 70) { isPassing = true; }

        score += 5;
    }
    ```
<details>
    <summary>Ans</summary>

You! Shall! Not! Pass!  
You! Shall! Not! Pass!  
You! Shall! Not! Pass!  
You! Shall! Not! Pass!  
You! Shall! Not! Pass!  
You! Shall! Not! Pass!  
You! Shall! Not! Pass!  
You! Shall! Not! Pass!  
You! Shall! Not! Pass!  
You! Shall! Not! Pass!  
You! Shall! Not! Pass!  
You! Shall! Not! Pass!  
You! Shall! Not! Pass!  
You! Shall! Not! Pass!  
You! Shall! Not! Pass!
</details>

2. ```c++
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
<details>
    <summary>Ans</summary>

Enter a number: *5*  
Enter a character: *a*  
5 != a  
Enter a number: *65*  
Enter a character: *a*  
65 != a  
Enter a number: *65*  
Enter a character: *A*  
65 == A
</details>

3. ```c++
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
<details>
    <summary>Ans</summary>

3  
9  
7  
2  
8  
9  
2  
6  
7
</details>

4. ```c++
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
<details>
    <summary>Ans</summary>

0-0-0-0  
0-0-0-0  
0-0-0-0  
0-0-0-0  
0-0-0-0  
0-0-0-0  
0-0-0-0  
0-0-0-0  
0-0-0-0  
**INF**
</details>

5. ```c++
    bool isTrue = false;
    int num1 = 0;
    int num2 = 10;

    while (isTrue || (num1 < 5 && num2 > 5)) {
        cout << num1++ << " " << num2-- << endl;
        if (isTrue) {
            isTrue = false;
        }
        if (num1 == num2) { 
            isTrue = true;
            num1++;
            num2--;
        }
    }
    ```
<details>
    <summary>Ans</summary>

0 10
1 9
2 8
3 7
4 6
6 4
</details>

6. ```c++
    int input = 0;
    int old = 0;

    cout << "Enter a nunber. -1 to exit: ";
    cin >> input;
    while (input != -1) {
        if (input < 0) {
            cout << "New number: " << input * -1 << endl;
        }
        else {
            cout << "I'll allow your number" << endl;
        }
        
        cout << "Enter a nunber. -1 to exit: ";
        cin >> input;
    }
    ```
<details>
    <summary>Ans</summary>

Enter a nunber. -1 to exit: *1*
I'll allow your number
Enter a nunber. -1 to exit: *-2*
New number: 2
Enter a nunber. -1 to exit: *-1*
</details>
<details>
    <summary></summary>

</details>
<details>
    <summary></summary>

</details>

#### Coding:
1. Broken Calculator: You will create a calculator, a little more simplified than last week's challenge activity, that will give an unexpected answer. It will:
    - Ask the user for **an operator** (+/-) 
        - If the user inputted an operator that is **not** + or -, it should output *"Invalid Operation"* and continue to ask the user for an operator.
    - Ask the user for **2 numbers** (x/y)
    - Compute the **opposite** operation between the two numbers (x with y)
    - Output its **opposite** sign (e.g. 9 will become -9)
2. Number Tracker: You will create a system that will keep track of three positive numbers. It will:
    - Ask the user for a **positive integer**
    - If the number is higher than the highest number tracked, make this new number the highest, and the previous highest the second highest.
    - If the number is higher than the second highest number tracked, make this new number the second highest.
    - The system will continue to ask for **positive integers** until a **-1** is inputted, from which the system will exit
    - *Hint: How do I compare and swap numbers?*
    - *Hint: How do I make sure the input is always positive except for -1?*

### For Loops
1. ```c++
    char letters[6];

    cout << "Enter a 6 letter word: ";
    for (int i = 0; i < 6; i++) {
        cin >> letters[i];
    }
    ```
<details>
    <summary>Ans</summary>

Enter a 6 letter word: *Pizzas*
</details>

2. ```c++
    for (int i = 0; i < 3; i++) {
        for (int j = i; j < 3; j++) {
            cout << i << "-" << j << endl;
        }
    }
    ```
<details>
    <summary>Ans</summary>

0-0  
0-1  
0-2  
1-1  
1-2  
2-2  
</details>

3. ```c++
    int sum = 0;

    for (int i = 0; i < 10; i++) {
        sum += i;
    }

    cout << static_cast<double>(sum) / 10 << endl;
    ```
<details>
    <summary>Ans</summary>

4.5
</details>

4. ```c++
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 5; j++) {
            if (j == 0 || j == 4) {
                for (int k = 0; k < 5; k++) {
                    cout << "#";
                }
            }
            else {
                cout << "#";
                for (int k = 0; k < 3; k++) {
                    cout << " ";
                }
                cout << "#";
            }
            cout << endl;
        }
    }
    ```
<details>
    <summary>Ans</summary>
<p>
    #####<br>
    #&nbsp; &nbsp; &nbsp; #<br> 
    #&nbsp; &nbsp; &nbsp; #<br>
    #&nbsp; &nbsp; &nbsp; #<br>
    #####<br>
    #####<br>
    #&nbsp; &nbsp; &nbsp; #<br> 
    #&nbsp; &nbsp; &nbsp; #<br>
    #&nbsp; &nbsp; &nbsp; #<br>
    #####
</p>
</details>
<details>
    <summary>Ans</summary>

</details>
<details>
    <summary></summary>

</details>
<details>
    <summary></summary>

</details>
<details>
    <summary></summary>

</details>

#### Coding:
1. Guess the Number: You will be creating a fun "Guess the Number" game. It will:
    - Generate a random number between **0 - 20**. (Use `srand(0)`)
    - Ask the user for a number.
        - If the input matches the random number, you will output *"Correct!"* and **exit**
            - **NOTE:** The game should exit, if correct, regardless of how many attemps the user has
        - Otherwise, you will output *"Incorrect! You have _ tries left."*
        - The user will have **5** attempts to guess the number
        - When they have **3** attempts remaining, give a hint of whether the number is **even** or **odd**
        - When they have **2** attempt remaining, give a hint of whether it is **greater than or less than 10**
    - If the user runs out of tries, output *"Better luck next time!"* and exit
    - *Hint: Should the `for` loop count up or down?*
    - *Hint: How do get the number **20** from rand()?*