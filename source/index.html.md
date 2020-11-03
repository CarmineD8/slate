---
title: Coding Playground

language_tabs: # must be one of https://git.io/vQNgJ
  - cpp
  - c

toc_footers:
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>
  - <a>Logo made by Diesmo16</a>
includes:
  

search: true

code_clipboard: true
---

# Introduction

Welcome to the Computer Science Playground! Learn to code with our beginner-friendly tutorials and examples. Read tutorials, try examples, write programs, and learn to code.


# Examples

## Introduction

### [E0] "Hello, World!" Program 

```c
#include <stdio.h>

int main() {
   // printf() displays the string inside quotation
   printf("Hello, World!");
   return 0;
}
```

```cpp
#include <iostream>

int main() {
  // displays the string inside quotation
  std::cout << "Hello, World!";
  return 0;
}
```

> The above command returns:

```shell
Hello, World!
```


[E0]
In this example, you will learn to print "Hello, World!" on the screen in C programming. 
To understand this example, you should have the knowledge of the following C programming topics:

* C Input Output (I/O)

How "Hello, World!" program works?


* `// Your First C++ Program`
  In C++, any line starting with `//` is a comment. Comments are intended for the person reading the code to better understand the functionality of the program. It is completely ignored by the C++ compiler.
* `#include <iostream>`
  The `#include` is a preprocessor directive used to include files in our program. The above code is including the contents of the iostream file.
  This allows us to use cout in our program to print output on the screen.
  For now, just remember that we need to use `#include <iostream>` to use cout that allows us to print output on the screen.
* `int main() {...}`
  A valid C++ program must have the `main()` function. The curly braces indicate the start and the end of the function.
  The execution of code beings from this function.
* `std::cout << "Hello World!";`
  `std::cout` prints the content inside the quotation marks. It must be followed by `<<` followed by the format string. In our example, "Hello World!" is the format string.
  Note: `;` is used to indicate the end of a statement.
* `return 0;`
  The `return 0;` statement is the "Exit status" of the program. In simple terms, the program ends with this statement.

<aside class="notice">
<p>C++ code</p>
We must include iostream if we want to use std::cout
</aside>

<br>

### [E0] Program to Print a number and a char (Entered by the User) 

```c
#include <stdio.h>

int main() {   
  int number;
  float real_number;
  char letter;

  printf("Enter an integer: ");  
  // reads and stores input
  scanf("%d", &number);

  printf("Enter a real number: ");  
  // reads and stores input
  scanf("%f", &real_number);

  printf("Enter a char: ");  
  // reads and stores input
  scanf("%c", &letter);

  // displays output
  printf("You entered: %d", number);
  printf("You entered: %f", real_number);
  printf("You entered: %c", letter);
  
  return 0;
}
```


```cpp
#include <iostream>
 
int main() {   
  int number;
  float realNumber;
  char letter;

  std::cout << "Enter an integer: ";  
  // reads and stores input
  std::cin >> number;

  std::cout << "Enter a real number: ";  
  // reads and stores input
  std::cin >> realNumber;

  std::cout << "Enter a char: ";  
  // reads and stores input
  std::cin >> letter;

  // displays output
  std::cout << "You entered: " << number  << std::endl;
  std::cout << "You entered: " << realNumber << std::endl;
  std::cout << "You entered: " << letter << std::endl;
  
  return 0;
}
```

> The above command returns:

```c
Enter an integer: 25
You entered: 25
```

```cpp
Enter an integer: 25
You entered: 25
```


In this example, the integer entered by the user is stored in a variable and printed on the screen.
To understand this example, you should have the knowledge of the following C programming topics:

  *  C Variables, Constants and Literals
  *  C Data Types
  *  C Input Output (I/O)

In this program, an integer variable number, a real number variable and a char variable are declared.

(Please, also notice that the variable are not initialized, but it is strongly reccomended to do that.)

Then, the user is asked to enter a value for each declared variable. This value is stored in the respective variable.

`std::cout << "Hello World!";`

`std::cin >> number;`

Finally, the value stored in number is displayed on the screen using `printf()`.

`std::cout << "You entered: " << number  << endl;`

<aside class="notice">
<p>C code</p>

All function and variable names are lowercase, with underscores as word separators where needed for clarity.
</aside>

<aside class="notice">
<p>C code</p>

Global variables are named with a <code>g_</code> prefix.
</aside>


<aside class="notice">
<p>C++ code</p>

Use CamelCase for all names. Start names (functions, variables) with a lowercase letter. You may use an all-lowercase name with underscores if your class closely resembles an external construct (e.g., a standard library construct) named that way.
</aside>

<br>


### [E1] Program to Print a number and multiply by 2

```c
#include <stdio.h>

int main() {   
  int number = 0;
  int result = 0;

  printf("Enter an integer: ");  
  // reads and stores input
  scanf("%d", &number);

  // multiply by two
  result = number * 2; 

  // displays output
  printf("You entered:: %d", number);
  printf("The result is: %d", result);
  
  return 0;
}
```


```cpp
#include <iostream>
 

int main() {   
  int number = 0;
  int result = 0;

  std::cout << "Enter an integer: ";  
  // reads and stores input
  std::cin >> number;

  // multiply by two
  result = number * 2; 

  // displays output
  std::cout << "You entered: " << number  << std::endl;
  std::cout << "The result is: " << result << std::endl;
  
  return 0;
}
```

> The above command returns:

```c
You entered: 4
The result is: 8
```

```cpp
You entered: 4
The result is: 8
```

In this example, the integer entered by the user is stored in a variable, multiply by 2 and printed on the screen.
To understand this example, you should have the knowledge of the following C programming topics:

  *  C Variables, Constants and Literals
  *  C Data Types
  *  C Input Output (I/O)

In this program, two integer variable numbers are declared and initialized to zero.

Then, the user is asked to enter an integer value. This value is stored in the respective variable, multiply by two and stored in a second variable.

`result = number * 2 ; `

Finally, the value stored in result is displayed on the screen.

<aside class="success">
<p>Best practice: Initialize your variables upon creation.</p>
When you declare a variable you specify a region of memory to hold a certain type of data. But just a declaration, writes nothing to that memory region. If the variable is read prior to being written, a value will be returned: whatever that part of memory held already, even if from other programs. In other words garbage.
</aside>
  
  
<br>


### [E1] Program to Add Two Integers

```c
#include <stdio.h>
int main() {    

  int number1 = 0;
  int number2 = 0;
  int sum = 0;
  
  
  printf("Enter two integers: ");
  scanf("%d %d", &number1, &number2);

  // calculating sum
  sum = number1 + number2;      
  
  printf("%d + %d = %d", number1, number2, sum);
  return 0;
}
```


```cpp
#include <iostream>

int main()
{
  int number1 = 0;
  int number2 = 0;
  int sum = 0;
  
  std::cout << "Enter two integers: ";
  std::cin >> number1 >> number2;

  // sum of two numbers in stored in variable sum
  sum = number1 + number2;

  // Prints sum 
  std::cout << number1 << " + " <<  number2 << " = " << sum;     

  return 0;
}
```

> The above command returns:

```c
Enter two integers: 4
5
4 + 5 = 9
```

```cpp
Enter two integers: 4
5
4 + 5 = 9
```

In this example, the user is asked to enter two integers. Then, the sum of these two integers is calculated and displayed on the screen.
To understand this example, you should have the knowledge of the following C programming topics:

  *  C Variables, Constants and Literals
  *  C Data Types
  *  C Input Output (I/O)
  *  C Programming Operators

In this program, the user is asked to enter two integers. These two integers are stored in variables `number1` and `number2` respectively.
```
printf("Enter two integers: ");
scanf("%d %d", &number1, &number2);
```
Then, these two numbers are added using the + operator, and the result is stored in the `sum` variable.

`sum = number1 + number2;`


Finally, the `cout` function is used to display the sum of numbers.

`std::cout << number1 << " + " <<  number2 << " = " << sum;`

<aside class="warning">
One of the most common mistakes that new programmers make is to confuse the assignment operator (=) with the equality operator (==). Assignment (=) is used to assign a value to a variable. Equality (==) is used to test whether two operands are equal in value.
</aside>
  
  
<br>

### [E1] Program to Compute the average of Two Integers

```c
#include <stdio.h>
int main() {    

  int number1 = 0;
  int number2 = 0;
  int sum = 0;
  int average = 0;
  
  
  printf("Enter two integers: ");
  scanf("%d %d", &number1, &number2);

  // calculating sum
  sum = number1 + number2; 

  // calculating average
  average = sum/2;     
  
  printf("The average is: %d", average);
  return 0;
}
```


```cpp
#include <iostream>

int main()
{
  int number1 = 0;
  int number2 = 0;
  int sum = 0;
  int average = 0;
  
  std::cout << "Enter two integers: ";
  std::cin >> number1 >> number2;

  // sum of two numbers in stored in variable sum
  sum = number1 + number2;

  average = sum / 2;

  // Prints sum 
  std::cout << " The average is: " << sum;     

  return 0;
}
```

> The above command returns:

```c
The average is: 4
```

```cpp
The average is: 4
```

In this example, the user is asked to enter two integers. Then, the average of these two integers is calculated and displayed on the screen.
To understand this example, you should have the knowledge of the following C programming topics:

  *  C Variables, Constants and Literals
  *  C Data Types
  *  C Input Output (I/O)
  *  C Programming Operators

In this program, the user is asked to enter two integers. These two integers are stored in variables `number1` and `number2` respectively.
```
printf("Enter two integers: ");
scanf("%d %d", &number1, &number2);
```
Then, these two numbers are added using the + operator, and the result is stored in the `sum` variable.

`sum = number1 + number2;`

Then the average is computed and stored in the `average` variable.


Finally, the result is displayed.  
  
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

### [E1] Program to convert Lowercase character to uppercase

```c
#include <stdio.h>
int main() {    

  char character = 0;
  
  printf("Enter a character in lowercase: ");
  scanf("%c", &character);

  // transform the character
  character = character - 32;   
  
  printf("The character in uppercase is: %c", character);
  return 0;
}
```


```cpp
#include <iostream>

int main()
{
  char character = 0;
  
  std::cout << "Enter a character in lowercase: ";
  std::cin >> character;

  // transform the character
  character = character - 32;

  // Prints converted char 
  std::cout << " The character in uppercase is: " << character;     

  return 0;
}
```

> The above command returns:

```c
Enter a character in lowercase: a
The character in uppercase is: A
```

```cpp
Enter a character in lowercase: a
The character in uppercase is: A
```

The program converts lowercase character to uppercase.

In this example, the user is asked to enter a char variable. 

Then the character is converted by subtracting 32 from the ASCII value of input char.

Finally, the result is displayed.

<aside class="notice">
<p>ASCII value of lowercase char a to z ranges from 97 to 122</p>
<p>ASCII value of uppercase char A to Z ranges from 65 to 92</p>
</aside>

<aside class="notice">
<p>C++ code</p>

<p>The <code>toupper()</code> function returns a uppercase version of ch if it exists. Otherwise it returns ch.</p>

<p>It is defined in <code>cctype</code> header file.</p>
</aside>


## Decision Making and Loops
In progress section...

## Functions
In progress section...

# Bash Basic Commands
* `ls` --> it shows the list of files in the current directory
* `ls -a` --> it shows the list of files in the current directory, also the hidden ones
* `cd nameDir` --> Change directory, changes the current path and enter in the specified directory
* `.` --> current directory 
* `..` --> Previous directory
* `touch nameFile` --> it creates a file named nameFile
* `rm nameFile` --> delete nameFile
* `rmdir nameDir` --> delete nameDir (only if the directory is empty)
* `rm -r nameDir` --> delete the directory and all the sub files in it
* `nano nameFile` --> open (or it creates if it doesn't exist) nameFile with an editor from bash. Use ctrl + x to save and exit


    
# Compiler

> To compile, use this code:

```shell
g++ -o HelloWorld helloworld.cpp 
./HelloWorld
```

A compiler is a computer program that transforms source code written in a high-level programming language (e.g., c, c++) into a lower level language (e.g., assembly language, object code, or machine code) to create an executable program. 

The compilation of a C++ program involves three steps:

1. Preprocessing: the preprocessor takes a C++ source code file and deals with the `#includes`, `#defines` and other preprocessor directives. The output of this step is a "pure" C++ file without pre-processor directives.

2. Compilation: the compiler takes the pre-processor's output and produces an object file from it.

3. Linking: the linker takes the object files produced by the compiler and produces either a library or an executable file.

In order to try this we have to write an hello world program (see, example section), save it, and go to the directory where the file has been saved. Once there we can compile the program!

How to install a compiler:

 1. Open the bash and run the following commands
 2. `sudo apt update`
 3. `sudo apt install build-essential`

<aside class="notice">
C++ source files have a <code>.cpp</code> extension, C source files <code>.c</code>, and headers for both use <code>.h</code>.
</aside>


If you want to try some examples, you can also try an online compiler, such as [programiz compiler](https://www.programiz.com/c-programming/online-compiler/).


# FAQ 

