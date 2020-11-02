# Week 5

### Loops
---
* What are Loops?
* What are `while` loops?
* What are `for` loops?

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
<details>
    <summary></summary>

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
1. Broken Calculator: You will create a calculator, a little more simplified than last week's challenge activity, that will give an unexpected answer. It will:
    - Ask the user for __an operator__ (+/-) 
        - If the user inputted an operator that is __not__ + or -, it should output *"Invalid Operation"* and continue to ask the user for an operator.
    - Ask the user for __2 numbers__ (x/y)
    - Compute the **opposite** operation between the two numbers (x with y)
    - Output its **opposite** sign (e.g. 9 will become -9)

### For Loops
1. ```c++
    int letters[6];

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
    <summary></summary>

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
    - Generate a random number between __0 - 20__. (Use `srand(0)`)
    - Ask the user for a number.
        - If the input matches the random number, you will output *"Correct!"* and __exit__
            - **NOTE:** The game should exit, if correct, regardless of how many attemps the user has
        - Otherwise, you will output *"Incorrect! You have _ tries left."*
        - The user will have **5** attempts to guess the number
        - When they have __3__ attempts remaining, give a hint of whether the number is __even__ or __odd__
        - When they have __2__ attempt remaining, give a hint of whether it is __greater than or less than 10__
    - If the user runs out of tries, output *"Better luck next time!"* and exit
    - *Hint: Should the `for` loop count up or down?*
    - *Hint: How do get the number __20__ from rand()?*