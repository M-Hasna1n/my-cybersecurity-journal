# Homelab 04: Conditional Statements in C

This repository contains C source code and execution summaries for tasks covering conditional logic (`if`, `if-else`, `else-if` ladders, and `switch` statements).

---

## Task 01: Simple Conditional Evaluation

### Description

This program demonstrates the usage of a simple `if` condition in C to evaluate user input. It prompts the user to enter an integer value and reads it using `scanf()`. The program then checks if the entered integer is greater than 10 using the condition `num > 10`. If the condition evaluates to true, it executes the code block containing `printf("I am greater than ten")`. If the input value is 10 or less, the condition evaluates to false, skipping the conditional block and terminating execution.

### C Source Code

```c
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int num;
    printf("Enter an integer value:");
    scanf("%d", &num);

    if (num > 10) {
        printf("I am greater than ten");
    }

    return 0;
}

```

### Output Analysis

During execution, the prompt requests an integer input. The user enters `12`. The relational comparison `12 > 10` yields true, triggering the output statement: `I am greater than ten`. Finally, the program returns `0` and exits successfully.

---

## Task 02: Difference Calculation using If-Else

### Description

This program calculates the absolute-style difference between two user-provided integer values using an `if-else` control structure. It prompts the user to enter two integers (`num1` and `num2`). The `if` condition checks whether `num1 < num2`. If true, it subtracts `num1` from `num2` (`result = num2 - num1`) to ensure a non-negative result and displays it. If `num1` is greater than or equal to `num2`, execution shifts to the `else` block, calculating `result = num1 - num2` before printing the final difference.

### C Source Code

```c
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int num1, num2, result;
    printf("Enter two integer values:");
    scanf("%d %d", &num1, &num2);

    if (num1 < num2) {
        result = num2 - num1;
        printf("Result: %d", result);
    } else {
        result = num1 - num2;
        printf("Result: %d", result);
    }

    return 0;
}

```

### Output Analysis

When executed, the program prompts for two values. The user enters `6` and `7`. Since `6 < 7` evaluates to true, the `if` block executes, performing `7 - 6` to store `1` in `result`. The output displays `Result: 1`, and the process exits with a return value of `0`.

---

## Task 03: Basic Arithmetic Calculator using If-Else Ladder

### Description

This program implements a basic arithmetic calculator using an `else-if` decision ladder. It accepts two integers (`num1` and `num2`) and an operator character (`Operator`). The program compares the entered operator against valid symbols using equality checks:

* If `'+'`, it performs addition (`num1 + num2`).
* If `'-'`, it performs subtraction (`num1 - num2`).
* If `'/'`, it performs integer division (`num1 / num2`).
* If `'%'`, it performs the modulus operation (`num1 % num2`).

Once a matching condition is met, the program executes the corresponding mathematical operation and prints the result.

### C Source Code

```c
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int num1, num2, addition, subtraction, division, mod;
    char Operator;

    printf("Enter two integer values & an operator:");
    scanf("%d %d %c", &num1, &num2, &Operator);

    if (Operator == '+') {
        addition = num1 + num2;
        printf("Addition: %d", addition);
    } else if (Operator == '-') {
        subtraction = num1 - num2;
        printf("Subtraction: %d", subtraction);
    } else if (Operator == '/') {
        division = num1 / num2;
        printf("Division: %d", division);
    } else if (Operator == '%') {
        mod = num1 % num2;
        printf("Modulus: %d", mod);
    }

    return 0;
}

```

### Output Analysis

The program prompts the user to input two integer values and an operator. The user enters `6` for the first integer, `6` for the second, and `+` for the operator. The condition `Operator == '+'` evaluates to true, leading to `addition = 6 + 6`. The program prints `Addition: 12` and exits cleanly.

---

## Task 04: Even and Odd Number Identification

### Description

This program determines whether a given integer is even or odd using the modulus operator (`%`) within an `if-else` statement. It prompts the user for an integer `num` and evaluates `num % 2 == 0`. If the remainder of the number divided by 2 is equal to 0, the number is even, and the `if` block executes. Otherwise, control moves to the `else` block, identifying the number as odd.

### C Source Code

```c
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int num;
    printf("Enter an integer value:");
    scanf("%d", &num);

    if (num % 2 == 0) {
        printf("The given number (%d) is even.", num);
    } else {
        printf("The given number (%d) is odd.", num);
    }

    return 0;
}

```

### Output Analysis

The user inputs `0` when prompted for an integer. The condition `0 % 2 == 0` evaluates to true because 0 divided by 2 leaves a remainder of 0. The program outputs `The given number (0) is even.` and terminates with return value `0`.

---

## Task 05: Vowel Identification using Logical OR Operator

### Description

This program evaluates whether an entered lowercase character is a vowel using compound logical conditions. It prompts the user to input a single character `ch` and checks it against all lowercase English vowels (`'a'`, `'e'`, `'i'`, `'o'`, `'u'`) combined with the logical OR operator (`||`). If `ch` matches any of these five characters, the expression evaluates to true, printing that the character is a vowel. If none match, execution shifts to the `else` block, displaying that the character is not a vowel.

### C Source Code

```c
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    char ch;
    printf("Enter a character:");
    scanf("%c", &ch);

    if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
        printf("The given character (%c) is a vowel.", ch);
    } else {
        printf("The given character (%c) is not a vowel.", ch);
    }

    return 0;
}

```

### Output Analysis

Upon execution, the prompt asks for a character input. The user enters `z`. The program tests `z` against `'a'`, `'e'`, `'i'`, `'o'`, and `'u'`. Since all individual equality checks evaluate to false, the overall OR expression returns false. Control transfers to the `else` block, printing `The given character (z) is not a vowel.` before program completion.

---

## Task 06: Grade Assignment using Switch Case

### Description

This program demonstrates fixed-value conditional evaluation using a `switch` statement in C. It prompts the user to enter subject marks as an integer and stores the value in `marks`. The `switch` statement compares `marks` against specific predefined case labels (`90`, `80`, `70`, and `60`). When a match occurs, the corresponding grade letter (`A`, `B`, `C`, or `D`) is printed to standard output. Each case block ends with a `break` statement to prevent control flow from falling through into subsequent cases.

### C Source Code

```c
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int marks;
    printf("Enter a subject marks:");
    scanf("%d", &marks);

    switch(marks){
        case 90:
            printf("A");
            break;

        case 80:
            printf("B");
            break;

        case 70:
            printf("C");
            break;

        case 60:
            printf("D");
            break;
    }

    return 0;
}

```

### Output Analysis

During execution, the program prompts `Enter a subject marks:`. The user enters `90`. The `switch(marks)` statement matches `case 90:`, executing `printf("A");` followed by `break;`. The console displays `A` and the program exits successfully with return code `0`.

---

## Task 07: Finding the Largest of Three Integers

### Description

This program identifies the maximum value among three user-provided integers using an `else-if` conditional chain combined with the logical AND operator (`&&`). The program prompts for three integer values (`num1`, `num2`, and `num3`) via `scanf()`. It first evaluates `(num1 > num2 && num1 > num3)`. If true, it outputs `num1` as the largest. If false, it checks `(num2 > num1 && num2 > num3)` for `num2`, and `(num3 > num1 && num3 > num2)` for `num3`. If none of these strictly greater conditions are met, control falls to the final `else` block, indicating that all three numbers are equal.

### C Source Code

```c
//Task 07
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int num1, num2, num3;
    int largest_num;

    printf("Enter three integer values:");
    scanf("%d %d %d", &num1, &num2, &num3);

    if(num1>num2 && num1>num3){
        printf("The greater number from the given is %d.", num1);
    }
    else if(num2>num1 && num2>num3){
        printf("The greater number from the given is %d.", num2);
    }
    else if(num3>num1 && num3>num2){
        printf("The greater number from the given is %d.", num3);
    }
    else{
        printf("All the given numbers are equal.");
    }

    return 0;
}

```

### Output Analysis

When executed, the program prompts for three integer inputs. The user enters `6`, `5`, and `4`. The first condition `(6 > 5 && 6 > 4)` evaluates to true. The program immediately executes the corresponding print statement, displaying `The greater number from the given is 6.`, and bypasses the remaining conditions before exiting cleanly with return value `0`.

---

## Task 08: Range Verification using Logical AND

### Description

This program determines whether a given integer falls strictly within the range (50, 100) using an `if-else` statement and the logical AND operator (`&&`). It reads an integer `num` from user input and evaluates the compound condition `num > 50 && num < 100`. If both comparisons return true, the `if` block executes to print that the number lies within the specified range. If either condition fails, control shifts to the `else` block, printing that the number does not lie between 50 and 100.

### C Source Code

```c
//Task 08
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int num;
    printf("Enter and integer value:");
    scanf("%d", &num);

    if(num>50 && num<100){
        printf("The given number (%d) lies between 50 & 100.", num);
    }
    else{
        printf("The given number (%d) doesn't lies between 50 & 100.", num);
    }

    return 0;
}

```

### Output Analysis

The program prompts for an integer value. The user enters `66`. The relational expression evaluates both `66 > 50` (true) and `66 < 100` (true). Because both conditions are satisfied, the compound logical AND evaluates to true, producing the output `The given number (66) lies between 50 & 100.` before terminating with return value `0`.

---

## Task 09: Uppercase and Lowercase Character Classification

### Description

This program classifies a given alphabetical character as uppercase or lowercase using character boundary checks with logical operators. After reading a character `ch` from standard input, it evaluates `ch >= 'A' && ch <= 'Z'`. Because characters are stored as ASCII values in C, this checks whether `ch` falls within the range reserved for uppercase letters. If true, it outputs that the character is uppercase; otherwise, the `else` block executes, reporting the character as lowercase.

### C Source Code

```c
//Task 9
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    char ch;
    printf("Enter and character value:");
    scanf("%c", &ch);

    if(ch >= 'A' && ch <= 'Z'){
        printf("The given character (%c) is in uppercase.", ch);
    }
    else{
        printf("The given character (%c) is in lowercase.", ch);
    }

    return 0;
}

```

### Output Analysis

Upon execution, the prompt asks for a character input. The user inputs `Z`. The condition checks if `'Z'` is greater than or equal to `'A'` and less than or equal to `'Z'`, which evaluates to true. The program prints `The given character (Z) is in uppercase.` and exits with return code `0`.

---

## Task 10: Leap Year Verification

### Description

This program verifies whether a user-specified calendar year is a leap year using standard astronomical rules implemented through modulus operations and logical operators. It takes an integer input `year` and tests the condition `(year % 400 == 0 || year % 4 == 0 && year % 100 != 0)`. A year qualifies as a leap year if it is either evenly divisible by 400, or evenly divisible by 4 while not being divisible by 100. If the condition is satisfied, it prints that the year is a leap year; otherwise, the `else` block outputs that it is not.

### C Source Code

```c
//Task 10
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int year;
    printf("Enter an year:");
    scanf("%d", &year);

    //below are the general conditions for verifying a leap year
    if(year % 400 == 0 || year % 4 == 0 && year % 100 != 0){
        printf("The given year (%d) is a leap year.", year);
    }
    else{
        printf("The given year (%d) is not a leap year", year);
    }

    return 0;
}

```

### Output Analysis

When executed, the program prompts `Enter an year:`. If a leap year is provided, the expression evaluates to true, outputting that the year is a leap year. Otherwise, control passes to the `else` block, displaying that it is not a leap year.

---

## Task 11: Divisibility Check by 5

### Description

This program evaluates whether a given integer is divisible by 5 using the modulus operator (`%`) inside a conditional statement. It prompts the user for an integer `num` and tests `num % 5 != 1`. If the remainder when divided by 5 is not equal to 1, the `if` block executes. Otherwise, control transfers to the `else` block.

### C Source Code

```c
//Task 11
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int num;
    printf("Enter an integer value:");
    scanf("%d", &num);

    //below are the general conditions for verifying a leap year
    if(num % 5 != 1){
        printf("The given number (%d) is divisible by 5.", num);
    }
    else{
        printf("The given number (%d) is not divisible by 5.", num);
    }

    return 0;
}

```

### Output Analysis

During execution, the prompt requests an integer input. The user enters `1`. The condition `1 % 5 != 1` evaluates to `1 != 1`, which is false. Control transfers to the `else` block, producing the output `The given number (1) is not divisible by 5.` and terminating with return code `0`.

---

## Task 12: Day of the Week Mapping using Switch Case

### Description

This program maps an integer input ranging from 1 to 7 to its corresponding weekday name using a `switch` control structure. It prompts the user to enter an integer between 1 and 7 and stores it in `day`. The `switch(day)` block checks the input value against discrete case labels (`case 1:` through `case 7:`). Matching inputs output the corresponding day name (e.g., `1` maps to `Monday`, `2` to `Tuesday`, up to `7` for `Sunday`) followed by a `break` statement to exit the `switch` block.

### C Source Code

```c
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int day;
    printf("Enter an integer value between 1-7:");
    scanf("%d", &day);

    switch(day){
        case 1:
            printf("Monday");
            break;

        case 2:
            printf("Tuesday");
            break;

        case 3:
            printf("Wednesday");
            break;

        case 4:
            printf("Thursday");
            break;

        case 5:
            printf("Friday");
            break;

        case 6:
            printf("Saturday");
            break;

        case 7:
            printf("Sunday");
            break;
    }

    return 0;
}

```

### Output Analysis

When executed, the program prompts `Enter an integer value between 1-7:`. The user inputs `6`. The `switch` statement matches `case 6:`, executing `printf("Saturday");` followed by `break;`. The console displays `Saturday` and the process exits with return code `0`.
