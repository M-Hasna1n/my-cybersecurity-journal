# LAB 09 & 10: POINTERS AND STRING HANDLING IN C

---

# LAB 09: POINTERS IN C

## 🎯 Objectives
* Understand memory addresses and pointer variables.
* Learn pointer declaration, initialization (`&`), and dereferencing (`*`).

---

## Lab 09 - Task 01: Pointer Address Access

### Description
Demonstrates pointer initialization and memory address retrieval. An integer variable `age` is initialized to `19`, and a pointer `ptr` stores its memory address (`&age`). The program outputs the hexadecimal memory address using the `%p` format specifier.

### C Source Code
```c
//Task1
#include<stdio.h>

int main(){
    int age = 19;
    int *ptr = &age;

    printf("Variable \'age\' address is: %p", ptr);
}
```

### Execution Output
```text
Variable 'age' address is: 000000000065FE14
```

---

## Lab 09 - Task 02: Dereferencing Pointers

### Description
Shows how to read a value from standard input into a variable and access it indirectly via a pointer. The program prompts for an integer value, stores it in `age`, and uses the dereference operator (`*ptr`) to print the stored value.

### C Source Code
```c
//Task2
#include<stdio.h>

int main(){
    int age;
    int *ptr = &age;

    printf("Enter an integer value: ");
    scanf("%d", &age);

    //%d for value, %p for address
    printf("Value at variable \'age\' is: %d", *ptr);
}
```

### Execution Output
```text
Enter an integer value: 19
Value at variable 'age' is: 19
```

---
---

# LAB 10: STRING HANDLING IN C

## 🎯 Objectives
* Understand string library functions in C.
* Implement lexicographical string comparison using `strcmp()`.

---

## Lab 10 - Task 01: Lexicographical String Comparison (`strcmp`)

### Description
Demonstrates string comparison using the standard library function `strcmp()` from `<string.h>`. The program compares two character arrays (`str1 = "apple"` and `str2 = "banana"`) and evaluates the return value using conditional branches (`== 0`, `< 0`, `> 0`) to determine lexicographical ordering.

### C Source Code
```c
#include<stdio.h>
#include<string.h>//includes strcmp()

int main()
{
    char str1[]= "apple";
    char str2[]= "banana";

    int result= strcmp(str1, str2);

    if (result==0)
        printf("Both strings are equal.");

    else if (result<0)
        printf("str1 comes before str2.");

    else
        printf("str1 comes after str2.");
}
```

### Execution Output
```text
str1 comes before str2.
```

> *Note: Console output images and terminal screenshots for all tasks are stored locally in the lab submission workspace.*
