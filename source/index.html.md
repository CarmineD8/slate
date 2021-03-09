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

# Tutorial 

Section in progress...


# Examples

## Practical examples - 1

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


### [E1][A1] Program to Print a number and multiply by 2

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

**Assignement 1**: *Write a C++ program that ask the user to enter an integer value, multiplies it by 2 and displays the result*.

**Solution**:
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


### [E1][A2] Program to Add Two Integers

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

**Assignment 2**: *Write a C++ program that ask the user to enter two integer values, sums them and displays the result*.

**Solution**:
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

### [E1][A3] Program to Compute the average of Two Integers

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
  std::cout << " The average is: " << average << std::endl;     

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

**Assignment 3**: *Write a C++ program that ask the user to enter two real values, makes the average of them and displays the result*.

**Solution**:
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

### [E1][A4] Program to convert Lowercase character to uppercase

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
  std::cout << " The character in uppercase is: " << character << std::endl;     

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

**Assignment 4**: *Write a C++ program that ask the user to enter a lowercase char, and displays the same char in uppercase as result*.

**Solution**:
The program converts lowercase character to uppercase.

In this example, the user is asked to enter a char variable. 

Then the character is converted by subtracting 32 from the ASCII value of input char.

Finally, the result is displayed.

<aside class="notice">
<p>ASCII value of lowercase char a to z ranges from 97 to 122</p>
<p>ASCII value of uppercase char A to Z ranges from 65 to 90</p>
</aside>

<aside class="notice">
<p>C++ code</p>

<p>The <code>toupper()</code> function returns a uppercase version of ch if it exists. Otherwise it returns ch.</p>

<p>It is defined in <code>cctype</code> header file.</p>
</aside>


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

### [E1][A5] Program to compute the area of a circle

```c
#include <stdio.h>
int main() {    

  float radius, area;

  printf("Enter the radius of circle\n");

  scanf("%f", &radius);

  area = 3.14 * radius * radius;

  printf("Area of the circle = %.1f\n", area);  // printing upto one decimal places

  return 0;
}
```


```cpp
#include <iostream>

int main()
{
  float radius, area;

  std::cout << "Enter the radius of circle : ";
  std::cin >> radius;

  area = 3.14 * radius * radius;

  std::cout << "Area of circle with radius " << radius << " is " << area << std::endl;

  return 0;
}
```

> The above command returns:

```c
Enter the radius of circle : 5
Area of the circle = 78.5
```

```cpp
Enter the radius of circle : 5
Area of circle with radius 5 is 78.5
```

**Assignment 5**: *Write a C++ program that ask the user to enter the value of the radiud of a circle, computes the area and displays the result*.

**Solution**:
The program computes area of circle. The program takes radius of the circle as an input from the user, calculates the area of the circle and outputs it on the screen.
In this example, the user is asked to enter a float variable. 

Then the radius is used to compute the area of the circle.

Finally, the result is displayed.

<aside class="notice">
<p>C++ code</p>
<p>You can set the decimal precision to be used to format floating-point values on output operations by using <code>std::setprecision</code>.</p>
<p>This manipulator is declared in header <code>iomanip</code>.</p>
</aside>

## Practical examples - 2

To understand these examples, you should have the knowledge of the following C++ programming topics:

*  C++ Variables, Constants and Literals
*  C++ Data Types
*  C++ Input Output (I/O)
*  C++ Programming Operators
*  C++ Functions
*  User-defined Functions in C++



### [E2][A1] Time converter 

 ```c
#include <stdio.h>
int main() {    

  
}
```


```cpp
#include <iostream>

int main() {
  // Declaration and variable init
  int seconds = 0;
  int minutes = 0;
  int hour = 0;
  int day = 0;
  int weeks = 0;
  // 
  std::cout << "Enter an integer value to convert: ";
  std::cin >> seconds;
  
  weeks = seconds / (24 * 3600 * 7);
  
  day = seconds / (24 * 3600); 

  hour = seconds / 3600; 

  minutes = seconds / 60 ; 
    
  std::cout << weeks << " " << "weeks \n" << day << " " << "days \n" << hour  
        << " " << "hours\n" << minutes << " " 
        << "minutes\n" << seconds << " " 
        << "seconds\n "  << std::endl; 

  return 0;
}
```

> The above command returns:

```c

```

```cpp
Enter an integer value to convert: 604700
0 weeks 
6 days 
167 hours
10078 minutes
604700 seconds
```

**Assignement 1**: *Write a C++ program that ask the user to insert an integer that refers to a time duration expressed in seconds. Then the program computes the same duration in terms of number of weeks, number of days, hours, minutes and seconds.*

**Solution**:
The program replaces a time duration expressed in second in number of weeks, days, hours, minutes and seconds.
In this example, the user is asked to enter a integer variable. This variable represents a duration expressed in seconds.

Then the variable is converted in weeks (there are 7 * 24 * 60 * 60 seconds in a week), days (there are 24 * 60 * 60 seconds in a day), hours (there are * 60 * 60 seconds in one hour) and minutes (there are 60 seconds in a minute).

Note that here, we are just expressing a value in seconds as weeks, days, etc.. So, 1 second is 0 weeks, 0 days, 0 hours, 0 mins and 1 second. 
We are not converting a time duration in another format (go to next example).

Finally, the result is displayed.


But let's see the next example...




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
 
  
   
    
     
 
  
    


### [E2] Time converter - variation 1 

```c
#include <stdio.h>
int main() {    

  
}
```


```cpp
#include <iostream>

int main() {
  // Declaration and variable init
  int seconds = 0;
  int minutes = 0;
  int hour = 0;
  int day = 0;
  int weeks = 0;
  // 
  std::cout << "Enter an integer value to convert: ";
  std::cin >> seconds;
  
  weeks = seconds / (24 * 3600 * 7);
  
  seconds = seconds % (24 * 3600 * 7);
  day = seconds / (24 * 3600); 

  seconds = seconds % (24 * 3600); 
  hour = seconds / 3600; 

  seconds %= 3600; 
  minutes = seconds / 60 ; 

  seconds %= 60; 
  seconds = seconds; 
    
  std::cout << weeks << " " << "weeks \n" << day << " " << "days \n" << hour  
        << " " << "hours\n" << minutes << " " 
        << "minutes\n" << seconds << " " 
        << "seconds\n "  << std::endl; 

  return 0;
}
```

> The above command returns:

```c

```

```cpp
Enter an integer value to convert: 604700
0 weeks 
6 days 
23 hours
58 minutes
20 seconds




```




The program converts a time duration expressed in second in number of weeks, days, hours, minutes and seconds.

In this example, the user is asked to enter a integer variable. This variable represents a duration expressed in seconds.

Here we are converting seconds to a format weeks:days:hours:minutes:seconds.

Try out different time duration to understand how it works.

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
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
  
   
    
     
 
  
   
    

### [E2] Time converter - variation 2

```c
#include <stdio.h>
int main() {    

  
}
```


```cpp
#include <iostream>

void convertSeconds(int seconds){
    
    int minutes = 0;
    int hour = 0;
    int day = 0;
    int weeks = 0;
    
    weeks = seconds / (24 * 3600 * 7);
    
    seconds = seconds % (24 * 3600 * 7);
    day = seconds / (24 * 3600); 
  
    seconds = seconds % (24 * 3600); 
    hour = seconds / 3600; 
  
    seconds %= 3600; 
    minutes = seconds / 60 ; 
  
    seconds %= 60; 
    seconds = seconds; 
      
    std::cout << weeks << " " << "weeks \n" << day << " " << "days \n" << hour  
         << " " << "hours\n" << minutes << " " 
         << "minutes\n" << seconds << " " 
         << "seconds\n "  << std::endl; 
}

int main() {
    // Declaration and variable init
    int seconds = 0;
    // 
    std::cout << "Enter an integer value to convert: ";
    std::cin >> seconds;
    
    convertSeconds(seconds);
    
    return 0;
}
```

> The above command returns:

```c

```

```cpp
Enter an integer value to convert: 604700
0 weeks 
6 days 
23 hours
58 minutes
20 seconds



```



The program converts a time duration expressed in second in number of weeks, days, hours, minutes and seconds.

In this example, the user is asked to enter a integer variable. This variable represents a duration expressed in seconds.

Here we are converting seconds to a format weeks:days:hours:minutes:seconds.

This version exploits the use of a custom defined function. We can define a function that takes in input some arguments and gives out something.
In this example the functions takes an integer value, converts it into weeks, days, hours, minutes and seconds and display the result.

Then in the main function, we can call this function. We have to pass to the function an integer number. 

Finally, the program returns.

You can also try to make another function to print out the result.  



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
<br>
<br>
<br>
<br>
<br>
<br>
<br>
  
   
  
  
   


### [E2][A2] Compute area of triangle 

```cpp
#include<iostream>
#include<cmath>

int main()
{
	float a = 0;
	float b = 0;
	float c = 0;
	float p = 0;
	float Area = 0;
	
	std::cout << "Enter three sides of triangle : ";
	std::cin >> a >> b >> c;
	
	p=(a+b+c)/2;
	Area=sqrt(p*(p-a)*(p-b)*(p-c));
	
	std::cout<<"Area of triangle is : "<< Area << std::endl;;
	
	return 0;
}

```

> The above command returns:

```c

```

```cpp
Enter three sides of triangle : 5 7 8
Area of triangle is : 17.32050

``` 

**Assignement 2**: *Write a program to compute area of triangle. Sides a, b, and c are input by user. Then the program computes the area and displays the result.*
 Note that the area can be computed as `A = sqrt(p*(p-a)*(p-b)*(p-c))` where `p=(a+b+c)/2`. Moreover to compute the square root you can use the library function `sqrt` available in `cmath`.



**Solution**:
 In this example we compute the area of a triangle. To do that, the user is asked to insert three real numbers.
 We save these values in three different float variable.
 Then, the programs computes the area of the triangle and displays the result.

 We can also decide to create a custum function to compute the area and call it in the main function. Try this!

 <aside class="notice">
<p>C++ code</p>
<p>You can explor Standard C++ library function [here](http://www.cplusplus.com/reference/)</p>
</aside>

<aside class="notice">
<p>C++ code</p>
<p>You can use a function defined in a library after importing it with <code>#include <cmath></code></p>
</aside>
 
  
   
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



### [E2][A3] Use increment and decrement operators 

```cpp
int main()
{
	int number = 0;
	int pre = 0;
	int post = 0;
	
	
	std::cout << "Enter an integer: ";
	std::cin >> number;
	
	//pre = number - 1;
	//pre = number--;
	pre = --number;
	
	//post = number + 1;
	//post = number++;
	post = ++ ++number;
	
	std::cout<<"The number is : "<< number << std::endl;
	std::cout<<"Pre is : "<< pre << std::endl;
	std::cout<<"Post is : "<< post << std::endl;
	
	return 0;
}
```

> The above command returns:

```c

```

```cpp
The number is: 8
Pre is: 7
Post is: 9

``` 

**Assignement 3**: *Write a C++ program that ask the user to insert an integer and displays the previous number and the next one. Use increment ++ and decrements -- operators.*

**Solution**:
In this example, the program asks for an integer number. The we use pre-decrement operator to compute the previous number, that returns the value contained in number variable after it has been incremented.
Then we concatenate two pre-increment operator to compute the next value. 
Try by yourself the different use of these operators.

<aside class="notice">
<p>C++ code</p>
<p>Pre-increment and pre-decrement operators increments or decrements the value of the object and returns a reference to the result.</p>
</aside>

<aside class="notice">
<p>C++ code</p>
<p>Post-increment and post-decrement creates a copy of the object, increments or decrements the value of the object and returns the copy from before the increment or decrement.</p>
</aside>

 
  
   
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
  



### [E2][A4] Check numbers 

```cpp
#include<iostream>

int main()
{
	int a = 0;
	int b = 0;
	int result = -1; 
	
	
	std::cout << "Enter two integers: ";
	std::cin >> a >> b;
	
	if (a == b){
	    result = 0;
	} else {
	    result = 1;
	}
	
	std::cout<<"Result is : "<< result << std::endl;
	
	return 0;
}
```

> The above command returns:

```c

```

```cpp
Enter two integers: 
1 2
Result is: 1

``` 

**Assignement 4**: *Write a C++ program that ask the user to insert two integers and display 0 if the two numbers are equal, or a positive number if the two are different.*

**Solution**:
In this example, the program asks the user to insert two integers. Then the program checks if the two numbers are equal. We use a comparison operator  `==` that returns true if the left value is equal to the right value, false otherwise.

<aside class="notice">
<p>C++ code</p>
<p>You can use also XOR operator (^).  XOR of two numbers is 0 if the numbers are same, otherwise non-zero.</p>
</aside>

 
  

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
<br>
  
   
 
   
   



### [E2][A5] Swap numbers 

 ```cpp

#include <iostream>

int main()
{
    int a = 0, b = 0, temp = 0;
    
    std::cout << "Enter two integers: "<< std::endl;
	std::cin >> a >> b;

    std::cout << "\nBefore swapping." << std::endl;
    std::cout << "a = " << a << ", b = " << b << std::endl;

    temp = a;
    a = b;
    b = temp;

    // method 2: we can use just two variables
    // a = a + b;
    // b = a - b;
    // a = a - b;

    std::cout << "\nAfter swapping." << std::endl;
    std::cout << "a = " << a << ", b = " << b << std::endl;

    return 0;
}

```

> The above command returns:

```c

```

```cpp
Enter two integers: 
1 2

Before swapping.
a = 1, b = 2

After swapping.
a = 2, b = 1

``` 

**Assignement 5**: *Write a C++ program that asks the user to insert two integers, swaps them and shows the result.*

**Solution**:
This example contains two different techniques to swap numbers in C programming. The first program uses temporary variable to swap numbers, whereas the second program doesn't use temporary variables.
To perform swapping in above example, three variables are used.

The contents of the first variable is copied into the temp variable. Then, the contents of second variable is copied to the first variable.

Finally, the contents of the temp variable is copied back to the second variable which completes the swapping process.

You can also perform swapping using only two variables as below.

The output of this program is the same as the first program above.

Let us see how this program works:

1. Initially, a = 1 and b = 2.
2. Then, we add a and b and store it in a with the code a = a + b. This means a = 1 + 2. So, a = 3 now.
3. Then we use the code b = a - b. This means b = 3 - 2. So, b = 1 now.
4. Again, we use the code a = a - b. This means a = 3 - 1. So finally, a = 2.

 
 
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
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
 
  
  
    
 
  


### [E2][A6] Use relational and logical operators 

```cpp
#include <iostream>

int main()
{
    int rows = 0, columns = 0;
    
    std::cout << "Enter two integers: "<< std::endl;
	std::cin >> rows >> columns;
    // || (rows == 1 && columns == 1)
    if (rows == 1 || columns == 1 ){
        std::cout << "Result: " << 0 << std::endl;
    }

    return 0;
}

```

> The above command returns:

```c

```

```cpp
Enter two integers: 
1 2
Result: 0

``` 

**Assignement 6**: *Write a C++ program that asks the user to insert two integers representing the number of rows and the number of columns of a matrix. The program displays 0 if the table has only one row, or if it as only one column or if it has just one element.* 

**Solution**:

in this example the user gives in input two integers. The program use logic operators and relational operators to check if the condition holds. 

Operator | Name | Description
-------------- | -------------- | --------------
&& | AND | Returns true if both statements are true
&#8741; | OR | Returns true if both statements are true
! | NOT | Reverse the result, returns false if the result is true 


## Practical examples - 3

To understand these examples, you should have the knowledge of the following C++ programming topics:

*  C++ Variables, Constants and Literals
*  C++ Data Types
*  C++ Input Output (I/O)
*  C++ Programming Operators
*  C++ Functions
*  User-defined Functions in C++
*  C++ if...else, switch case





### [E3][A1]  Quadratic Equation

```cpp
#include <iostream>
#include <cmath>

int main() {

  float a, b, c, x1, x2, discriminant, realPart, imaginaryPart;

  std::cout << "Enter coefficients a, b and c: ";
  std::cin >> a >> b >> c;

  discriminant = b*b - 4*a*c;
  
  if (discriminant > 0) {
    x1 = (-b + sqrt(discriminant)) / (2*a);
    x2 = (-b - sqrt(discriminant)) / (2*a);
    cout << "Roots are real and different." << endl;
    std::cout << "x1 = " << x1 << std::endl;
    std::cout << "x2 = " << x2 << std::endl;
  } 
  else if (discriminant == 0) {
    std::cout << "Roots are real and same." << std::endl;
    x1 = -b/(2*a);
    std::cout << "x1 = x2 =" << x1 << std::endl;
  }
  else {
    realPart = -b/(2*a);
    imaginaryPart =sqrt(-discriminant)/(2*a);
    std::cout << "Roots are complex and different."  << std::endl;
    std::cout << "x1 = " << realPart << "+" << imaginaryPart << "i" << std::endl;
    std::cout << "x2 = " << realPart << "-" << imaginaryPart << "i" << std::endl;
  }

  return 0;
}

```

> The above command returns:

```c

```

```cpp
Enter coefficients a, b and c: 4
5
1
Roots are real and different.
x1 = -0.25
x2 = -1

``` 

**Assignement 1**: *Write a C++ program to compute all roots of a quadratic equation like this `ax^2+bx+c = 0`. The program asks the user to insert three coefficients a,b,c and computes the solutions, both real and complex roots depending upon the discriminant.*



**Solution**:
 This program accepts coefficients of a quadratic equation from the user and displays the roots (both real and complex roots depending upon the discriminant).

 For a quadratic equation `ax2+bx+c = 0` (where a, b and c are coefficients), it's roots is given by following the formula: `(-b +- sqrt(b^2 - 4ac))/ 2a `.

 The term `b2-4ac` is known as the discriminant of a quadratic equation. The discriminant tells the nature of the roots.

  * If discriminant is greater than 0, the roots are real and different.
  * If discriminant is equal to 0, the roots are real and equal.
  * If discriminant is less than 0, the roots are complex and different.

In this program, `sqrt()` library function is used to find the square root of a number. Remember to import `cmath` to use this function. 



 <aside class="notice">

  <p> math.h VS cmath</p>
  The C++ library includes the same definitions as the C language library organized in the same structure of header files, with the following differences:

  1. Each header file has the same name as the C language version but with a "c" prefix and no extension. For example, the C++ equivalent for the C language header file < stdlib.h > is < cstdlib>.

  2. Every element of the library is defined within the std namespace.

</aside>
<aside class="notice">
<p> math.h VS cmath</p>
<p> We recommend to use <code>cmath</code> when writing C++ programs because they are standard C++, meaning you have strong guarantees of what is supported in those headers and how the functions in them work.</p>
</aside>
 
  
   
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
 
  




### [E3][A2] Calculator 

```cpp
# include <iostream>

int main()
{
  char op;
  float num1, num2;

  std::cout << "Enter operation (a + b):";

  std::cin >> num1 >> op >>  num2;

  switch(op)
  {
    case '+':
      std::cout << num1+num2 << std::endl;
      break;

    case '-':
      std::cout << num1-num2 << std::endl;
      break;

    case '*':
      std::cout << num1*num2 << std::endl;
      break;

    case '/':
      if (num2 == 0){
          std::cout << "Error! division per 0" << std::endl;
          break;
      }
      std::cout << num1/num2 << std::endl;
      break;

    default:
      // If the operator is other than +, -, * or /, error message is shown
      std::cout << "Error! operator is not supported";
      break;
  }

  return 0;
}

```

> The above command returns:

```c

```

```cpp
Enter operation (a + b): 2+3
5

``` 

**Assignement 2**: *Write a C++ program that implements a simple calculator. The program asks the user two real number and an operator (+, -, *, /) , then it computes the operation and displays the result. In the case that the operator given by the user is not in the list of accepted operators, the program will show an error message.*

**Solution**:
This program takes an arithmetic operator (+, -, *, /) and two operands from an user and performs the operation on those two operands depending upon the operator entered by user.
This program takes an operator and two operands from user.

The operator is stored in variable op and two operands are stored in num1 and num2 respectively.

Then, `switch...case` statement is used for checking the operator entered by user.

If user enters `+` then, statements for `case: '+'` is executed and program is terminated.

If user enters `-` then, statements for `case: '-'` is executed and program is terminated.

This program works similarly for `*` and `/` operator. But, if the operator doesn't matches any of the four character [ +, -, * and / ], default statement is executed which displays error message.


  
   
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
<br>
<br>

### [E3][A2][v2] Calculator while

```cpp
# include <iostream>

int main()
{
  char op;
  float num1, num2;
  char flag = 'y';
  
  do {

    std::cout << "Enter operation (a + b):";
    std::cin >> num1 >> op >>  num2;

    switch(op)
    {
      case '+':
        std::cout << num1+num2 << std::endl;
        break;

      case '-':
        std::cout << num1-num2 << std::endl;
        break;

      case '*':
        std::cout << num1*num2 << std::endl;
        break;

      case '/':
        if (num2 == 0){
          std::cout << "Error! division per 0" << std::endl;
          break;
        }
        std::cout << num1/num2 << std::endl;
        break;

      default:
        // If the operator is other than +, -, * or /, error message is shown
        std::cout << "Error! operator is not supported";
        break;
    }

    std::cout << "Press y to continue ";
    std::cin >> flag;

  } while (flag == 'y');
  
  std::cout << "Exit...";

  return 0;
}

```

> The above command returns:

```c

```

```cpp
Enter operation (a + b):3+4
7
Press y to continue g
Exit...

``` 

**Assignement 2**: *Write a C++ program that implements a simple calculator. The program asks the user two real number and an operator (+, -, *, /) , then it computes the operation and displays the result. In the case that the operator given by the user is not in the list of accepted operators, the program will show an error message.*

**Solution**:
This program takes an arithmetic operator (+, -, *, /) and two operands from an user and performs the operation on those two operands depending upon the operator entered by user.
This program takes an operator and two operands from user.

The operator is stored in variable op and two operands are stored in num1 and num2 respectively.

Then, `switch...case` statement is used for checking the operator entered by user.

If user enters `+` then, statements for `case: '+'` is executed and program is terminated.

If user enters `-` then, statements for `case: '-'` is executed and program is terminated.

This program works similarly for `*` and `/` operator. But, if the operator doesn't matches any of the four character [ +, -, * and / ], default statement is executed which displays error message.

In this implementation the programkeeps to accepts operations until the user types something different from `y`. There are many other methods to do that, try by yourself!


  
   
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
<br>
<br>
  





 
  


  
   
 
   
   



### [E3][A4] Leap Year

 ```cpp
#include <iostream>
// Function declarations
bool isLeap(int year);
int computeDays(int month, int year);


// Function definitions
bool isLeap(int year)
{
  bool leap = false;
  if (year % 4 == 0)
  {
    if (year % 100 == 0)
    {
      if (year % 400 == 0)
      {
        std::cout << year << " is a leap year.";
        leap = true;
      }
      else
      {
        std::cout << year << " is not a leap year.";
        leap = false;
      }
    }
    else
    {
      std::cout << year << " is a leap year.";
      leap = true;
    }
  }
  else
  {
    std::cout << year << " is not a leap year.";
    leap = false;
  }
  return leap;
}

int computeDays(int month, int year){
  int result = 0;
  switch (month)
    {
    case 4:
    case 6:
    case 9:
    case 11:
    {
      // mesi 30 giorni
      result = 30;
      break;
    }
    case 1:
    case 3:
    case 5:
    case 7:
    case 8:
    case 10:
    case 12:
    {
      // mesi 31 giorni
      result = 31;
      break;
    }
    case 2:
    {
      // mesi 28 giorni
      if (isLeap(year))
        result = 29;
      else
        result = 28;
      break;
    }
    }
  return result;
}

int main() {
  int year;
  int month;

  std::cout << "Enter a year: ";
  std::cin >> year;

  std::cout << "Enter a month: ";
  std::cin >> month;

  int result = computeDays(month, year);

   std::cout << "The result is: " << result << std::endl; 

  return 0;
}


```

> The above command returns:

```c

```

```cpp
Enter a year: 2020
Enter a month: 12
The result is: 31

``` 

**Assignement 4**: *Write a C++ program tha asks the user to insert two integers representing a month and a year and computes the number of days of the given month. Pay attention, remember that February of a leap year has  29 days. A leap year is divisible by 4, with the exception of years also divisible by 100, that are leap only if the are divisible by 400.*

**Solution**:
The program asks the user to enter two integers number. We use two integer variables, `month` and `year` to store these values.

Then the program calls a custum function `computeDays`, which takes two input parameters. 

The `computeDays` function returns an integer corresponding to the number of days in a specified month.

Inside this function a switch case is used to assign to the result variable the right number of days according to the month. There are months with 30, 31 and 28 days. 

Moreover, the program check if the year is leap. 

In this case, if the month is February the days will be set to 29. 

The `isLeap` function takes in input an integer. Then it checks if the number is dividible by 4, by 100 and by 400.

Finally, the program displays the result.

</aside>
<aside class="notice">
<p> Switch case</p>
<p> We can group cases together, but pay attention to the code readability and not to miss any case! </p>
</aside>
 
 
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
<br>
<br>
<br>
  
    
 
  


### [E3][A5] Birthday

```cpp
#include <iostream>

// Questa è una dichiarazione di funzione
// La dichiarazione esprime il nome di una funzione e la relazione in termini di di ingresso/uscita
void computeAge(int currentDay, int currentMonth, int currentYear, int bdayDay, int bdayMonth, int bdayYear);


// // Questa è una definizione di una funzione
/**
 * Funzione che calcola l'età di una persona.
 * La funzione calcola l'età di una persona a partire dalla data corrente e dalla data di nascita.
 * 
 * @param currentDay variabile intera che indica il giorno corrente
 * @param currentMonth variabile intera che indica il mese corrente
 * @param currentYear variabile intera che indica l'anno corrente
 * @param bdayDay variabile intera che indica il giorno del compleanno
 * @param bdayMonth variabile intera che indica il mese corrente
 * @param bdayYear variabile intera che indica l'anno corrente
 *
 */
void computeAge(int currentDay, int currentMonth, int currentYear, int bdayDay, int bdayMonth, int bdayYear)
{
  if (bdayDay > currentDay)
  {
    switch (currentMonth)
    {
      case 4:
      case 6:
      case 9:
      case 11:
      {
        // mesi 30 giorni
        currentDay = currentDay + 30;
        currentMonth = currentMonth - 1;
        break;
      }
      case 1:
      case 3:
      case 5:
      case 7:
      case 8:
      case 10:
      case 12:
    {
      // mesi 31 giorni
      currentDay = currentDay + 31;
      currentMonth = currentMonth - 1;
      break;
    }
    case 2:
    {
      // mesi 28 giorni
      currentDay = currentDay + 28;
      currentMonth = currentMonth - 1;
      break;
    }
    }
  }

  if (bdayMonth > currentMonth)
  {
    currentYear = currentYear - 1;
    currentMonth = currentMonth + 12;
  }

  int giorni = currentDay - bdayDay;
  int mesi = currentMonth - bdayMonth;
  int anni = currentYear - bdayYear;

  if (anni > 100){
    std::cout << "Pay attention! It seems you are 100 years old! " << std::endl;
    return;
  }

  if (anni < 1){
    std::cout << "Age: " << mesi << " months and " << giorni << " days " << std::endl;
    return;
  }

  std::cout << "Age: " << anni << "years "<< std::endl;

  return; 
}


//[E3][A5] Birthday
int main()
{
  int currentDay;
  int currentMonth;
  int currentYear;

  int bdayDay;
  int bdayMonth;
  int bdayYear;

  std::cout << "Enter current date (gg mm yyyy): ";
  std::cin >> currentDay >> currentMonth >> currentYear;

  std::cout << "Enter your birthday (gg mm yyyy): ";
  std::cin >> bdayDay >> bdayMonth >> bdayYear;

  std::cout << "Current date: " << currentDay << "/" << currentMonth << "/" << currentYear << std::endl;

  std::cout << "Birthday: " << bdayDay << "/" << bdayMonth << "/" << bdayYear << std::endl;

  computeAge(currentDay, currentMonth, currentYear, bdayDay, bdayMonth, bdayYear);

  return 0;
}

```

> The above command returns:

```c

```

```cpp
Enter current date (gg mm yyyy): 2 12 2020
Enter your birthday (gg mm yyyy): 1 2 1900
Current date: 2/12/2020
Birthday: 1/2/1900
Pay attention! It seems you are 100 years old!

``` 

**Assignement 5**: *Write a C++ program that ask the user to insert the current date and his birthday, so the user enters three integers (day, month, year) for the current date and three more integers for his birthday. After the validation of the input the program displays the age of the person. if the birthday date is in the future the program displays an error message. If the result, i.e. the age is greater than 100 years, the program displays a warning. If the result is under 1 year, the programs displays the result in terms of months and days.* 

**Solution**:

The program ask the user to enter six integers values.

Then we use `computeAge` function to compute the difference between the two dates.

The function prints out the result and takes as input six parameters.

If we want to computes the age in terms of years, months and days we have to computed each difference taking into account the number of days of each month.

We use a `switch case` to to that. 

Finally, we compute the difference of each quantity and display the result.

If you want you can recycle the code of the previous exercise and call directly that function, try this!

You can also try out a solution in which you print the result in the main function and not inside the custom function, try this! 



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
<br>
<br>
<br>
<br>

### [E3][A6] Fibonacci series WHILE

```cpp
#include <iostream>


int main()
{
  int t1 = 0, t2 = 1, nextTerm = 0, n;

  std::cout << "Enter a positive number: ";
  std::cin >> n;

  // displays the first two terms which is always 0 and 1
  std::cout << "Fibonacci Series: " << t1 << ", " << t2 << ", ";

  nextTerm = t1 + t2;

  while(nextTerm <= n)
  {
    std::cout << nextTerm << ", ";
    t1 = t2;
    t2 = nextTerm;
    nextTerm = t1 + t2;
  }
  return 0;
}

```

> The above command returns:

```c

```

```cpp
Enter a positive integer: 100
Fibonacci Series: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89,

``` 

**Assignement 6**: *Write a C++ program that shows the Fibonacci sequence up to a certain number*

**Solution**:
The Fibonacci sequence is a series where the next term is the sum of pervious two terms. The first two terms of the Fibonacci sequence is 0 followed by 1.

Here the program asks the user to enter an integer to know the value up to which the program has to compute the sequence. 

Then a while loop is used to iterate until the entered value is reached. For each loop we update t1 and t2 value and compute the next term.

Note that the first two terms in a Fibonacci sequence are always the same, 0 and 1.

 
  
   
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
<br> 
<br>
<br>


### [E3][A6] Fibonacci series FOR

```cpp
#include <iostream>

int main()
{
  int n, t1 = 0, t2 = 1, nextTerm = 0;

  std::cout << "Enter the number of terms: ";
  std::cin >> n;

  std::cout << "Fibonacci Series: ";

  for (int i = 1; i <= n; ++i)
  {
    // Prints the first two terms.
    if(i == 1)
    {
      std::cout << " " << t1;
      continue;
    }
    if(i == 2)
    {
      std::cout << t2 << " ";
      continue;
    }
    nextTerm = t1 + t2;
    t1 = t2;
    t2 = nextTerm;
    
    std::cout << nextTerm << " ";
  }
  return 0;
}

```

> The above command returns:

```c

```

```cpp
Enter the number of terms: 10
Fibonacci Series: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34,

``` 

**Assignement 6**: *Write a C++ program that shows the Fibonacci sequence up to a number n of terms*

**Solution**:
The Fibonacci sequence is a series where the next term is the sum of pervious two terms. The first two terms of the Fibonacci sequence is 0 followed by 1. 

Here the program asks the user to enter an integer to know the number of therms to compute. 

Then a for loop is used to iterate n times. For each loop we compute the next term and update t1 and t2 value accordingly.

Note that the first two terms in a Fibonacci sequence are always the same, 0 and 1.

 
  
   
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
<br>
<br>
<br>
<br>
<br>
<br>
<br>




### [E3][A7] Check Prime Number

```cpp
#include <iostream>

int main() {
  int i, n;
  bool isPrime = true;

  std::cout << "Enter a positive integer: ";
  std::cin >> n;

  // 0 and 1 are not prime numbers
  if (n == 0 || n == 1) {
      isPrime = false;
  }
  else {
    for (i = 2; i <= n / 2; ++i) {
      if (n % i == 0) {
        isPrime = false;
        break;
      }
    }
  }
  if (isPrime)
    std::cout << '\n' << n << " is a prime number" << std::endl;
  else
    std::cout << '\n' << n << " is not a prime number" << std::endl;

  return 0;
}

```

> The above command returns:

```c

```

```cpp
Enter a positive integer: 8
8 is not a prime number

``` 

**Assignement 7**: *Write a C++ program that check if a number is prime or not.*

**Solution**:

A positive integer which is only divisible by 1 and itself is known as prime number.

For example: 13 is a prime number because it is only divisible by 1 and 13 but, 15 is not prime number because it is divisible by 1, 3, 5 and 15.

Note: 0 and 1 are not prime numbers.

This program takes a positive integer from the user and stores it in the variable `n`.

Notice that the boolean variable `isPrime` is initialized to `true` at the beginning of the program.

Since 0 and 1 are not prime numbers, we first check if the input number is one of those numbers or not. If the input number is either 0 or 1, then the value of `isPrime` is set to false.

Else, the initial value of `isPrime` is left unchanged and the for loop is executed, which checks whether the number entered by the user is perfectly divisible by `i` or not.

The for loop runs from `i == 2` to `i <= n / 2` and increases the value of `i` by 1 with each iteration.

The loop terminates at `i == n / 2` because we cannot find any factor for n beyond the number `n / 2` . So, any iterations beyond `n / 2` is redundant.

If the number entered by the user is perfectly divisible by `i`, then `isPrime` is set to `false` and the number will not be a prime number.

But if the input number is not perfectly divisible by `i` throughout the entirety of the loop, then it means that the input number is only divisible by 1 and that number itself.

So, the given number is a prime number.

In the case of `n == 2`, the for loop fails to run and the value of `isPrime` remains `true`. 
  
   
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


## Practical examples - 4

### [E4][A1] Displaying Array Elements

```cpp
#include <iostream>

int main() {
  int numbers[5] = {7, 5, 6, 12, 35};

  // cout << "The numbers are: ";
  // //  Printing array elements
  // // using range based for loop
  // for (const int &n : numbers) {
  //     cout << n << "  ";
  // }

  std::cout << "\nThe numbers are: ";
  //  Printing array elements
  // using traditional for loop
  for (int i = 0; i < 5; ++i) {
      std::cout << numbers[i] << ",  ";
  }

  return 0;
}

```

> The above command returns:

```c

```

```cpp
7, 5, 6, 12, 35

``` 

**Assignement 1**: *Write a C++ program that prints an array.*

**Solution**:
We initialized an array called numbers of size 5 and type int. This means that each element of the array if of type int.  

If we don't mention the size of the array, the compiler automatically computes the size only if it is initialized.

Here, we have used a for loop to iterate from i = 0 to i = 4. In each iteration, we have printed numbers[i].

 
  
   
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
<br>
<br>
<br>
<br>

### [E4][A2] Take Inputs from User and Store Them in an Array

```cpp
#include <iostream>


int main() {
  int numbers[5];

  std::cout << "Enter 5 numbers: " << std::endl;

  //  store input from user to array
  for (int i = 0; i < 5; ++i) {
      std::cin >> numbers[i];
  }

  std::cout << "The numbers are: ";

  //  print array elements
  for (int n = 0; n < 5; ++n) {
      std::cout << numbers[n] << "  ";
  }

  return 0;
}

```

> The above command returns:

```c

```

```cpp
7 5 6 12 35

``` 

**Assignement 2**: *Write a C++ program that prints an array taken in input by the user.*

**Solution**:
We initialized an array called numbers of size 5 and type int. This means that each element of the array if of type int.  

Once again, we have used a for loop to iterate from i = 0 to i = 4. In each iteration, we took an input from the user and stored it in numbers[i].

Then, we used another for loop to print all the array elements.

We have seen also that we can make a custum function to print the array! try by yourlself.
  
   
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

### [E4][A3] Display Sum and Average of Array Elements Using for Loop
```cpp
#include <iostream>

int main() {
    
  // initialize an array without specifying size
  double numbers[] = {7, 5, 6, 12, 35, 27};

  double sum = 0;
  double count = 0;
  double average;

  std::cout << "The numbers are: ";

  // 
  for (int i=0; i<6; ++i>) {
    std::cout << numbers[i] << "  ";

    //  calculate the sum
    sum += numbers[i];

    // count the no. of array elements
    ++count;
  }

  // print the sum
  std::cout << "\nTheir Sum = " << sum << endl;

  // find the average
  average = sum / count;
  std::cout << "Their Average = " << average << endl;

  return 0;
}

```

> The above command returns:

```c

```

```cpp
The numbers are: 7  5  6  12  35  27
Their Sum = 92
Their Average = 15.3333

``` 

**Assignement 3**: *Write a C++ program that computes sum and average of an array.*

**Solution**:
In this program:

We have initialized a double array named `numbers` but without specifying its size. We also declared three double variables `sum`, `count`, and `average`.

Then we used a `for loop` to print the array elements. In each iteration of the loop, we add the current array element to sum.

We also increase the value of `count` by 1 in each iteration, so that we can get the size of the array by the end of the for loop.

After printing all the elements, we print the sum and the average of all the numbers.

The average of the numbers is given by `average = sum / count`;

  
   
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

### [E4][A4] Display Largest Element of an array
```cpp
#include <iostream>

int main()
{
    int i, n;
    float arr[100];

    std::cout << "Enter total number of elements(1 to 100): ";
    std::cin >> n;
    std::cout << endl;

    // Store number entered by the user
    for(i = 0; i < n; ++i)
    {
      std::cout << "Enter Number " << i + 1 << " : ";
      std::cin >> arr[i];
    }

    // Loop to store largest number to arr[0]
    for(i = 1;i < n; ++i)
    {
      // Change < to > if you want to find the smallest element
      if(arr[0] < arr[i]){
        arr[0] = arr[i];
      }
    }
    std::cout << "Largest element = " << arr[0];

    return 0;
}

```

> The above command returns:

```c

```

```cpp
nter total number of elements: 8

Enter Number 1: 23.4
Enter Number 2: -34.5
Enter Number 3: 50
Enter Number 4: 33.5
Enter Number 5: 55.5
Enter Number 6: 43.7
Enter Number 7: 5.7
Enter Number 8: -66.5

Largest element = 55.5

``` 

**Assignement 4**: *Write a C++ program that display largest element of an array.*

**Solution**:
This program takes n number of elements from user and stores it in array `arr[]`.

To find the largest element, the first two elements of array are checked and largest of these two element is placed in `arr[0]`.

Then, the first and third elements are checked and largest of these two element is placed in `arr[0]`.

This process continues until and first and last elements are checked.

After this process, the largest element of an array will be in `arr[0]` position.

  
   
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

### [E4][A5] check values at even indexes
```cpp
#include <iostream>

int main()
{
  int a[10];
  bool ok = true;

  // input
  std::cout<<"Enter 10 numbers: "<<endl;
  for (int i = 0; i < 10; i++)
    {
      std::cin >> a[i];
    }
  //check
  for(int i=0;i<9;i++)
  {
    if(i % 2 == 0)
    {
        if(a[i] % 2 != 0){
          ok=false;
        }
    }
  }
  if(ok){
    std::cout<<"Correct.";
  }
  else{
    std::cout<<"Not correct.";
  }
  return 0;
}

```

> The above command returns:

```c

```

```cpp
Correct.

``` 

**Assignement 5**: *Write a C++ program that check values at even indexes of an array.*

**Solution**:
This program takes n number of elements from user and stores it in array `a[]`.

A `bool` variable is initilized to `true`. 

Then the program check each value with an even index in the array and check if that value is even itself. 

If it is not the condition turns to `false`.

Then the result is shown to the screen. 

  
   
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

### [E4][A6] Passing One-dimensional Array to a Function
```cpp
#include <iostream>

// declare function to display x
// take a 1d array as parameter
void display(int array[5]) {
  std::cout << "Displaying x: " << endl;

  // display array elements    
  for (int i = 0; i < 5; ++i) {
    std::cout << "Student " << i + 1 << ": " << array[i] << endl;
  }
}

int main() {

  // declare and initialize an array
  int x[5] = {88, 76, 90, 61, 69};
  
  // call display function
  // pass array as argument
  display(x);

  return 0;
}

```

> The above command returns:

```c

```

```cpp
Displaying x: 
Student 1: 88
Student 2: 76
Student 3: 90
Student 4: 61
Student 5: 69

``` 

**Assignement 6**: *Write a C++ program that prints an array using a custom function.*

**Solution**:
Here,

When we call a function by passing an array as the argument, only the name of the array is used.

`display(x);`

Here, the argument `x` represent the memory address of the first element of array `x[5]`.
However, notice the parameter of the `display()` function.

`void display(int array[5])`

Here, we use the full declaration of the array in the function parameter, including the square braces `[]`.
The function parameter `int array[5]` converts to `int* array`;. This points to the same address pointed by the array `x`. This means that when we manipulate `array[5]` in the function body, we are actually manipulating the original array `x`.

C++ handles passing an array to a function in this way to save memory and time.

  
   
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

### [E4][A7]  Cipher a given text
```cpp
#include <iostream>
#include <string>
using namespace std;

// Funzione per la criptazione della password
string encrypt(string passwordToEncrypt, int shiftValue)
{
  // Inizializzazione della password criptata e del numero intero utilizzato nel ciclo for
  string encryptedString = "";
  int i;
  // Ciclo for che procede finche non finisce di decriptare tutti i caratteri (lunghezza stringa)
  for (i = 0; i < passwordToEncrypt.length(); i++)
  {
    // Se le lettere sono maiuscole
    if (isupper(passwordToEncrypt[i]))
    {
      // Utilizzo formula per la criptazione con mod26 utilizzando tabella ASCII (Maiuscole)
      encryptedString += char(int(passwordToEncrypt[i] + shiftValue - 'A' + 26) % 26 + 'A');
    }
    // Altrimenti se sono minuscoli
    else
    {
      // Utilizzo formula per la criptazione con mod26 utilizzando tabella ASCII (Minuscole)
      encryptedString += char(int(passwordToEncrypt[i] + shiftValue - 'a' + 26) % 26 + 'a');
    }
  }
  return encryptedString;
}
// Funzione per la decriptazione della password
string decrypt(string passwordToDecrypt, int shiftValue)
{
  // Inizializzazione variabili per la password decriptata e int da utilizzare nel ciclo for
  string decryptedPassword = "";
  int n;
  // Ciclo for che procede finche non finisce di decriptare tutti i caratteri (lunghezza stringa)
  for (n = 0; n < passwordToDecrypt.length(); n++)
  {
    // Se le lettere sono maiuscole
    if (isupper(passwordToDecrypt[n]))
    {
      // Utilizzo formula per la decriptazione con mod26 utilizzando tabella ASCII (Maiuscole)
      decryptedPassword += char(int(passwordToDecrypt[n] - shiftValue - 'A' + 26) % 26 + 'A');
    }
    // Altrimenti se sono minuscole
    else
    {
      // Utilizzo formula per la decriptazione con mod26 utilizzando tabella ASCII (Minuscole)
      decryptedPassword += char(int(passwordToDecrypt[n] - shiftValue - 'a' + 26) % 26 + 'a');
    }
  }
  return decryptedPassword;
}

int main()
{
  // Inizializzazione valori principali quali scelta del menu, valore per shift e stringhe
  int shiftValue = 0;
  int sceltaMenu;
  bool ended = false;
  string passwordToEncrypt;
  string passwordToDecrypt;

  do
  {
    cout << "Select an option:" << endl;
    cout << "1. Encrypt" << endl;
    cout << "2. Decrypt" << endl;
    cout << "3. Quit" << endl;
    cin >> sceltaMenu;
    // Utilizzo switch per generare un menu in grado di cambiare funzionalità
    switch (sceltaMenu)
    {
    case 1:
      cout << "Enter a string to encrypt:" << endl;
      cin >> passwordToEncrypt;
      cout << "Enter a shift value between 0-25:" << endl;
      cin >> shiftValue;
      while (shiftValue > 25 || shiftValue < 0)
      {
        cin >> shiftValue;
      }
      cout << "Password: " << passwordToEncrypt << endl;
      cout << "Shift: " << shiftValue << endl;
      cout << "Encrypted Password: " << encrypt(passwordToEncrypt, shiftValue) << endl;
      break;
    case 2:
      cout << "Enter a string to decrypt:" << endl;
      cin >> passwordToDecrypt;
      cout << "Enter a shift value between 0-25:" << endl;
      cin >> shiftValue;
      cout << "The plain text is:" << decrypt(passwordToDecrypt, shiftValue) << endl;
      break;
    case 3:
      ended = true;
      break;
    default:
      cout << "Invalid option. Try again." << endl;
    }
  } while (!ended);
  return 0;
}

```

> The above command returns:

```c

```

```cpp
plainText : ABCDEFGHIJKLMNOPQRSTUVWXYZ
shift: 1
cipherText:BCDEFGHIJKLMNOPQRSTUVWXYZA

``` 

**Assignement 7**: Write a C++ program to cipher a given text.
Use the Caesar Cipher technique to make the encryption. The Caesar Cipher technique is one of the simplest method of encryption method.
 It’s a type of substitution cipher, i.e., each letter of a given text is replaced by a letter some fixed number of positions down the alphabet [Wikipedia link: https://en.wikipedia.org/wiki/Caesar_cipher ]. For example with a shift of 1, A would be replaced by B, B wouldbecome C, and so on. Thus to cipher a given text we need an integer value (shift), which indicates the number of position each letter of the text has been moved down. The encryption can be represented using modular arithmetic by first transforming the letters into numbers, according to the scheme, A = 0, B = 1,..., Z = 25. Encryption of a letter by a shift n can be described mathematically as: 

* e(x)=(x+n)mod26(Encryption Phase with shift n)

* d(x)=(x−n)mod26(Decryption Phase with shift n)
 
 Examples :

 plainText : ABCDEFGHIJKLMNOPQRSTUVWXYZ

 shift: 1

 cipherText: BCDEFGHIJKLMNOPQRSTUVWXYZA


 plainText : password
 
 shift: 2

 cipherText: rcuuyqtf

So, the program takes in input a String (you can use `#include <string>` or an array of char) of lower or upper case letters, and an Integer between 0-25 denoting the required shift and prints out the plain text (with lower or upper case letters), the shift value and the cipher text like in the examples provided above.

Tips: Write a function `encrypt()` which takes as arguments the plain text and the shift. In this function traverse the given text one character at a time. For each character, transform the given character, according to the encryption rule (pay attention also to lower and upper letter case).

Task 2. Add to the program a function to decrypt the cipher text.

Task 3. Add to the program a menu that let the user select what action he wants to take

Goal: Send us your name encrypted with a shift given by deciphering this cipher text (shift=8): NQDM

**Solution**:
Firstly, we initialized the variables we need during the execution of the program. An integer value to store the shift value, an integer value to store the selected option from the menu, a bool flag to control the execution of the do ... while and two strings to store the values of the words to decrypt or encrypt.

Then a do while is used to keep the program until the user select the quit option.

In the case the user select the encryption option, the program calls a custom function that we have defined.

The encryption function takes as argument a string to encrypt and the value of the shift. Then for each character of the strings we shift the char in the range 0-25 by doing -'a', then we apply the shift and finally we shift the result again in the range a-z by doing +'a'. 

We can also check and maintains uppercase letter by using 'A'. 

The function return the encrypted string. 

In the case the user select the decryption option, the program calls a custom function that we have defined.

The decryption function takes as argument a string to decrypt and the value of the shift. Then for each character of the strings we shift the char in the range 0-25 by doing -'a', then we apply the shift and finally we shift the result again in the range a-z by doing +'a'. 

We can also check and maintains uppercase letter by using 'A'. 

The function return the decrypted string. 

Finally the program displays the result.

  
   
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
<br>
<br>

## Practical examples - 5

### [E5][A1]  Add Two Matrices using Multi-dimensional Arrays
```cpp
#include <iostream>
using namespace std;

int main()
{
  int r, c, a[100][100], b[100][100], sum[100][100], i, j;

  cout << "Enter number of rows (between 1 and 100): ";
  cin >> r;

  cout << "Enter number of columns (between 1 and 100): ";
  cin >> c;

  cout << endl << "Enter elements of 1st matrix: " << endl;

  // Storing elements of first matrix entered by user.
  for(i = 0; i < r; ++i){
    for(j = 0; j < c; ++j)
    {
      cout << "Enter element a" << i + 1 << j + 1 << " : ";
      cin >> a[i][j];
    }
  }

  // Storing elements of second matrix entered by user.
  cout << endl << "Enter elements of 2nd matrix: " << endl;
  for(i = 0; i < r; ++i){
    for(j = 0; j < c; ++j)
    {
      cout << "Enter element b" << i + 1 << j + 1 << " : ";
      cin >> b[i][j];
    }
  }

  // Adding Two matrices
  for(i = 0; i < r; ++i){
    for(j = 0; j < c; ++j){
      sum[i][j] = a[i][j] + b[i][j];
    }
  }
  // Displaying the resultant sum matrix.
  cout << endl << "Sum of two matrix is: " << endl;
  for(i = 0; i < r; ++i){
    for(j = 0; j < c; ++j)
    {
      cout << sum[i][j] << "  ";
      if(j == c - 1)
        cout << endl;
    }
  }

  return 0;
}

```

> The above command returns:

```c

```

```cpp
Enter number of rows (between 1 and 100): 2
Enter number of columns (between 1 and 100): 2

Enter elements of 1st matrix:
Enter element a11: -4
Enter element a12: 5
Enter element a21: 6
Enter element a22: 8

Enter elements of 2nd matrix:
Enter element b11: 3
Enter element b12: -9
Enter element b21: 7
Enter element b22: 2

Sum of two matrix is:
-1   -4
13   10

``` 

**Assignement 1**: This program takes two matrices of order r*c and stores it in two-dimensional array. Then, the program adds these two matrices and displays it on the screen.

**Solution**:
In this program, user is asked to entered the number of rows r and columns c. The value of r and c should be less than 100 in this program.

The user is asked to enter elements of two matrices (of order r*c).

Then, the program adds these two matrices, saves it in another matrix (two-dimensional array) and displays it on the screen.

  
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
<br>
<br>
<br>
<br>

### [E5][A2]  Find Transpose of a Matrix
```cpp
#include <iostream>
using namespace std;

int main() {
   int a[10][10], transpose[10][10], row, column, i, j;

   cout << "Enter rows and columns of matrix: ";
   cin >> row >> column;

   cout << "\nEnter elements of matrix: " << endl;

   // Storing matrix elements
   for (int i = 0; i < row; ++i) {
    for (int j = 0; j < column; ++j) {
      cout << "Enter element a" << i + 1 << j + 1 << ": ";
      cin >> a[i][j];
    }
   }

   // Printing the a matrix
   cout << "\nEntered Matrix: " << endl;
   for (int i = 0; i < row; ++i) {
    for (int j = 0; j < column; ++j) {
      cout << " " << a[i][j];
      if (j == column - 1){
        cout << endl << endl;
      }
    }
   }

   // Computing transpose of the matrix
   for (int i = 0; i < row; ++i){
    for (int j = 0; j < column; ++j) {
      transpose[j][i] = a[i][j];
    }
   }

   // Printing the transpose
   cout << "\nTranspose of Matrix: " << endl;
   for (int i = 0; i < column; ++i){
    for (int j = 0; j < row; ++j) {
      cout << " " << transpose[i][j];
      if (j == row - 1){
        cout << endl << endl;
      }
    }
   }

   return 0;
}

```

> The above command returns:

```c

```

```cpp
Enter rows and columns of matrix: 2
3

Enter elements of matrix:
Enter element a11: 1
Enter element a12: 2
Enter element a13: 9
Enter element a21: 0
Enter element a22: 4
Enter element a23: 7

Entered Matrix:
1  2  9

0  4  7


Transpose of Matrix:
1  0

2  4

9  7

``` 

**Assignement 2**: This program takes a matrix of order r*c from the user and computes the transpose of the matrix.

**Solution**:
In this program, user is asked to entered the number of rows and columns. The value of rows and columns should be less than 10 in this program.

Then, the user is asked to enter elements of the matrix.

The program computes the transpose of the matrix and displays it on the screen.

  
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
<br>
<br>
<br>

### [E5][A3]   Multiply Matrix by Passing it to a Function
```cpp
#include <iostream>
using namespace std;

void enterData(int firstMatrix[][10], int secondMatrix[][10], int rowFirst, int columnFirst, int rowSecond, int columnSecond);
void multiplyMatrices(int firstMatrix[][10], int secondMatrix[][10], int multResult[][10], int rowFirst, int columnFirst, int rowSecond, int columnSecond);
void display(int mult[][10], int rowFirst, int columnSecond);

void enterData(int firstMatrix[][10], int secondMatrix[][10], int rowFirst, int columnFirst, int rowSecond, int columnSecond)
{
	int i, j;
	cout << endl << "Enter elements of matrix 1:" << endl;
	for(i = 0; i < rowFirst; ++i)
	{
		for(j = 0; j < columnFirst; ++j)
		{
			cout << "Enter elements a"<< i + 1 << j + 1 << ": ";
			cin >> firstMatrix[i][j];
		}
	}

	cout << endl << "Enter elements of matrix 2:" << endl;
	for(i = 0; i < rowSecond; ++i)
	{
		for(j = 0; j < columnSecond; ++j)
		{
			cout << "Enter elements b" << i + 1 << j + 1 << ": ";
			cin >> secondMatrix[i][j];
		}
	}
}

void multiplyMatrices(int firstMatrix[][10], int secondMatrix[][10], int mult[][10], int rowFirst, int columnFirst, int rowSecond, int columnSecond)
{
	int i, j, k;

	// Initializing elements of matrix mult to 0.
	for(i = 0; i < rowFirst; ++i)
	{
		for(j = 0; j < columnSecond; ++j)
		{
			mult[i][j] = 0;
		}
	}

	// Multiplying matrix firstMatrix and secondMatrix and storing in array mult.
	for(i = 0; i < rowFirst; ++i)
	{
		for(j = 0; j < columnSecond; ++j)
		{
			for(k=0; k<columnFirst; ++k)
			{
				mult[i][j] += firstMatrix[i][k] * secondMatrix[k][j];
			}
		}
	}
}

void display(int mult[][10], int rowFirst, int columnSecond)
{
	int i, j;

	cout << "Output Matrix:" << endl;
	for(i = 0; i < rowFirst; ++i)
	{
		for(j = 0; j < columnSecond; ++j)
		{
			cout << mult[i][j] << " ";
			if(j == columnSecond - 1)
				cout << endl << endl;
		}
	}
}

int main()
{
	int firstMatrix[10][10], secondMatrix[10][10], mult[10][10], rowFirst, columnFirst, rowSecond, columnSecond, i, j, k;

	cout << "Enter rows and column for first matrix: ";
	cin >> rowFirst >> columnFirst;

	cout << "Enter rows and column for second matrix: ";
	cin >> rowSecond >> columnSecond;

	// If colum of first matrix in not equal to row of second matrix, asking user to enter the size of matrix again.
	while (columnFirst != rowSecond)
	{
		cout << "Error! column of first matrix not equal to row of second." << endl;
		cout << "Enter rows and column for first matrix: ";
		cin >> rowFirst >> columnFirst;
		cout << "Enter rows and column for second matrix: ";
		cin >> rowSecond >> columnSecond;
	}

	// Function to take matrices data
  enterData(firstMatrix, secondMatrix, rowFirst, columnFirst, rowSecond, columnSecond);

  // Function to multiply two matrices.
  multiplyMatrices(firstMatrix, secondMatrix, mult, rowFirst, columnFirst, rowSecond, columnSecond);

  // Function to display resultant matrix after multiplication.
  display(mult, rowFirst, columnSecond);

	return 0;
}



```

> The above command returns:

```c

```

```cpp
Enter rows and column for first matrix: 3
2
Enter rows and column for second matrix: 3
2
Error! column of first matrix not equal to row of second.

Enter rows and column for first matrix: 2
3
Enter rows and column for second matrix: 3
2

Enter elements of matrix 1:
Enter elements a11: 3
Enter elements a12: -2
Enter elements a13: 5
Enter elements a21: 3
Enter elements a22: 0
Enter elements a23: 4

Enter elements of matrix 2:
Enter elements b11: 2
Enter elements b12: 3
Enter elements b21: -9
Enter elements b22: 0
Enter elements b31: 0
Enter elements b32: 4

Output Matrix:
24 29

6  25

``` 

**Assignement 3**: Multiply two matrices and display it using user defined function.

**Solution**:
This program asks user to enter the size of the matrix (rows and columns).

Then, it asks the user to enter the elements of two matrices and finally it multiplies two matrix and displays the result.

To perform this task three functions are made:

1. To take matrix elements from user
2. To multiply two matrix
3. To display the resultant matrix after multiplication


  
   
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
<br>
<br>
<br>
<br>
<br>




##  Practical examples - 6
In this section, you'll learn about structures in C++ programming; what is it, how to define it and use it in your program.

**Structure** is a collection of variables of different data types under a single name. 

### [E6][A1]  
```cpp
#include <iostream>

struct Person
{
  char name[50];
  int age;
  float salary;
};

int main()
{
  Person p1;
  
  std::cout << "Enter Full name: ";
  std::cin.get(p1.name, 50);
  std::cout << "Enter age: ";
  std::cin >> p1.age;
  std::cout << "Enter salary: ";
  std::cin >> p1.salary;

  std::cout << "\nDisplaying Information." << endl;
  std::cout << "Name: " << p1.name << endl;
  std::cout <<"Age: " << p1.age << endl;
  std::cout << "Salary: " << p1.salary;

  return 0;
}

```

> The above command returns:

```c

```

```cpp
Enter Full name: Magdalena Dankova
Enter age: 27
Enter salary: 1024.4

Displaying Information.
Name: Magdalena Dankova
Age: 27
Salary: 1024.4
``` 

**Assignement 1**: 
C++ Program to assign data to members of a structure variable and display it.

**Solution**:
The struct keyword defines a structure type followed by an identifier (name of the structure).
Then inside the curly braces, you can declare one or more members (declare variables inside curly braces) of that structure.
When a structure is created, no memory is allocated.
Here a structure `Person` is declared which has three members `name`, `age` and `salary`.
Once you declare a structure person as above. You can define a structure variable.
When structure variable is defined, only then the required memory is allocated by the compiler.
The members of structure variable is accessed using a `dot (.)` operator.
Inside `main()` function, a structure variable `p1` is defined. Then, the user is asked to enter information and data entered by user is displayed.

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
<br>



### [E6][A2] Passing structure to function in C++
```cpp
#include <iostream>

struct Person
{
    char name[50];
    int age;
    float salary;
};

void displayData(Person);   // Function declaration

void displayData(Person p) // Function definition
{
  std::cout << "\nDisplaying Information." << endl;
  std::cout << "Name: " << p.name << endl;
  std::cout <<"Age: " << p.age << endl;
  std::cout << "Salary: " << p.salary;
}

int main()
{
  Person p;

  std::cout << "Enter Full name: ";
  std::cin.get(p.name, 50);
  std::cout << "Enter age: ";
  std::cin >> p.age;
  std::cout << "Enter salary: ";
  std::cin >> p.salary;

  // Function call with structure variable as an argument
  displayData(p);

  return 0;
}



```

> The above command returns:

```c

```

```cpp
Enter Full name: Bill Jobs
Enter age: 55
Enter salary: 34233.4

Displaying Information.
Name: Bill Jobs
Age: 55
Salary: 34233.4
``` 

**Assignement 2**: 
Structure variables can be passed to a function and returned in a similar way as normal arguments.

**Solution**:
In this program, user is asked to enter the name, age and salary of a `Person` inside `main()` function.
Then, the structure variable `p` is to passed to a function using `displayData()` function.
The return type of `displayData()` is void and a single argument of type structure `Person` is passed.
Then the members of structure `p` is displayed from this function.



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
<br>


### [E6][A3] Input/output with files
```cpp
// basic file operations
#include <iostream>
#include <fstream>
using namespace std;

int main () {
  ofstream myfile;
  myfile.open ("example.txt");
  myfile << "Writing this to a file.\n";
  myfile.close();
  return 0;
}


```

> The above command returns:

```c

```

```cpp
[file example.txt]
Writing this to a file.
``` 

**Assignement 3**: 
C++ provides the following classes to perform output and input of characters to/from files:

  * ofstream: Stream class to write on files
  * ifstream: Stream class to read from files
  * fstream: Stream class to both read and write from/to files.


These classes are derived directly or indirectly from the classes istream and ostream.

**Solution**:
This code creates a file called example.txt and inserts a sentence into it in the same way we are used to do with cout, but using the file stream myfile instead.
The first operation generally performed on an object of one of these classes is to associate it to a real file. This procedure is known as to open a file. An open file is represented within a program by a stream (i.e., an object of one of these classes) and any input or output operation performed on this stream object will be applied to the physical file associated to it.

In order to open a file with a stream object we use its member function open:

open (filename, mode);

Where filename is a string representing the name of the file to be opened, and mode is an optional parameter.
Each of the open member functions of classes ofstream, ifstream and fstream has a default mode that is used if the file is opened without a second argument: 
class | default mode 
----- | ------------
ofstream | ios::out
ifstream | ios::in
fstream | ios::in ios::out

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
<br>


### [E6][A4] 
```cpp
#include <iostream>
#include <cstring>

using namespace std;


//////////////////////////////////////////////////////////////////////////////////////
// Strutture dati
//////////////////////////////////////////////////////////////////////////////////////

// Costanti
const int max_esami = 100;
const int max_lunghezza_stringhe = 32;

// Struttura per la memorizzazione dei dati relativi a un esame
struct esame {
	char nome_studente[max_lunghezza_stringhe];
	char cognome_studente[max_lunghezza_stringhe];
	int numero_matricola;
	int voto;
};

// Struttura per la memorizzazione degli esami della sessione
struct sessione_di_esami {
	esame archivio_esami[max_esami];
	int num_esami;
};


//////////////////////////////////////////////////////////////////////////////////////
// Funzioni per l'inizializzazione delle strutture dati
//////////////////////////////////////////////////////////////////////////////////////

// Inizializzazione di un esame
void inizializza_esame(esame& e)
{
	strcpy(e.nome_studente, "");	//Inizializza e.Nome con la stringa vuota ""
	strcpy(e.cognome_studente, "");
	e.numero_matricola = 0;
	e.voto = 0;
}

// Inizializzazione di una sessione di esami
void inizializza_sessione_esami(sessione_di_esami& sessione)
{
	for (int k = 0; k < max_esami; k++)
		inizializza_esame(sessione.archivio_esami[k]);

	sessione.num_esami = 0;
}


//////////////////////////////////////////////////////////////////////////////////////
// Funzioni per l'inserimento dei dati
//////////////////////////////////////////////////////////////////////////////////////

// Inserimento dei dati di un esame
void inserisci_dati_esame(esame& e)
{
	// cleaning
	cin.clear();   
	cin.sync();

	cout << "Inserire il nome dello studente: ";
	cin.getline(e.nome_studente, 32, '\n');
	cout << endl;

	cout << "Inserire il cognome dello studente: ";
	cin.getline(e.cognome_studente, 32, '\n');
	cout << endl;

	cout << "Inserire il numero di matricola: ";
	cin >> e.numero_matricola;
	cout << endl;

	do {
		cout << "Inserire il voto di esame: ";
		cin >> e.voto;
		cout << endl;
		if ((e.voto > 30) || (e.voto < 18))
			cout << "Attenzione: il voto deve essere compreso tra 18 e 30." << endl << endl;
	} while ((e.voto > 30) || (e.voto < 18));
}

// Inserimento di un esame in una sessione
// Ritorna 1 se l'inserimento è riuscito, 0 altrimenti
int inserisci_esame(sessione_di_esami& sessione, esame e)
{
	if (sessione.num_esami < max_esami) {
		sessione.archivio_esami[sessione.num_esami] = e;
		sessione.num_esami++;
		return 1;
	}
	return 0;
}


//////////////////////////////////////////////////////////////////////////////////////
// Funzioni per la stampa dei dati
//////////////////////////////////////////////////////////////////////////////////////

// Stampa di un esame
void stampa_dati_esame(esame e)
{
	cout << "Nome: " << e.nome_studente << endl;
	cout << "Cognome: " << e.cognome_studente << endl;
	cout << "Numero di matricola: " << e.numero_matricola << endl;
	cout << "Voto di esame: " << e.voto << endl << endl;
}

// Stampa di una sessione di esami
// const significa che s (passato per riferimento) non verrà modificato dalla funzione
// Passiamo s per riferimento per evitare il passaggio per valore che implica
// la copia di TUTTA la struttura dati, che può essere uno spreco di tempo(e memoria)!
void stampa_sessione(const sessione_di_esami& sessione)
{
	for (int k = 0; k < sessione.num_esami; k++)
		stampa_dati_esame(sessione.archivio_esami[k]);
}


//////////////////////////////////////////////////////////////////////////////////////
// Funzioni per l'elaborazione dei dati
//////////////////////////////////////////////////////////////////////////////////////

// Calcolo della media dei voti di una sessione
double calcola_media_voti(const sessione_di_esami& sessione)
{
	if (sessione.num_esami > 0) {
		double somma = 0.0;
		for (int k = 0; k < sessione.num_esami; k++)
			somma += sessione.archivio_esami[k].voto;
		return somma / sessione.num_esami;
	}
	return 0.0;
}

// Calcolo del numero di studenti con voto maggiore di n
int calcola_num_studenti(const sessione_di_esami& sessione, int n)
{
	int contatore = 0;

	for (int k = 0; k < sessione.num_esami; k++)
		if (sessione.archivio_esami[k].voto > n) 
			contatore++;

	return contatore;
}

// Calcolo dell'istogramma dei voti di esame di una sessione
void calcola_istogramma(const sessione_di_esami& sessione, int istogramma[13])
{
	for (int i = 0; i < 13; i++)
		istogramma[i] = 0;

	for (int k = 0; k < sessione.num_esami; k++) {
		int indice = sessione.archivio_esami[k].voto - 18;  // Riporta l'indice da 0 a 13 in base al voto
		istogramma[indice]++;
	}
}


//////////////////////////////////////////////////////////////////////////////////////
// Funzione main
//////////////////////////////////////////////////////////////////////////////////////

int main()
{
	// Sessione di esami
	sessione_di_esami sessione;
	inizializza_sessione_esami(sessione);
	
	// Variabili ausiliarie per l'elaborazione dati
	esame e;
	inizializza_esame(e);
	double media = 0.0;
	int soglia = 18;
	int num_studenti = 0;
	int istogramma[13];

	// Variabile per la condizione di terminazione del programma
	int continua = 1;

	// Pulizia dei flussi in ingresso
	cin.clear();   
	cin.sync();

	do {
		
		// Stampa del menu delle operazioni diponibili
		cout << "Operazioni disponibili: " << endl;
		cout << "1 - Inserire un nuovo esame" << endl;
		cout << "2 - Media dei voti conseguiti" << endl;
		cout << "3 - Numero di studenti con voto superiore ad una specifica soglia" << endl;
		cout << "4 - Istogramma dei voti conseguiti" << endl;
		cout << "5 - Esci" << endl << endl;
		cout << "Selezionare un'opzione: ";
		
		// Inserimento della scelta da parte dell'utente
		int scelta = 0;
		cin >> scelta;
		system("cls");

		// Esecuzione dell'operazione richiesta
		switch (scelta) {
			case 1:			// Inserimento di un nuovo esame
				inserisci_dati_esame(e);
				if (inserisci_esame(sessione, e)) 
					cout << "Nuovo esame inserito" << endl <<endl;
				else
					cout << "E' stato raggiunto il massimo numero di esami per sessione. Non si possono inserire ulteriori esami" << endl << endl;
				system("pause");
				system("cls");
				break;
			case 2:			// Calcolo della media dei voti conseguiti
				media = calcola_media_voti(sessione);
				cout << "La media dei voti conseguiti e': " << media << endl << endl;
				system("pause");
				system("cls");
				break;
			case 3:			// Calcolo del numero di studenti che hanno conseguito un voto superiore ad una data soglia
				cout << "Inserire il voto di soglia: ";
				cin >> soglia;
				cout << endl;
				num_studenti = calcola_num_studenti(sessione, soglia);
				cout << num_studenti << " studenti hanno conseguito un voto maggiore o uguale a " << soglia << endl << endl;
				system("pause");
				system("cls");
				break;
			case 4:		// Calcolo dell'istogramma dei voti conseguiti
				calcola_istogramma(sessione, istogramma);
				cout << "Istogramma dei voti conseguiti:" << endl;
				for (int k = 0; k < 13; k++)
					cout << k + 18 << ": " << istogramma[k] << endl;
				cout << endl;
				system("pause");
				system("cls");
				break;
			case 5:		// Uscita dal programma
				continua = 0;
				break;
			default:	// Opzione non disponibile
				system("cls");
				cout << "Opzione non disponibile: inserire un numero tra 1 e 6" << endl << endl;
		}

	} while (continua);

	return 0;
}

```

> The above command returns:

```c

```

```cpp
Student name: Anthony 
Student surname: Hopkins
Student_id: 12345
Rank: 28
``` 

**Assignement 4**: 
Write a c++ programs to gather data about the exams period of a specific university course. For each exam the program stores the name and the surname of the student, his/her student id and the exam mark. The exams period has 100 exams at most. The program should provide the following functions: A function to enter student data, a function to compute and print the mean of the marks, a function to compute the number of students that have passed an exam with a grade above n, with n specified from the user; a function to compute and print the hystogram of exams marks (occurrency of each mark).
The main function will allow the user to select one of the features provided by the program and execute the corresponding function.

**Solution**:
In progress....

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
<br>
<br>
<br>
<br>
<br>

### [E6][A5] 
```cpp

#include <iostream>
#include <fstream>
using namespace std;

const int r = 31;
const int c = 10;

double totaleMerce(double T[r][c])
{
	double s = 0;
	for (int i = 0; i < r; i++)
		for (int j = 0; j < c; j++)
			s += T[i][j];
	return s;
}

int numTreni(double T[r][c])
{
    int count = 0;
    for (int i = 0; i < r; i++)
        for (int j = 0; j < c; j++)
            if (T[i][j] != 0.0) {
                count++;
                break;
            }
    return count;
}

double maxTreno(double T[r][c], int& v, int& g) 
{
	g = 0; v = 0;
	double s = 0.0;
	for (int i = 0; i < r; i++) {
		int count = 0;
		double sum = 0.0;
		for (int j = 0; j < c; j++) {
			if (T[i][j] != 0.0) {
				count++;
				sum += T[i][j];
			}
		}
		if (count > v) {
			v = count;
			g = i;
			s = sum;
		}
	}
	return s;
}

int main() {
	double Treni[r][c] = {0};
	fstream fin;
	fin.open("Dati.txt", ios::in);
	for (int i = 0; i < r; i++)
		for (int j = 0; j < c; j++)
			fin >> Treni[i][j];
	fin.close();
	cout << "Totale merce movimentata: " << totaleMerce(Treni) << endl;
	cout << "Numero di treni: " << numTreni(Treni) << endl;
	int giorno = 0;
	int nVagoni = 0;
	double merce = maxTreno(Treni, nVagoni, giorno);
	cout << "Massimo numero di vagoni: " << nVagoni << endl;
	cout << "Giorno del treno con massimo numero di vagoni: " << giorno << endl;
	cout << "Merce del treno con massimo numero di vagoni: " << merce << endl;
	return 0;
}

```

> The above command returns:

```c

```

```cpp

``` 

**Assignement 5**: 
A shipping agency organizes almost daily the movement of goods between two cities connected by a railway. The goods are therefore placed on a train that can consist of a maximum of 10 wagons. To represent the data relating to this activity over the course of a month, a matrix T of real numbers of 31 rows and 10 columns can be used, where the rows represent the days of a month and the columns the wagons of the train. The Tij element of the matrix represents the number of tons of goods loaded on a specific wagon (the j-th wagon) on a specific day (the i-th day). If the train on a certain day was made up of less than 10 wagons, the remaining elements of the corresponding row of the matrix T are set to zero. If on a certain day the train
not started, all the elements of the corresponding row of the matrix T are set to zero (in the same way months that have at least 31 days are managed). To process this data, develop the following in C ++ language: 1.The totalMerceche function receives as a parameter the matrix T described above and returns as a return value the total number of tons of goods handled during the month (a real number). The function will then calculate and return the sum of the values ​​of the elements of the matrix T. For simplicity, assume that the values ​​assumed by the elements of the matrix T are always valid. 2 The numTrenic function receives as a parameter the matrix T described above and returns as a return value, the total number of trains that traveled during the month (an integer). The function will then calculate and return the number of rows of the matrix T that contain at least one non-zero element. For the sake of simplicity, assume that the values ​​assumed by the elements of the matrix T are always valid. 3 The maxTren function, which receives the matrix T described above as a parameter, has as output parameters (i.e. by reference) two integers v and g and returns the value of return a real number. The function assigns to v the number of wagons of the train composed of the largest number of wagons, assigns the index of the day on which that train traveled and returns as a return value the number of tons of goods that this train has transported. is more than one train with the same maximum number of wagons, the function returns the data of the train that traveled first (i.e. the first that is found by scanning the rows of the matrix T from the first to the last). For the sake of simplicity, assume that the values ​​assumed by the elements of the matrix T are always valid. 4. A program that operates as follows: declares and initializes to zero an array of real numbers of 31 rows and 10 columns organized as described above; open the Data.txt file for reading: the file consists of 31 lines, each containing 10 real numbers (for simplicity, suppose that the file exists and that its content is always valid) scan the file and assign to each element of the Trains matrix the corresponding value contained in the file; call the function totalMerce and print its return value on the screen; you call the numTrenie function and print its return value on the screen; you call the maxTreno function and print its return value and the values ​​assumed by the parameters passed by reference after calling the function.

**Solution**:
In progress





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
<br>
<br>
<br> 
<br>
<br>
<br>
<br>
<br>

### [E6][A6] 
```cpp
#include <iostream>
#include <cstring>

using namespace std;


//////////////////////////////////////////////////////////////////////////////////////
// Strutture dati
//////////////////////////////////////////////////////////////////////////////////////

// Costanti
const int max_appartamenti = 100;

// Struttura per la memorizzazione dei dati relativi a un appartamento
struct appartamento {
	int codice;
	char indirizzo[100];
	char comune[32];
	int numero_vani;
	double superficie;
	double prezzo;
};

// Struttura per la memorizzazione degli appartamenti di una agenzia immobiliare
struct archivio_appartamenti {
	appartamento archivio[max_appartamenti];
	int num_appartamenti;
};


//////////////////////////////////////////////////////////////////////////////////////
// Funzioni per l'inizializzazione delle strutture dati
//////////////////////////////////////////////////////////////////////////////////////

// Inizializzazione di un appartamento
void inizializza_appartamento(appartamento& a)
{
	a.codice = 0;
	strcpy(a.indirizzo, "");
	strcpy(a.comune, "");
	a.numero_vani = 0;
	a.superficie = 0.0;
	a.prezzo = 0.0;
}

// Inizializzazione dell'archivio di appartamenti
void inizializza_archivio(archivio_appartamenti& arch)
{
	for (int k = 0; k < max_appartamenti; k++)
		inizializza_appartamento(arch.archivio[k]);

	arch.num_appartamenti = 0;
}


//////////////////////////////////////////////////////////////////////////////////////
// Funzioni per l'inserimento dei dati
//////////////////////////////////////////////////////////////////////////////////////

// Inserimento dei dati di un appartamento
void inserisci_dati_appartamento(appartamento& a)
{
	cout << "Inserire il codice dell'appartamento: ";
	cin >> a.codice;
	cout << endl;

	// cleaning
	cin.clear();   
	cin.sync();

	cout << "Inserire l'indirizzo dell'appartamento: ";
	cin.getline(a.indirizzo, 100, '\n');
	cout << endl;

	cout << "Inserire il comune: ";
	cin.getline(a.comune, 32, '\n');
	cout << endl;

	do {
		cout << "Inserire il numero di vani: ";
		cin >> a.numero_vani;
		cout << endl;
		if (a.numero_vani <= 0)
			cout << "Attenzione: il numero di vani deve essere un numero positivo" << endl << endl;
	} while (a.numero_vani <= 0);

	do {
		cout << "Inserire la superficie (in mq.): ";
		cin >> a.superficie;
		cout << endl;
		if (a.superficie <= 0)
			cout << "Attenzione: la superficie deve essere un numero positivo" << endl << endl;
	} while (a.superficie <= 0);

	do {
		cout << "Inserire il prezzo (in Euro): ";
		cin >> a.prezzo;
		cout << endl;
		if (a.prezzo <= 0)
			cout << "Attenzione: il prezzo deve essere un numero positivo" << endl << endl;
	} while (a.prezzo <= 0);
}

// Inserimento di un appartamento nell'archivio
int inserisci_appartamento(archivio_appartamenti& arch, appartamento a)
{
	if (arch.num_appartamenti < max_appartamenti) {
		arch.archivio[arch.num_appartamenti] = a;
		arch.num_appartamenti++;
		return 1;
	}
	return 0;
}


//////////////////////////////////////////////////////////////////////////////////////
// Funzioni per la stampa dei dati
//////////////////////////////////////////////////////////////////////////////////////

// Stampa di un appartamento
void stampa_dati_appartamento(appartamento a)
{
	cout << "Codice: " << a.codice << endl;
	cout << "Indirizzo: " << a.indirizzo << endl;
	cout << "Comune: " << a.comune << endl;
	cout << "Numero di vani: " << a.numero_vani << endl;
	cout << "Superficie: " << a.superficie << endl;
	cout << "Prezzo: " << a.prezzo << endl << endl;
}

// Stampa dell'archivio di appartamenti
void stampa_archivio(const archivio_appartamenti& arch)
{
	for (int k = 0; k < arch.num_appartamenti; k++)
		stampa_dati_appartamento(arch.archivio[k]);
}


//////////////////////////////////////////////////////////////////////////////////////
// Funzioni per l'elaborazione dei dati
//////////////////////////////////////////////////////////////////////////////////////

// Calcolo del prezzo minimo degli appartamenti in vendita
double calcola_prezzo_minimo(const archivio_appartamenti& arch)
{
	if (arch.num_appartamenti > 0) {
		double minimo = arch.archivio[0].prezzo;
		for (int k = 0; k < arch.num_appartamenti; k++)
			if (arch.archivio[k].prezzo < minimo)
				minimo = arch.archivio[k].prezzo;
		return minimo;
	}
	return 0.0;
}

// Calcolo del prezzo massimo degli appartamenti in vendita
double calcola_prezzo_massimo(const archivio_appartamenti& arch)
{
	if (arch.num_appartamenti > 0) {
		double massimo = arch.archivio[0].prezzo;
		for (int k = 0; k < arch.num_appartamenti; k++)
			if (arch.archivio[k].prezzo > massimo)
				massimo = arch.archivio[k].prezzo;
		return massimo;
	}
	return 0.0;
}

// Calcolo del prezzo medio degli appartamenti in vendita
double calcola_prezzo_medio(const archivio_appartamenti& arch)
{
	if (arch.num_appartamenti > 0) {
		double somma = 0.0;
		for (int k = 0; k < arch.num_appartamenti; k++)
			somma += arch.archivio[k].prezzo;
		return somma / double(arch.num_appartamenti);
	}
	return 0.0;
}

// Calcolo del prezzo medio degli appartamenti la cui superficie e' compresa tra un valore minimo e un valore massimo
double calcola_prezzo_medio_superficie(const archivio_appartamenti& arch, double sup_min, double sup_max)
{
	if ((arch.num_appartamenti > 0) && (sup_max >= sup_min)) {
		double somma = 0.0, contatore = 0.0;
		for (int k = 0; k < arch.num_appartamenti; k++) {
			if ((arch.archivio[k].superficie >= sup_min) && (arch.archivio[k].superficie <= sup_max)) {
				somma += arch.archivio[k].prezzo;
				contatore++;
			}
		}
		if (contatore > 0)
			return somma / contatore;
	}
	return 0.0;
}

// Calcolo dell'istogramma del numero di vani degli appartamenti in vendita
void calcola_istogramma_vani(const archivio_appartamenti& arch, int istogramma[9])
{
	for (int i = 0; i < 9; i++)
		istogramma[i] = 0;

	for (int k = 0; k < arch.num_appartamenti; k++) {
		int numero_vani = arch.archivio[k].numero_vani;
		if (numero_vani > 8)
			istogramma[8]++;
		else
			istogramma[numero_vani - 1]++;
	}
}

// Stampa dell'istogramma del numero di vani degli appartamenti in vendita
void stampa_istogramma_vani(const int istogramma[9])
{
	cout << "Numero di appartamenti per numero di vani:" << endl;
	cout << "Monolocali (1 vano): " << istogramma[0] << endl;
	cout << "Bilocali (2 vani): " << istogramma[1] << endl;
	cout << "Trlocali (3 vani): " << istogramma[2] << endl;
	for (int k = 3; k < 8; k++)
		cout << k + 1 << " vani: " << istogramma[k] << endl;
	cout << "Piu' di 8 vani: " << istogramma[8] << endl;
	cout << endl;
}

// Stampa dei dati relativi agli appartamenti con un dato numero di vani
void stampa_selezione_vani(const archivio_appartamenti& arch, int num_vani)
{
	if ((num_vani > 0) && (arch.num_appartamenti > 0)) {
		int contatore = 0;
		for (int k = 0; k < arch.num_appartamenti; k++) {
			if (arch.archivio[k].numero_vani == num_vani) { 
				stampa_dati_appartamento(arch.archivio[k]);
				contatore++;
			}
		}
		if (contatore == 0)
			cout << "Non vi sono appartamenti di " << num_vani << " vani" << endl << endl;
	}
	else 
		cout << "Attenzione: l'archivio e' vuoto o e' stato inserito un valore negativo per il numero di vani." << endl << endl;
}

// Stampa dei dati relativi agli appartamenti il cui prezzo e' compreso tra un valore minimo e un valore massimo
void stampa_selezione_prezzo(const archivio_appartamenti& arch, double prezzo_minimo, double prezzo_massimo)
{
	if ((arch.num_appartamenti > 0) && (prezzo_massimo >= prezzo_minimo)) {
		int contatore = 0;
		for (int k = 0; k < arch.num_appartamenti; k++) {
			if ((arch.archivio[k].prezzo >= prezzo_minimo) && (arch.archivio[k].prezzo <= prezzo_massimo)) {
				stampa_dati_appartamento(arch.archivio[k]);
				contatore++;
			}
		}
		if (contatore == 0)
			cout << "Non vi sono appartamenti con prezzo compreso tra " << prezzo_minimo << " e " << prezzo_massimo << " Euro" << endl << endl;
	}
	else 
		cout << "Attenzione: l'archivio e' vuoto o e' il prezzo massimo inserito e' inferiore al prezzo minimo." << endl << endl;
}


//////////////////////////////////////////////////////////////////////////////////////
// Funzione main
//////////////////////////////////////////////////////////////////////////////////////

int main()
{
	archivio_appartamenti arch;
	inizializza_archivio(arch);

	appartamento a;

	double sup_min, sup_max;
	double prezzo_medio = 0.0;
	double prezzo_min, prezzo_max;
	int numero_vani;
	int istogramma[9];

	int continua = 1;

	do {
		cin.clear();   
		cin.sync();

		int scelta = 0;
		cout << "Operazioni disponibili: " << endl;
		cout << "1 - Inserimento di un nuovo appartamento" << endl;
		cout << "2 - Calcolo del prezzo minimo, medio e massimo" << endl;
		cout << "3 - Calcolo del prezzo medio degli appartamenti con superficie compresa tra due estremi prefissati" << endl;
		cout << "4 - Calcolo del numero di appartamenti composti da diversi numeri di vani" << endl;
		cout << "5 - Stampa degli appartamenti composti da un dato numero di vani" << endl;
		cout << "6 - Stampa degli appartamenti con prezzo compreso tra due estremi prefissati" << endl;
		cout << "7 - Esci" << endl << endl;
		cout << "Selezionare un'opzione: ";
		cin >> scelta;
		system("cls");

		switch (scelta) {
			// Inserimento di un nuovo appartamento
			case 1:
				inserisci_dati_appartamento(a);
				if (inserisci_appartamento(arch, a))
					cout << "Nuovo appartamento inserito" << endl <<endl;
				else
					cout << "E' stato raggiunto il massimo numero di appartamenti. Non si possono inserire ulteriori appartamenti" << endl << endl;
				system("pause");
				system("cls");
				break;
			// Calcolo del prezzo minimo, medio e massimo
			case 2:
				cout << "Prezzo minimo: " << calcola_prezzo_minimo(arch) << endl;
				cout << "Prezzo medio: " << calcola_prezzo_medio(arch) << endl;
				cout << "Prezzo massimo: " << calcola_prezzo_massimo(arch) << endl << endl;
				system("pause");
				system("cls");
				break;
			// Calcolo del prezzo medio degli appartamenti con superficie compresa tra due estremi prefissati
			case 3:
				cout << "Inserire la superficie minima: ";
				cin >> sup_min;
				cout << "Inserire la superficie massima: ";
				cin >> sup_max;
				system("cls");
				prezzo_medio = calcola_prezzo_medio_superficie(arch, sup_min, sup_max);
				cout << "Prezzo medio degli appartamenti con superficie compresa tra " << sup_min << " e " << sup_max << " mq: " << prezzo_medio << endl << endl;
				system("pause");
				system("cls");
				break;
			// Calcolo del numero di appartamenti composti da diversi numeri di vani
			case 4:
				calcola_istogramma_vani(arch, istogramma);
				stampa_istogramma_vani(istogramma);
				system("pause");
				system("cls");
				break;
			// Stampa degli appartamenti composti da un dato numero di vani
			case 5:
				cout << "Inserire un numero di vani: ";
				cin >> numero_vani;
				system("cls");
				stampa_selezione_vani(arch, numero_vani);
				system("pause");
				system("cls");
				break;
			// Stampa dei dati relativi agli appartamenti il cui prezzo e' compreso tra un valore minimo e un valore massimo
			case 6:
				cout << "Inserire il prezzo minimo: ";
				cin >> prezzo_min;
				cout << "Inserire il prezzo massimo: ";
				cin >> prezzo_max;
				system("cls");
				stampa_selezione_prezzo(arch, prezzo_min, prezzo_max);
				system("pause");
				system("cls");
				break;
			// Uscita dal programma
			case 7:
				continua = 0;
				break;
			default:
				system("cls");
				cout << "Opzione non disponibile: inserire un numero tra 1 e 7" << endl << endl;
		}

	} while (continua);
		
	return 0;
}

```

> The above command returns:

```c

```

```cpp

``` 

**Assignement 6**: 
Write a C ++ program that processes information relating to apartments for sale at a real estate agency. The following information will be stored for each apartment: the identification code (an integer), the address (a string of characters for the street and one for the municipality), number of rooms, the surface in square meters, the price. The number of apartments for sale does not exceed 100 units. The collection of apartments for sale can be created as a suitably initialized array of apartments. The program must provide the following functions: 1.Input data by the user from standard input, verifying the validity of the same (i.e. number of rooms, surface and price must be positive numbers); 2.Calculation and video printing of the average, minimum and maximum price of the apartments for sale; 3.Calculation and video printing of the average price of the apartments whose surface is between a minimum and a maximum value entered by the user; 4.Calculation and screen printing of the number of one-room apartments (n = 1), of two-room apartments (n = 2), of three-room apartments (n = 3), of apartments of 4, 5, 6, 7 and 8 rooms and those with more than 8 rooms. 5.Print on the screen of the information relating to all the apartments of nvani, with the user entering it; 6.Print on the video of the information relating to all the apartments whose price is between a val minimum hours and a maximum value entered by the user. The main function will allow the user to select one of the features provided by the program and execute the corresponding function.

**Solution**:
In progress...






### [E6][A5] 
```cpp


```

> The above command returns:

```c

```

```cpp

``` 

**Assignement 2**: 


**Solution**:



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

