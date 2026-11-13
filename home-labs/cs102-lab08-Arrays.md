# Lab 08: Arrays in C (1D & 2D Arrays)

This repository contains C source code and execution summaries for one-dimensional and two-dimensional array operations, including static initialization, reverse traversal, dynamic summation, passing arrays to functions, and matrix input/output.

---

## Task 01: Static Array Initialization and Traversal

### Description

Demonstrates the declaration, static initialization, and sequential traversal of a one-dimensional integer array in C. An array `num[5]` is initialized with the elements `{1, 2, 3, 4, 5}`. A `for` loop iterates through indices `0` to `4`, printing each element separated by a space.

### C Source Code

```c
//Task1
#include<stdio.h>

int main()
{
    int num[5]={1,2,3,4,5};
    printf("The array elements are:\n");
    for (int i=0; i<=4; i++){
        printf("%d ", num[i]);
    }
}

```



### Execution Output

```text
The array elements are:
1 2 3 4 5

```



---

## Task 02: Array Input and Reverse Traversal

### Description

Reads eight integer values into a one-dimensional array `num[8]` from standard input and prints them in reverse order. The first `for` loop populates the array sequentially from index `0` to `7`, while the second `for` loop decrements from index `7` down to `0` to display the reversed elements.

### C Source Code

```c
//Task2
#include<stdio.h>

int main()
{
    int num[8];
    printf("Enter eight elements for the array:\n");

    //takes input
    for (int i=0; i<=7; i++){
        scanf("%d", &num[i]);
    }

    //reverse input
    printf("The reversed array is:\n");
    for (int i=7; i>=0; i--){
        printf("%d ", num[i]);
    }
}

```



### Execution Output

```text
Enter eight elements for the array:
1 2 3 4 5 6 7 8
The reversed array is:
8 7 6 5 4 3 2 1

```



---

## Task 03: Variable-Length Array Summation

### Description

Calculates the sum of all elements in a dynamically sized one-dimensional array. The program prompts the user for the array size `n`, declares a variable-length array `num[n]`, reads `n` integer inputs via a `for` loop, and accumulates their total into `sum` using a second loop.

### C Source Code

```c
//Task3
#include<stdio.h>

int main()
{
    int n;
    printf("Enter array size:\n");
    scanf("%d", &n);

    int num[n];//assigns that number to array size

    printf("Now enter %d values for the array:\n", n);
    for (int i=0; i<n; i++){
        scanf("%d", &num[i]);
    }

    int sum=0;
    for (int i=0; i<n; i++){
        sum += num[i];
    }
    printf("Sum: %d", sum);
}

```



### Execution Output

```text
Enter array size:
3
Now enter 3 values for the array:
1 2 3
Sum: 6

```



---

## Task 04: Passing Arrays to Functions (In-Place Element Modification)

### Description

Demonstrates passing a one-dimensional array to a user-defined function `void add(int num[], int size)`. After reading `n` integers into `num[n]`, `main()` passes the array and its size to `add()`, which modifies each element in-place by adding `22` (`num[i] += 22`) and prints the updated array elements.

### C Source Code

```c
void add(int num[], int size);

int main()
{
    int n;
    printf("Enter array size:\n");
    scanf("%d", &n);
    printf("\n");

    int num[n];//assigns that number to array size

    printf("Now enter %d values for the array:\n", n);
    for (int i=0; i<n; i++){
        scanf("%d", &num[i]);
    }
    printf("\n");

    add(num, n);
}

void add(int num[], int size) {
    for (int i = 0; i < size; i++) {//size = n (input number)
        num[i] += 22; // Adds 22 to each element
    }

    printf("Result after adding 22 to each array element:\n");
    for (int i=0; i<size; i++){
        printf("Element %d: %d\n", i+1, num[i]);
    }
}

```



### Execution Output

```text
Enter array size:
6

Now enter 6 values for the array:
0 1 2 3 4 5

Result after adding 22 to each array element:
Element 1: 22
Element 2: 23
Element 3: 24
Element 4: 25
Element 5: 26
Element 6: 27

```



---

## Task 05: Two-Dimensional Array (Matrix) Input and Display

### Description

Demonstrates the declaration, population, and traversal of a two-dimensional variable-length array `num[row][col]`. The program reads user-defined `row` and `col` dimensions, uses nested `for` loops to populate each matrix cell `num[i][j]`, and iterates through the 2D array again to print all stored elements.

### C Source Code

```c
int main()
{
    int row, col;
    printf("Enter row size of an array:\n");
    scanf("%d", &row);
    printf("\n");

    printf("Enter column size of an array:\n");
    scanf("%d", &col);
    printf("\n");

    int num[row][col];//assigns that number to array size

    printf("Now enter %d(row) and %d(col) values for the array:\n", row, col);
    for (int i=0; i<row; i++){
        for (int j=0; j<col; j++){
            scanf("%d", &num[i][j]);
        }
    }
    printf("\n");

    printf("Array elements:\n");
    for (int i=0; i<row; i++){
        for (int j=0; j<col; j++){
            printf("%d ", num[i][j]);
        }
    }
}

```



### Execution Output

```text
Enter row size of an array:
2

Enter column size of an array:
2

Now enter 2(row) and 2(col) values for the array:
1 2
3 4
Array elements:
1 2 3 4

```
