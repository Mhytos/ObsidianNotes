#theory #datatypes
## Variables and Constants

### [](#introduction)Introduction

In programming, variables and constants are essential components that store data values. Understanding how to use them effectively is crucial for writing efficient and maintainable code. This document provides an in-depth look at variables, constants, and the most important, primitive data types in C#.

Understanding variables, constants, and data types is fundamental to programming in C#. By using them effectively, you can write clear, efficient, and maintainable code. This guide should help you grasp these concepts and apply them in your C# programs.

---

### [](#variables)Variables

Variables are storage locations in memory with a specific data type, which determines the kind of data they can hold along with the amount of memory required to store the actual information (value). A variable's value can be changed during program execution.

#### [](#declaring-variables)Declaring Variables

In C#, variables are declared by specifying the **data type** followed by the variable's **name**.

Some examples:

```
int age;
string name;
double salary;
```

#### [](#defining-variables)Defining Variables

Variables can be initialized at the time of declaration or later in the code.

```
// Declare a variable and LATER assign a value
int age;
age = 30;

string name;
name = "Alice";

// Declare a variable and IMMEDIATELY assign a value
double salary = 50000.00;
bool isProgrammer = true;
```

#### [](#declaration-vs-definition)Declaration vs. Definition

It is important that _declaration_ and _definition_ is not the same. When you _declare_ a variable you specify the **data type** and the **name** of the variable. For _local variables_, **no memory** is allocated. When you define it, you additionally assign a value to the variable.

The declaration can only be done once and must happen always before the definition. The declaration and definition can be done at the same time. The definition can only be done, if the variable previously was declared.

```
// Declaration only
int age;

// Declaration and definition at once
string name = "Alice";

// Definition of a previously declared variable
age = 5000;

// Not possible (results in compiler error):
// Definition before declaration
salary = 600;   // ERROR!
double salary;

// Also not possible (results in compiler error):
// Use of an undefined variable.
bool isProgrammer;
Console.WriteLine(isProgrammer);    // ERROR!
```

### [](#constants)Constants

Constants are similar to variables, but their values cannot be changed once they are initialized. They are declared using the `const` keyword.

```
const double Pi = 3.14159;
const int DaysInWeek = 7;
```

Constants must be initialized at the time of declaration and their values cannot be modified later.

> Try to find an explanation: _Why is it not possible to declare constants without assigning a value?_

### [](#names-of-constants-and-variables)Names of Constants and Variables

It is important that the names of variables and constants are always **one word**! It is possible to concatenate multiple words, but they cannot be divided by spaces. For example, `daysInWeek` is a valid name (also known as `identifier`).

There are other important _rules_ and _conventions_ to consider for identifiers:

#### [](#rules-for-identifiers)Rules for Identifiers

- Allowed characters are letters `a`-`z`and `A`-`Z`, digits `0`-`9` and the underscore `_`.
- The identifier must start with a letter.
- Identifiers in C# are case sensitive.
- Identifiers must be different from [reserved keywords in C#](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/) (such as `new`, `class`, `long`, `if`, `while`, ...)

#### [](#conventions-for-identifiers)Conventions for Identifiers

- Identifiers should be self descriptive.
- Avoid single-letter identifiers (except from loop counters).
- For local variables in C# use camelCase where the first letter is lowercase.
- Avoid abbreviations unless they are widely understood and accepted (such as `id` for _identifier_)
- Identifiers for boolean data types are often prefixed to indicate a true/false condition. They often start with `is`, `has` or `can`.
- Use consistent singular and plural forms for single or multiple values respectively.
- Try to stick to terms relevant for the field you program for.

## [](#data-types)Data Types

C# is a strongly typed language, meaning every variable and constant must have a data type. Further more, the type of a variable cannot change during the whole execution of a program.

> This is not true for all programming languages. As you might already know, in JavaScript or Python, you can sequentially assign values of different types to the same variable.

Bellow you find a list of some of the most important data types in C#.

### [](#overview-some-primitive-data-types-in-c)Overview: Some Primitive Data Types in C#

| Category                       | Data Type | Description                                             | Information about ranges/precision                             | Example                         |
| ------------------------------ | --------- | ------------------------------------------------------- | -------------------------------------------------------------- | ------------------------------- |
| **Numbers (without decimals)** | `byte`    | 8-bit unsigned integer                                  | Range: 0 to 255                                                | `byte level = 255;`             |
|                                | `short`   | 16-bit signed integer                                   | Range: -32,768 to 32,767                                       | `short temperature = -10;`      |
|                                | `int`     | 32-bit signed integer                                   | Range: -2,147,483,648 to 2,147,483,647                         | `int age = 30;`                 |
|                                | `long`    | 64-bit signed integer                                   | Range: -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | `long distance = 1234567890L;`  |
| **Numbers (with decimals)**    | `float`   | 32-bit single-precision floating point                  | Precision: ~6-9 digits                                         | `float height = 5.9f;`          |
|                                | `double`  | 64-bit double-precision floating point                  | Precision: ~15-17 digits                                       | `double distance = 12345.6789;` |
|                                | `decimal` | 128-bit precise decimal type for financial calculations | Precision: 28-29 digits                                        | `decimal price = 19.99m;`       |
| **Boolean Type**               | `bool`    | Represents a Boolean value (`true` or `false`)          |                                                                | `bool isAlive = true;`          |
| **Characters**                 | `char`    | Represents a single 16-bit Unicode character            |                                                                | `char grade = 'A';`             |
|                                | `string`  | Represents a sequence of characters                     |                                                                | `string name = "Alice";`        |

### [](#primitive-data-types-vs-complex-data-types)Primitive Data Types vs. Complex Data Types

Primitive data types are the basic types you can use in C#. They store a simple value like a number or a character. The list above shows some of the most important primitive types - with the exception of **string**. The datatype `string` is one of the most used _complex_ data types. It is considered a complex type since its value is composed out of multiple other values of atomic type. More specifically, `string` is a special case of an array (as you will learn more about soon).

If you are interested in more details regarding primitive and complex data types, you might wand to read this article on LinkedIn: [https://www.linkedin.com/pulse/primitive-types-non-primitive-c-vikram--xramf](https://www.linkedin.com/pulse/primitive-types-non-primitive-c-vikram--xramf)