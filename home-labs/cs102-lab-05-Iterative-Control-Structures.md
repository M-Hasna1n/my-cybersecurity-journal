# Programming Fundamnetals(C language) - Lab 05 

This repository contains C source code and execution summaries for iterative control structures, including `for` loops, nested loops, star pattern generation, and prime number verification tasks.

---

## Task 01: Printing Numbers from 1 to 10

### Description

Demonstrates basic counter-controlled iteration using a `for` loop in C. The loop initializes an integer counter `i` to 1, continues execution as long as `i <= 10`, and increments `i` by 1 after each iteration. Inside the loop body, `printf("%d ", i)` prints the current counter value followed by a space, generating a horizontal sequence of numbers from 1 through 10.

### C Source Code

```c
//Task01
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    for (int i=1; i<=10; i++){
        printf("%d ", i);
    }
    return 0;
}

```

---

## Task 02: Reverse Summation Series

### Description

Computes the sum of natural numbers from a user-specified integer $n$ down to 1 while dynamically formatting the mathematical series. The program initializes `sum = 0` and loops backward from $i = n$ down to $i = 1$ using `i--`. For each value where $i > 1$, it prints `i+`. When $i$ reaches 1, an `else` branch prints `1=` to complete the series expression before printing the calculated cumulative sum.

### C Source Code

```c
//Task02
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int n;
    int sum=0;

    printf("Enter an integer value:");
    scanf("%d", &n);

    for (int i=n; i>=1; i--){
        if (i>1){
            printf("%d+", i);
        }
        else{
            printf("%d=", i);
        }
        sum+=i;
    }
    printf("%d", sum);
    return 0;
}

```

---

## Task 03: Factorial Calculation with Formatted Multiplication Series

### Description

Calculates the factorial of an input integer $n!$ using an iterative loop while printing the expanded multiplication breakdown. Variable `factorial` is initialized to 1 to avoid zero-product multiplication. The loop iterates backward from $i = n$ down to $i = 1$. For $i > 1$, it prints `i*`. At $i = 1$, it prints `1 = ` followed by the final computed product.

### C Source Code

```c
//Task03
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int n;
    int factorial=1;

    printf("Enter an integer value:");
    scanf("%d", &n);
    printf("%d! = ", n);

    for (int i=n; i>=1; i--){
        if (i>1){
            printf("%d*", i);
        }
        else{
            printf("%d = ", i);
        }
        factorial*=i;
    }
    printf("%d", factorial);

    return 0;
}

```

---

## Task 04: Exponential Power Computation

### Description

Computes the power of a base number raised to an exponent using a `for` loop without relying on standard library mathematical functions. The program takes two integer inputs: `base` and `power`. It initializes `result = 1` and iterates a loop from $i = 1$ up to $i = \text{power}$. In each iteration, it multiplies `result` by `base` (`result *= base`) while printing `base*` for $i < \text{power}$ and `base = ` on the final iteration.

### C Source Code

```c
//Task04
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int base, power;
    int result=1;

    printf("Enter an integer base value:");
    scanf("%d", &base);
    printf("Enter an integer power value:");
    scanf("%d", &power);

    for (int i=1; i<=power; i++){
        if (i<power){
            printf("%d*", base);
        }
        else{
            printf("%d = ", base);
        }
        result*=base;
    }
    printf("%d", result);

    return 0;
}

```

---

## Task 05: Multiplication Table Generator

### Description

Generates a multiplication table for a specified integer up to a user-defined number of iterations. The program prompts for two integer values: `num` (the target table number) and `iterations` (how many rows to generate). A `for` loop runs from $i = 1$ up to $i = \text{iterations}$, outputting `num * i = result` on a new line in each pass.

### C Source Code

```c
//Task05
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int num, iterations;

    printf("Enter an integer value:");
    scanf("%d", &num);
    printf("Enter an integer value for the number of iterations:");
    scanf("%d", &iterations);

    for (int i=1; i<=iterations; i++){
        printf("%d * %d = %d\n", num, i, num*i);
    }

    return 0;
}

```

---

## Task 06: Execution Loop Header Printing

### Description

Demonstrates loop header evaluation where output operations are embedded directly within the update section of a `for` loop header. The loop header `for (int i=1; i<=6; printf("%d ", i++))` handles variable initialization, termination check (`i <= 6`), and post-iteration increment with printing inside the third header expression.

### C Source Code

```c
//Task06
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    for (int i=1; i<=6; printf("%d ", i++)){
        // Explanation of execution:
        /* 1. Initialization, 2. Condition check,
           3. Executes loop body (empty), 4. Increment */
    }
    return 0;
}

```

---

## Task 07: Nested Multiplication Tables Matrix

### Description

Generates multiple full multiplication tables up to a specified integer using nested `for` loops. The outer loop controls the primary table multiplier (`i`), while the inner loop iterates through column multipliers (`j`) from 1 up to `num1`.

### C Source Code

```c
//Task07
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    int num1;

    printf("Enter integer value:");
    scanf("%d", &num1);

    for (int i=1; i<=num1; i++){
        for (int j=1; j<=num1; j++){
            printf("%d * %d = %d\n", i, j, i*j);
        }
        printf("\n");
    }

    return 0;
}

```

---

## Task 08: Triple-Nested Loop Permutation Matrix

### Description

Demonstrates multi-dimensional iteration using three nested `for` loops. The loops maintain three independent index counters (`i`, `j`, and `k`), each iterating from 1 to 3. During execution, the innermost loop prints the triplet `i j k` on standard output.

### C Source Code

```c
//Task08
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    for (int i=1; i<=3; i++){
        for (int j=1; j<=3; j++){
            for (int k=1; k<=3; k++){
                printf("%d %d %d", i, j, k);
                printf("  ");
            }
            printf("\n");
        }
        printf("\n");
    }

    return 0;
}

```

---

## Task 09: Prime Number Verification

### Description

Determines whether an input integer is a prime number using a standalone function `isPrime()`. The function tests all potential divisors from `i = 1` up to `i = num`. If exactly two divisors are found (1 and the number itself), `count == 2` evaluates to true, returning `1` (prime). Otherwise, it returns `0` (not prime).

### C Source Code

```c
//Task09
#include <stdio.h>
#include <stdlib.h>

int isPrime(int num) {
    if (num < 2) return 0;
    
    int count = 0;
    for (int i = 1; i <= num; i++) {
        if (num % i == 0) {
            count++;
        }
    }
    
    if (count == 2) {
        return 1;
    } else {
        return 0;
    }
}

int main(int argc, char *argv[]) {
    int num;
    printf("Enter an integer value:");
    scanf("%d", &num);

    if (isPrime(num)) {
        printf("%d is a Prime number\n", num);
    } else {
        printf("%d is NOT a Prime number", num);
    }

    return 0;
}

```

---

## Task 10: Prime Numbers Generation within Range (1 to 300)

### Description

Generates and prints all prime numbers between 1 and 300 using a modular trial-division helper function. The helper `isPrime()` returns `0` if a number is less than 2 or has any exact divisors between 2 and `num - 1`. The main program loops from `n = 1` to `n = 300`, printing numbers that evaluate as prime.

### C Source Code

```c
//Task10
#include <stdio.h>
#include <stdlib.h>

int isPrime(int num) {
    if (num < 2) {
        return 0;
    }
    for (int i = 2; i < num; i++) {
        if (num % i == 0) {
            return 0;
        }
    }
    return 1;
}

int main(void) {
    printf("Prime numbers from 1 to 300:\n");

    for (int n = 1; n <= 300; n++) {
        if (isPrime(n)) {
            printf("%d ", n);
        }
    }

    printf("\n");
    return 0;
}

```

---

## Task 11: Right-Angled Star Pattern Generation

### Description

Generates a right-angled triangle star pattern using nested `for` loops. The outer loop controls the current row index `i` from 1 to `rows = 6`. The inner loop prints `*` characters `i` times for row `i`, increasing the printed width incrementally per row.

### C Source Code

```c
//Task11
#include <stdio.h>

int main() {
    int rows = 6;

    for (int i = 1; i <= rows; i++) {
        for (int j = 1; j <= i; j++) {
            printf("*");
        }
        printf("\n");
    }

    return 0;
}

```

---

## Task 12: Inverted Right-Angled Star Pattern Generation

### Description

Generates an inverted right-angled triangle star pattern. The outer loop initializes `i = rows = 7` and decrements `i` down to 1. The inner loop prints `*` characters `i` times, decreasing the number of printed stars on each row.

### C Source Code

```c
//Task12
#include <stdio.h>

int main(void) {
    int rows = 7;

    for (int i = rows; i >= 1; i--) {
        for (int j = 1; j <= i; j++) {
            printf("*");
        }
        printf("\n");
    }

    return 0;
}

```

---

## Task 13: Right-Aligned Star Pattern Generation

### Description

Generates a right-aligned right-angled triangle star pattern using two sequential inner `for` loops. For a given total of `rows = 5`, the first inner loop prints leading spaces (`rows - i`), and the second inner loop prints `i` asterisks.

### C Source Code

```c
//Task13
#include <stdio.h>

int main() {
    int rows = 5;

    for (int i = 1; i <= rows; i++) {
        for (int j = 1; j <= rows - i; j++) {
            printf(" ");
        }
        for (int k = 1; k <= i; k++) {
            printf("*");
        }
        printf("\n");
    }

    return 0;
}

```

---

## Task 14: Inverted Right-Angled Star Pattern (5 Rows)

### Description

Generates an inverted right-angled triangle star pattern with a fixed height of 5 rows using nested `for` loops. The outer loop initializes `i = rows = 5` and decrements `i` down to 1, while inner loops handle spacing and asterisks.

### C Source Code

```c
//Task14
#include <stdio.h>

int main() {
    int rows = 5;

    for (int i = rows; i >= 1; i--) {
        for (int j = 1; j <= rows - i; j++) {
            printf(" ");
        }
        for (int k = 1; k <= i; k++) {
            printf("*");
        }
        printf("\n");
    }

    return 0;
}

```

---

## Task 15: Centered Pyramid Star Pattern

### Description

Generates a centered pyramid star pattern using nested `for` loops. For each row `i` up to `rows = 5`, leading spaces are printed followed by an odd number of asterisks calculated by the formula `2 * i - 1`.

### C Source Code

```c
//Task15
#include <stdio.h>

int main() {
    int rows = 5;

    for (int i = 1; i <= rows; i++) {
        for (int j = 1; j <= rows - i; j++) {
            printf(" ");
        }
        for (int k = 1; k <= (2 * i - 1); k++) {
            printf("*");
        }
        printf("\n");
    }

    return 0;
}

```

---

## Task 16: Hollow Square Star Pattern

### Description

Generates a hollow square star pattern of dimensions $5 \times 5$ using nested loops and conditional branching. The inner loop checks whether the current row or column index corresponds to the outer boundary (`i == 1`, `i == size`, `j == 1`, or `j == size`) to print asterisks, leaving the interior hollow.

### C Source Code

```c
//Task16
#include <stdio.h>

int main() {
    int size = 5;

    for (int i = 1; i <= size; i++) {
        for (int j = 1; j <= size; j++) {
            if (i == 1 || i == size || j == 1 || j == size) {
                printf("*");
            } else {
                printf(" ");
            }
        }
        printf("\n");
    }

    return 0;
}

```

---

## Task 17: Alternating Pattern Generation

### Description

Constructs an alternating grid pattern across 8 rows using conditional row checks. Even-numbered rows introduce a leading offset space followed by space-separated asterisks, while odd-numbered rows print continuous consecutive asterisks.

### C Source Code

```c
//Task17
#include <stdio.h>

int main() {
    int rows = 8;

    for (int i = 1; i <= rows; i++) {
        if (i % 2 == 0) {
            printf(" ");
            for (int j = 1; j <= rows; j++) {
                printf("* ");
            }
        } else {
            for (int j = 1; j <= 8; j++) {
                printf("*");
            }
        }
        printf("\n");
    }

    return 0;
}

```

---

## Task 18: Tabular Multiples Formatting

### Description

Generates a formatted mathematical multiples table for numbers 1 through 5 using horizontal tab spacing (`\t`). The program first prints a formatted header row (`N`, `10*N`, `100*N`, `1000*N`) and then uses a `for` loop to compute and align scale multiplications across columns.

### C Source Code

```c
//Task18
#include <stdio.h>

int main() {
    printf("N\t10*N\t100*N\t1000*N\n");

    for (int n = 1; n <= 5; n++) {
        printf("%d\t%d\t%d\t%d\n", n, 10 * n, 100 * n, 1000 * n);
    }

    return 0;
}

```
