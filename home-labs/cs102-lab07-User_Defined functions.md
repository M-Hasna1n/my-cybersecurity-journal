# Lab 07: User-Defined Functions in C

This repository contains C source code and execution summaries for user-defined functions, including function prototypes, chained function calls, parameter passing, return values, conditional comparisons, variable swapping, and aggregate calculations.

---

## Task 01: User-Defined Function for Name and Batch Display

### Description

Demonstrates the creation and invocation of a user-defined function `named()` that prints student identification details without returning a value. The `main()` function calls `named()`, which outputs the name and batch information to the console.

### C Source Code

```c
//Task1
#include <stdio.h>
#include <stdlib.h>

char named(){
    printf("Name: M.Hasnain\n");
    printf("Batch No. : 1st (Fall 2026)");
}

int main(int argc, char *argv[]) {

    char about_me= named();
    return 0;
}

```



### Execution Output

```text
Name: M.Hasnain
Batch No. : 1st (Fall 2026)

```



---

## Task 02: Function Prototypes and Chained Function Calls

### Description

Demonstrates declaring function prototypes (`test_1()`, `test_2()`, and `test_3()`) above `main()` and executing chained function calls. Calling `test_1()` triggers `test_2()`, which subsequently invokes `test_3()`, illustrating sequential control flow across multiple functions.

### C Source Code

```c
//Task2
#include <stdio.h>
#include <stdlib.h>

//It's called function prototype :)
char test_1();
char test_2();
char test_3();


int main(){

    char Test_1=test_1();
    return 0;
}

char test_1(){
    printf("Week 9 (test_1)\n");
    test_2();
}

char test_2(){
    printf("Week 9 (test_2)\n");
    test_3();
}

char test_3(){
    printf("Week 9 (test_3)\n");
}

```



### Execution Output

```text
Week 9 (test_1)
Week 9 (test_2)
Week 9 (test_3)

```



---

## Task 04: Function Multiplication with Parameter Passing

### Description

Implements a user-defined function `multiply(int a, int b, int c)` that accepts three integer arguments, computes their product (`a * b * c`), and returns the result to `main()` for display.

### C Source Code

```c
//Task4
#include<stdio.h>
#include<stdlib.h>

int multiply(int a, int b, int c){
    return a*b*c;
}

int main(){
    int a,b,c;
    printf("Enter three integers values:\n");
    scanf("%d %d %d", &a, &b, &c);

    int multiplication=multiply(a,b,c);
    printf("Mulitplication: %d\n", multiplication);

}

```



### Execution Output

```text
Enter three integers values:
3
3
3
Mulitplication: 27

```



---

## Task 05: Conditional Function for Finding Greater Number

### Description

Uses a user-defined function `greater(int a, int b)` containing an `if-else` conditional structure to compare two user-supplied integers and print the larger value.

### C Source Code

```c
//Task5
#include<stdio.h>
#include<stdlib.h>

int greater(int a, int b){
    if(a>b){
        printf("Greater number is %d", a);
    }
    else{
        printf("Greater number is %d", b);
    }
}

int main(){
    int a,b;
    printf("Enter two integers values:\n");
    scanf("%d %d", &a, &b);

    int greatest=greater(a,b);

}

```



### Execution Output

```text
Enter two integers values:
6
7
Greater number is 7

```



---

## Task 06: Value Swapping Function

### Description

Demonstrates parameter passing and variable value swapping inside a user-defined function `swap(int num1, int num2)`. The function preserves the initial values in temporary variables (`original_num1` and `original_num2`), swaps `num1` and `num2`, and prints both the original and swapped pairs.

### C Source Code

```c
//Task6
#include<stdio.h>
#include<stdlib.h>

int swap(int num1, int num2){
    int original_num1=num1; //1=1
    int original_num2=num2; //2=2

    //2=2
    num1 = num2;
    //1=1
    num2 = original_num1;

    printf("Original values are: \n %d(num1) and %d(num2)\n\n", original_num1, original_num2);
    printf("Swapped values are: \n %d(num1) and %d(num2)", num1, num2);

}

int main(){
    int num1, num2;
    printf("Enter two integers values:\n");
    scanf("%d %d", &num1, &num2);

    int swapped=swap(num1,num2);

}

```



### Execution Output

```text
Enter two integers values:
1
2
Original values are:
 1(num1) and 2(num2)

Swapped values are:
 2(num1) and 1(num2)

```



---

## Task 07: Sum and Average Calculator Function

### Description

Implements a user-defined function `sum_aver()` that takes five integer inputs, calculates their total sum and floating-point average (`sum / 5.0`), and prints the formatted results to two decimal places (`%.2f`).

### C Source Code

```c
//Task7
#include<stdio.h>
#include<stdlib.h>

int sum_aver(int num1, int num2, int num3, int num4, int num5, int sum, float average){

    sum = num1+num2+num3+num4+num5;
    average = sum/5.0;

    printf("Sum: %d\n", sum);
    printf("Average: %.2f", average);
}

int main(){
    int num1, num2, num3, num4, num5, sum;
    float average;
    printf("Enter five integer values: \n");
    scanf("%d %d %d %d %d", &num1, &num2, &num3, &num4, &num5);

    sum_aver(num1, num2, num3, num4, num5, sum, average);

}

```



### Execution Output

```text
Enter five integer values:
1
3
5
7
11
Sum: 27
Average: 5.40

```
