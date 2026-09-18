Programming Fundamentals — Lab 02

## Task 1 & 2: Data Types, Formatting, and Escape Sequences

### Description
This program demonstrates basic variable declaration and initialization across standard C data types (int, float, char). It prints these values using format specifiers (%d, %.1f, %c) and displays multi-line text blocks using escape sequences (\n)

### Code
```c
  //Task 1
#include <stdio.h>
#include <conio.h>

int main()
{
    int num = 5;
    float val = 2.5;
    char ch = 'H';

    clrscr();

    printf("Integer: %d\n", num);
    printf("Float: %.1f\n", val);
    printf("Character: %c\n", ch);

    //Task 2
    printf("This is my first program.\nMy name is hasnain.\nI am CS student.");

    getch();
    return 0;
}
```

---

## Task 3: Interactive Sequential Input and Immediate Display

### Description
This task demonstrates reading sequential user inputs (`age`, `height`, `weight`) using `scanf()`[cite: 3]. Each value is immediately printed back to the terminal prompt after it is entered[cite: 3, 4].

### Code
```c
//Task 3
#include <stdio.h>
#include <conio.h>

int main()
{
    int age;
    float height, weight;

    clrscr();

    printf("Enter your age.\n");
    scanf("%d", &age);
    printf("Your age is %d\n", age);

    printf("Enter your height.\n");
    scanf("%f", &height);
    printf("Your height is %.1f\n", height);

    printf("Enter your weight.\n");
    scanf("%f", &weight);
    printf("Your weight is %.1f\n", weight);

    getch();
    return 0;
}
```

---

## Task 4: Grouped Input Parsing and Batch Output

### Description
This task demonstrates collecting all user inputs (`age`, `height`, `weight`) first before executing output statements[cite: 5]. All formatted output values are displayed together in a single block at the end[cite: 5, 6].

### Code
```c
//Task 04
#include <stdio.h>
#include <conio.h>

int main()
{
    int age;
    float height, weight;

    clrscr();

    printf("Enter your age.\n");
    scanf("%d", &age);

    printf("Enter your height.\n");
    scanf("%f", &height);

    printf("Enter your weight.\n");
    scanf("%f", &weight);

    printf("Your age is %d\n", age);
    printf("Your height is %.1f\n", height);
    printf("Your weight is %.1f\n", weight);

    getch();
    return 0;
}
```

---

## Task 5: Integer and Float Precision Formatting

### Description
This task focuses on accepting integer (`age`) and floating-point (`marks`) values from standard input[cite: 7]. It uses `%.1f` to format floating-point numbers to one decimal place[cite: 7, 8].

### Code
```c
//Task 5
#include <stdio.h>
#include <conio.h>

int main()
{
    int age;
    float marks;

    clrscr();

    printf("Enter your age:\n");
    scanf("%d", &age);
    printf("Your age is %d\n", age);

    printf("Enter your marks:\n");
    scanf("%f", &marks);
    printf("Your marks are %.1f\n", marks);

    getch();
    return 0;
}
```

---

## Task 6: Multi-Variable Input Processing

### Description
This program demonstrates reading multiple variables of different data types simultaneously in a single `scanf("%d %f")` call[cite: 9, 10].

### Code
```c
//Task 6
#include <stdio.h>
#include <conio.h>

int main()
{
    int num;
    float val;

    clrscr();

    printf("Enter an integer and float: ");
    scanf("%d %f", &num, &val);
    printf("Integer: %d\n , Float: %.2f\n", num, val);

    getch();
    return 0;
}
```

---

## Task 7: Character Input and Display

### Description
This task demonstrates character I/O in C[cite: 11, 12]. It prompts the user for a single character input using `scanf("%c", &ch)` and prints the entered character back to the console[cite: 11, 12].

### Code
```c
//Task 7
#include <stdio.h>
#include <conio.h>

int main()
{
    char ch;

    clrscr();

    printf("Enter any character:");
    scanf("%c", &ch);
    printf("You entered %c", ch);

    getch();
    return 0;
}
```

---

## Key Takeaways

* **Data Types & Format Specifiers:** Mastered using specifiers like `%d` for integers, `%f` / `%.1f` / `%.2f` for floats with controlled decimal precision, and `%c` for individual characters.
* **Immediate vs. Batch Input Handling:** Explored the structural differences between displaying outputs immediately after each prompt versus storing inputs first and printing batch outputs together.
* **Multi-Input `scanf()` Operations:** Learned how to capture multiple variables of distinct types (e.g., `int` and `float`) in a single input function call using `scanf("%d %f", &num, &val)`.
* **Console Operations in Turbo C++:** Reinforced console window initialization using `clrscr()` to clear prior output screens and `getch()` to pause console execution until user interaction.
