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

  sdt::cout << "Enter coefficients a, b and c: ";
  sdt::cin >> a >> b >> c;

  discriminant = b*b - 4*a*c;
  
  if (discriminant > 0) {
    x1 = (-b + sqrt(discriminant)) / (2*a);
    x2 = (-b - sqrt(discriminant)) / (2*a);
    cout << "Roots are real and different." << endl;
    sdt::cout << "x1 = " << x1 << sdt::endl;
    sdt::cout << "x2 = " << x2 << sdt::endl;
  } 
  else if (discriminant == 0) {
    sdt::cout << "Roots are real and same." << sdt::endl;
    x1 = -b/(2*a);
    sdt::cout << "x1 = x2 =" << x1 << sdt::endl;
  }
  else {
    realPart = -b/(2*a);
    imaginaryPart =sqrt(-discriminant)/(2*a);
    sdt::cout << "Roots are complex and different."  << sdt::endl;
    sdt::cout << "x1 = " << realPart << "+" << imaginaryPart << "i" << sdt::endl;
    sdt::cout << "x2 = " << realPart << "-" << imaginaryPart << "i" << sdt::endl;
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


## Lessons code 2/12/2020
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

