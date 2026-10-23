# LAB REPORT 06: REPETITIVE STRUCTURES (`WHILE` & `DO-WHILE` LOOPS)

## 📌 Student Information
* **Name:** M. Hasnain
* **Section:** C
* **Roll No:** 29
* **Reg No:** 1414
* **Course:** Programming Fundamentals (Lab)
* **Instructor:** Ms. Hafsa

---

## 🎯 Lab Objectives
* Understand the mechanics of condition-controlled iteration in C.
* Implement pre-test iteration structures (`while` loops) for dynamic and conditional repetition.
* Implement post-test iteration structures (`do-while` loops) to guarantee at least one execution of a code block.
* Apply entry-controlled and exit-controlled loops to mathematical computations, interactive loops, accumulators, and nested pattern generation.

---

## 📋 Table of Contents
1. [Task 01: Pre-test vs Post-test Counting (1 to 10)](#task-01)
2. [Task 02: Decrementing Sum Series](#task-02)
3. [Task 03: Factorial Calculation ($n!$)](#task-03)
4. [Task 04: Exponential Power Computation ($base^{power}$)](#task-04)
5. [Task 05: Exit-Controlled Interactive Loop (`Y/N`)](#task-05)
6. [Task 06: Multiplication Table Generator](#task-06)
7. [Task 07: Nested Multiplication Tables Matrix](#task-07)
8. [Task 08: Triple-Nested While Loop Permutations](#task-08)
9. [Task 09: Prime Number Verification Range](#task-09)
10. [Task 10: Conditional Loop Exit on Odd Input](#task-10)
11. [Tasks 11–18: Star Patterns & Tabular Multiples](#tasks-11-18)

---

<a name="task-01"></a>
### Task 01: Pre-test (`while`) vs. Post-test (`do-while`) Counting

```c
//Task01
#include <stdio.h>
#include <stdlib.h>

int main() {
    int i = 1;
    int j = 1;
    
    printf("While loop\n");
    while (i <= 10) {
        printf("%d\n", i);
        i++;
    }

    printf("\n");

    printf("Do-while loop\n");
    do {
        printf("%d\n", j);
        j++;
    } while (j <= 10);

    return 0;
}
```
* **Output Preview:** Displays numbers 1 through 10 sequentially under both loop headers.

---

<a name="task-02"></a>
### Task 02: Decrementing Sum Series ($n + (n-1) + \dots + 1$)

```c
#include <stdio.h>

int main() {
    int n;
    int sum = 0;

    printf("Enter an integer value: ");
    scanf("%d", &n);

    int i = n;
    while (i > 1) {
        printf("%d+", i);
        sum += i;
        i--;
    }

    sum += i;
    printf("%d=%d\n", i, sum);

    return 0;
}
```

---

<a name="task-03"></a>
### Task 03: Factorial Calculation ($n!$)

```c
//Task03
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n;
    int factorial = 1;

    printf("Enter an integer value: ");
    scanf("%d", &n);
    printf("%d! = ", n);

    int i = n;
    while (i > 1) {
        printf("%d*", i);
        factorial *= i;
        i--;
    }

    factorial *= i;
    printf("%d = %d\n", i, factorial);

    return 0;
}
```

---

<a name="task-04"></a>
### Task 04: Exponential Power Computation

```c
#include <stdio.h>

int main() {
    int base, power;

    printf("Enter an integer base value: ");
    scanf("%d", &base);
    printf("Enter an integer power value: ");
    scanf("%d", &power);

    int result = 1;
    int counter = 0;
    
    while (counter < power - 1) {
        printf("%d*", base);
        result *= base;
        counter += 1;
    }
    result *= base;
    printf("%d = %d\n", base, result);

    return 0;
}
```

---

<a name="task-05"></a>
### Task 05: Exit-Controlled Interactive Loop (`Y/N`)

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    char choice;
    do {
        int num1, num2;
        int sum;

        printf("Enter first integer value: ");
        scanf("%d", &num1);
        printf("Enter second integer value: ");
        scanf("%d", &num2);

        sum = num1 + num2;
        printf("Sum: %d\n", sum);

        printf("Do you want to continue the loop? (Y/N): ");
        scanf(" %c", &choice);

    } while (choice == 'Y');

    return 0;
}
```

---

<a name="task-06"></a>
### Task 06: Multiplication Table Generator

```c
//Task06
#include <stdio.h>
#include <stdlib.h>

int main() {
    int number, iterations;

    printf("Enter an integer value for number: ");
    scanf("%d", &number);
    printf("Enter an integer value for iterations: ");
    scanf("%d", &iterations);

    int counter = 1;
    while (counter <= iterations) {
        printf("%d x %d = %d\n", number, counter, number * counter);
        counter += 1;
    }

    return 0;
}
```

---

<a name="task-07"></a>
### Task 07: Nested Multiplication Tables Matrix
* Implements nested iteration structures using `while` and `do-while` loops to generate a $6 \times 6$ grid matrix.

---

<a name="task-08"></a>
### Task 08: Triple-Nested While Loop Permutations
* Iterates through 3 independent counters (`i`, `j`, `k`) from 1 to 3 to output all 27 3-digit permutations.

---

<a name="task-09"></a>
### Task 09: Prime Number Verification Range
* Uses trial division inside nested `while` loops to identify and print all prime numbers up to a user-defined threshold.

---

<a name="task-10"></a>
### Task 10: Conditional Loop Exit on Odd Input
* Continuously computes squares of numbers inside a `do-while` loop, breaking immediately upon detecting an odd number.

---

<a name="task-11-18"></a>
### Tasks 11–18: Star Patterns & Tabular Multiples
* Includes implementations for:
  * **Task 11:** Right-Angled Star Triangle
  * **Task 12:** Inverted Right-Angled Triangle
  * **Task 13:** Right-Aligned Star Triangle
  * **Task 14:** 5-Row Inverted Triangle
  * **Task 15:** Centered Pyramidal Pattern
  * **Task 16:** Hollow Square Pattern
  * **Task 17:** Alternating Grid Rows Pattern
  * **Task 18:** Tabular Multiples with Tab Spacing

---
> *Note: Console output images and terminal screenshots for all tasks are stored locally in the lab submission workspace.*