# Theory_of_Java

<img src="https://upload.wikimedia.org/wikipedia/en/thumb/3/30/Java_programming_language_logo.svg/242px-Java_programming_language_logo.svg.png" width="128"/>


# # Data Types


```java
public class first_prog {

	public static void main(String[] args) {
		
// DATA TYPES BELOW:

		int number = 68; // creating int value
		

		String text = "lol"; // creating str value
				
		
		boolean open = false; // creating bool value
		

		float fl_num = 6.9f; // creating float value - need to add "f" in the end ( float = float32 )
		
		
		double db_num = 6.345345345345345345345723546344656456465f; // double = float64
		
		
		char ch_num = 'a'; // creating char
		
		
		int num = 68, num1 = 69; // declaring 2 int on the same line
		
	}

}
```

# Comments

# Java Comments

In computer programming, comments are a portion of the program that are completely ignored by Java compilers. They are mainly used to help programmers to understand the code. For example,

```java
// declare and initialize two variables
int a =1;
int b = 3;

// print the output
System.out.println("This is output");

```

Here, we have used the following comments,

- declare and initialize two variables
- print the output

---

# Types of Comments in Java

In Java, there are two types of comments:

- single-line comment
- multi-line comment

---

### **Single-line Comment**

A single-line comment starts and ends in the same line. To write a single-line comment, we can use the `//` symbol. For example,

```java
// "Hello, World!" program example

class Main {
    public static void main(String[] args) {
        // prints "Hello, World!"
        System.out.println("Hello, World!");
    }
}

```

**Output**:

```
Hello, World!

```

Here, we have used two single-line comments:

- "Hello, World!" program example
- prints "Hello World!"

The Java compiler ignores everything from `//` to the end of line. Hence, it is also known as **End of Line** comment.

---

### **Multi-line Comment**

When we want to write comments in multiple lines, we can use the multi-line comment. To write multi-line comments, we can use the /*....*/ symbol. For example,

```java
/* This is an example of  multi-line comment.
 * The program prints "Hello, World!" to the standard output.
 */

class HelloWorld {
    public static void main(String[] args) {

        System.out.println("Hello, World!");
    }
}

```

**Output**:

```
Hello, World!

```

Here, we have used the multi-line comment:

```java
/* This is an example of multi-line comment.
* The program prints "Hello, World!" to the standard output.
*/

```

This type of comment is also known as **Traditional Comment**. In this type of comment, the Java compiler ignores everything from `/*` to `*/`.


# Input / Output

# Java Output

In Java, you can simply use

```java
System.out.println(); or

System.out.print(); or

System.out.printf();

```

to send output to standard output (screen).

Here,

- `System` is a class
- `out` is a `public` `static` field: it accepts output data.

Let's take an example to output a line.

```java
class AssignmentOperator {
    public static void main(String[] args) {

        System.out.println("Java programming is interesting.");
    }
}

```

**Output**:

```
Java programming is interesting.

```

Here, we have used the `println()` method to display the string.

---

### **Difference between println(), print() and printf()**

- `print()` - It prints string inside the quotes.
- `println()` - It prints string inside the quotes similar like `print()` method. Then the cursor moves to the beginning of the next line.
- `printf()` - It provides string formatting.

---

### **Example: print() and println()**

```java
class Output {
    public static void main(String[] args) {

        System.out.println("1. println ");
        System.out.println("2. println ");

        System.out.print("1. print ");
        System.out.print("2. print");
    }
}

```

**Output**:

```
1. println
2. println
1. print 2. print

```

In the above example, we have shown the working of the `print()` and `println()`methods. To learn about the `printf()` method, visit [Java printf()](https://www.cs.colostate.edu/~cs160/.Summer16/resources/Java_printf_method_quick_reference.pdf).

---

### **Example: Print Concatenated Strings**

```java
class PrintVariables {
    public static void main(String[] args) {

        Double number = -10.6;

        System.out.println("I am " + "awesome.");
        System.out.println("Number = " + number);
    }
}

```

**Output**:

```
I am awesome.
Number = -10.6

```

---

# Java Input

Java provides different ways to get input from the user. However, in this tutorial, you will learn to get input from user using the object of `Scanner` class.

In order to use the object of `Scanner`, we need to import `java.util.Scanner` package.

```java
import java.util.Scanner;

```

To learn more about importing packages in Java, visit [Java Import Packages](https://www.programiz.com/java-programming/packages-import).

Then, we need to create an object of the `Scanner` class. We can use the object to take input from the user.

```java
// create an object of Scanner
Scanner input = new Scanner(System.in);

// take input from the user
int number = input.nextInt();

```

**Similarly, we can use `nextLong()`, `nextFloat()`, `nextDouble()`, and `next()` methods to get `long`, `float`, `double`, and `string` input respectively from the user.**

---

### **Example: Get Integer Input From the User**

```java
import java.util.Scanner;

class Input {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

        System.out.print("Enter an integer: ");

        int number = input.nextInt();

        System.out.println("You entered " + number);

        // closing the scanner object
        input.close();
    }
}

```

**Output**:

```
Enter an integer: 23
You entered 23

```

**Note**: We have used the `close()` method to close the object. It is recommended to close the scanner object once the input is taken.


# Operators

# 1. Java Arithmetic Operators

Arithmetic operators are used to perform arithmetic operations on variables and data. For example,

```java
a + b;
```

Here, the `+` operator is used to add two variables a and b. Similarly, there are various other arithmetic operators in Java.

| Operator | Operation |
| --- | --- |
| + | Addition |
| - | Subtraction |
| * | Multiplication |
| / | Division |
| % | Modulo Operation (Remainder after division) |

**Division Operator ( / )**

Note the operation, `a / b` in our program. The `/` operator is the division operator.

If we use the division operator with two integers, then the resulting quotient will also be an integer. And, if one of the operands is a floating-point number, we will get the result will also be in floating-point.

```java
In Java,

(9 / 2) is 4
(9.0 / 2) is 4.5
(9 / 2.0) is 4.5
(9.0 / 2.0) is 4.5
```

**Modulo Operator ( % )**

The modulo operator `%` computes the remainder. When `a = 7` is divided by `b = 4`, the remainder is **3**.

**Note**: The `%` operator is mainly used with integers.

---

# 2. Java Assignment Operators

Assignment operators are used in Java to assign values to variables. For example,

```java
int age;
age = 5;
```

Here, `=` is the assignment operator. It assigns the value on its right to the variable on its left. That is, **5** is assigned to the variable age.

Let's see some more assignment operators available in Java.

| Operator | Example | Equivalent to |
| --- | --- | --- |
| = | a = b; | a = b; |
| += | a += b; | a = a + b; |
| -= | a -= b; | a = a - b; |
| *= | a *= b; | a = a * b; |
| /= | a /= b; | a = a / b; |
| %= | a %= b; | a = a % b; |

---

# 3. Java Relational Operators

Relational operators are used to check the relationship between two operands. For example,

```java
// check if a is less than b
a < b;
```

Here, `<` operator is the relational operator. It checks if a is less than b or not.

It returns either `true` or `false`.

| Operator | Description | Example |
| --- | --- | --- |
| == | Is Equal To | 3 == 5 returns false |
| != | Not Equal To | 3 != 5 returns true |
| > | Greater Than | 3 > 5 returns false |
| < | Less Than | 3 < 5 returns true |
| >= | Greater Than or Equal To | 3 >= 5 returns false |
| <= | Less Than or Equal To | 3 <= 5 returns true |

---

# 4. Java Logical Operators

Logical operators are used to check whether an expression is `true` or `false`. They are used in decision making.

| Operator | Example | Meaning |
| --- | --- | --- |
| && (Logical AND) | expression1 && expression2 | true only if both expression1 and expression2 are true |
| || (Logical OR) | expression1 || expression2 | true if either expression1 or expression2 is true |
| ! (Logical NOT) | !expression | true if expression is false and vice versa |

### **Example:**

```java
class Main {
  public static void main(String[] args) {

    // && operator
    System.out.println((5 > 3) && (8 > 5));  // true
    System.out.println((5 > 3) && (8 < 5));  // false

    // || operator
    System.out.println((5 < 3) || (8 > 5));  // true
    System.out.println((5 > 3) || (8 < 5));  // true
    System.out.println((5 < 3) || (8 < 5));  // false

    // ! operator
    System.out.println(!(5 == 3));  // true
    System.out.println(!(5 > 3));  // false
  }
}
```

---

# 5. Java Unary Operators

Unary operators are used with only one operand. For example, `++` is a unary operator that increases the value of a variable by **1**. That is, `++5` will return **6**.

Different types of unary operators are:

| Operator | Meaning |
| --- | --- |
| + | Unary plus: not necessary to use since numbers are positive without using it |
| - | Unary minus: inverts the sign of an expression |
| ++ | Increment operator: increments value by 1 |
| -- | Decrement operator: decrements value by 1 |
| ! | Logical complement operator: inverts the value of a boolean |

# Increment and Decrement Operators

Java also provides increment and decrement operators: `++` and `--` respectively. `++`increases the value of the operand by **1**, while `--` decrease it by **1**. For example,

```java
int num = 5;

// increase num by 1
++num;

// decrease num by 1
--num;
```

# If / Else

# 1. Java if (if-then) Statement

The syntax of an **if-then** statement is:

```java
if (condition) {
  // statements
}
```

Here, condition is a boolean expression such as `age >= 18`.

- if  evaluates to `true`, statements are executed
    
    condition
    
- if  evaluates to `false`, statements are skipped
    
    condition
    

---

### **Example:**

```java
class IfStatement {
  public static void main(String[] args) {

    int number = 10;

    // checks if number is less than 0
    if (number < 0) {
      System.out.println("The number is negative.");
    }

    System.out.println("Statement outside if block");
  }
}
```

**Output**

```
Statement outside if block
```

---

# 2. Java if...else (if-then-else) Statement

The `if` statement executes a certain section of code if the test expression is evaluated to `true`. However, if the test expression is evaluated to `false`, it does nothing.

In this case, we can use an optional `else` block. Statements inside the body of `else`block are executed if the test expression is evaluated to `false`. This is known as the **if-...else** statement in Java.

The syntax of the **if...else** statement is:

```java
if (condition) {
  // codes in if block
}
else {
  // codes in else block
}
```

---

# 3. Java if...else...if Statement

In Java, we have an **if...else...if** ladder, that can be used to execute one block of code among multiple other blocks.

```java
if (condition1) {
  // codes
}
else if(condition2) {
  // codes
}
else if (condition3) {
  // codes
}
else {
  // codes
}
```

### **Example:**

```java
class Main {
  public static void main(String[] args) {

    int number = 0;

    // checks if number is greater than 0
    if (number > 0) {
      System.out.println("The number is positive.");
    }

    // checks if number is less than 0
    else if (number < 0) {
      System.out.println("The number is negative.");
    }

    // if both condition is false
    else {
      System.out.println("The number is 0.");
    }
  }
}
```

**Output**

```
The number is 0.
```

---


# Switch Statement

# Java switch Statement

The `switch` statement allows us to execute a block of code among many alternatives.

The syntax of the `switch` statement in Java is:

```java
switch (expression) {

  case value1:
    // code
    break;

  case value2:
    // code
    break;

  default:
    // default statements

  }
```

---

# Example: Java switch Statement

```java
// Java Program to check the size
// using the switch...case statement

class Main {
  public static void main(String[] args) {

    int number = 44;
    String size;

    // switch statement to check size
    switch (number) {

      case 29:
        size = "Small";
        break;

      case 42:
        size = "Medium";
        break;

      // match the value of week
      case 44:
        size = "Large";
        break;

      case 48:
        size = "Extra Large";
        break;

      default:
        size = "Unknown";
        break;

    }
    System.out.println("Size: " + size);
  }
}
```

**Output**:

```
Size: Large
```

In the above example, we have used the switch statement to find the size. Here, we have a variable number. The variable is compared with the value of each case statement.

Since the value matches with **44**, the code of `case 44` is executed.

```java
size = "Large";
break;
```

Here, the size variable is assigned with the value `Large`.

---

# Break statement in Java switch...case

Notice that we have been using `break` in each case block.

```java
 ...
case 29:
  size = "Small";
  break;
...
```

The `break` statement is used to terminate the **switch-case** statement. If `break` is not used, all the cases after the matching case are also executed. For example,

```java
class Main {
  public static void main(String[] args) {

    int expression = 2;

    // switch statement to check size
    switch (expression) {
      case 1:
        System.out.println("Case 1");

        // matching case
      case 2:
        System.out.println("Case 2");

      case 3:
        System.out.println("Case 3");

      default:
        System.out.println("Default case");
    }
  }
}
```

**Output**

```
Case 2
Case 3
Default case
```

---

# Default case in Java switch-case

The switch statement also includes an **optional default case**. It is executed when the expression doesn't match any of the cases. For example,

```java
class Main {
  public static void main(String[] args) {

    int expression = 9;

    switch(expression) {

      case 2:
        System.out.println("Small Size");
        break;

      case 3:
        System.out.println("Large Size");
        break;

      // default case
      default:
        System.out.println("Unknown Size");
    }
  }
}
```

**Output**

```
Unknown Size
```

In the above example, we have created a **switch-case** statement. Here, the value of expression doesn't match with any of the cases.

Hence, the code inside the **default case** is executed.

```java
default:
  System.out.println("Unknown Size);
```

# While Loop

# Java while loop

Java `while` loop is used to run a specific code until a certain condition is met. The syntax of the `while` loop is:

```java
while (testExpression) {
    // body of loop
}
```

---

# Flowchart of while loop

!https://cdn.programiz.com/sites/tutorial2program/files/java-while-loop.png

---

### **Example: Display Numbers from 1 to 5**

```java
// Program to display numbers from 1 to 5

class Main {
  public static void main(String[] args) {

    // declare variables
    int i = 1, n = 5;

    // while loop from 1 to 5
    while(i <= n) {
      System.out.println(i);
      i++;
    }
  }
}
```

**Output**

```
1
2
3
4
5
```

---

### **Infinite while loop**

If **the condition** of a loop is always `true`, the loop runs for infinite times (until the memory is full). For example,

```java
// infinite while loop
while(true){
    // body of loop
}
```

In the above programs, the **textExpression** is always `true`. Hence, the loop body will run for infinite times.

