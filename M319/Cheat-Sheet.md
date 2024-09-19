#exams #M319 #theory 
# Problems, Solutions and Stakeholders
[[Analysing Problems |Here is the problem and solution space stuff]]
[[User Stories|Here the user story stuff]]

# Variables and Constants
[[Datatypes|this is the theory we have]]

## Variables
Variables are storage locations in memory with a specific data type, which determines which kind of data they can hold along with the amount of requires memory to store the actual value

### Declaring Variables
We declare variables by specifying the data type followed by the variable's name
```Cs
int age;
string name;
double salary;
```
We can either initialize a variable at the time of declaration or later in the code 
```Cs
// Declaring a variable and assigning a value later
int age;
age = 30

string name;
name = "John Cena";

//Declaring a variable and immediately assigning a value
double salary = 500000.00;
bool isProgrammer = true;
```
### Declaration vs. Definition
The difference between these 2 is pretty important, cause they are not the same
When declaring a variable, we specify the name and the data type of the variable. (For local variables, no memory is allocated)
We can only declare a variable once and only before we define it (who would have thought that)
```Cs
//Declaring only
int age;

//Declaring and defining at once
string name = "Obama"

//Defining a previously declared variable
age = 9000;
```

## Constants

Constants are similar to variables (no shit sherlock, why else would they be packaged together)
We use the 'const' keyword to declare constants

```Cs
const couble Pi = 3.14159;
const int DaysInWeek = 7;
```
Constants must be initialized at the time of declaration
Their values **cannot** be modified later

## Naming 
- Names can't contain spaces
- Allowed characters are letters (a-z/ A-Z), digits (0-9) and the underscore
- Identifiers (Names) must start with a letter
- Identifiers must be different from reserved keywords in C# (be creative)
---
- **PascalCase**: Each word starts with an uppercase letter, with no spaces or underscores. Used for class names, method names, and properties.  
    Example: `MyClass`, `CalculateTotal`
    
- **camelCase**: The first word starts with a lowercase letter, and subsequent words start with an uppercase letter. Used for local variables, method parameters, and private fields.  
    Example: `myVariable`, `calculateTotal`
    
- **snake_case**: Words are written in lowercase and separated by underscores. Rarely used in C# but can be seen in some legacy code or constants in certain contexts.  
    Example: `my_variable`
    
- **kebab-case**: Words are written in lowercase and separated by hyphens. Not used in C#, as hyphens are not allowed in identifiers. Common in URLs and CSS.  
    Example: `my-variable` (**not valid in C#**)
---


# Data Types
#datatypes 
[[Datatypes#[]( data-types)Data Types|Here the theory]]

Yeah there also are primitive vs. complex data types
Primitive data types are used to store simple values like a number or a character.
So the whole list I linked to, except strings, those are arrays of chars
strings are complex data types cause they store more than just a single value

- implicit 
implicit data types refer to types that the compiler infers automatically based on the assigned value.
The most common way to use implicit typing in C# is with the 'var' keyword
- explicit
explicit data types refer to types not inferred by the complier, but are set by the developer when writing the code 

## Arrays
What arrays are and what use cases they have I know.
Here I am just going to put the possible ways to initialize an array
```cs
//'numbers' array that stores integers
int[] numbers = { 3, 14, 59};

//'strings' array that stores strings
string[] strings = new string[] { "John", "Biden", "Trump"};
```
declaring an array 
```cs
//Declaring an array of length 8 without setting values
string[] stringArray = new string[8]

//Defining an array by setting its initial values
int[] intArray = new int[] {3, 4, 5};
```
declaring **and** initializing an array
one way to do that is by directly assigning values to the array
```cs
//both these arrays are declared and initialized with values
int[] numbers = { 1, 2, 5, -10, 8};
string[] animals = { "shark", "bear", "dog", "raccoon" };
```
if we want to access a specific index of the array, we do that by calling the array and and then putting the index we want in the square brackets
```cs
// Initialize an array with 6 values.
int[] numbers = { 3, 14, 59, 26, 53, 0 };
// Assign the last element, the 6th number in the array (currently 0), to 58.
numbers[5] = 58;
// Store the first element, 3, in the variable `first`.
int first = numbers[0];
```
if we want to write out every single value of an array, we can do this with a for loop
```cs
int[] evenNumbers = { 2, 4, 6, 8, 10}

for (int i = 0; i < evenNumbers.Length; i++)
{
	Console.WriteLine(evenNumbers[i])
}
```

 #whilePreppingForTest #randomInputs
 I was doing the exercise where I have to add Items to an array with some logic being done for the price. so this is what i did to do that, seems important
```Cs
void viewInventory()

{

    // Add "17 Carrots" to the first available slot in the Basket array

    for (int i = 0; i < Basket.Length; i++)

    {

        if (Basket[i] == null)

        {

            Basket[i] = "17 Carrots";

            Console.WriteLine("Added 17 Carrots to your basket.");

            break;

        }

    }

}
```
# Functions
[[Functions|Here is the script we got for functions]]
*All the theory I am leaving for the script to explain*
and this is how to make a function
```cs
<type of return value> <name of function>(<parameter list>)
{
    <instructions>   // content of function, also called "body"
}
```
## technical terms
- **Head/Signature**: The function's declaration line, which includes the function name, return type, and parameter list. It defines the structure and how the function can be invoked.
    
- **Body**: The block of code within the function that performs the operation or task. It contains the statements that execute when the function is called.
    
- **Parameter List**: A list of variables defined in the function signature that receive values when the function is called. These parameters act as placeholders for the input data that the function will process.
    
- **Arguments**: The actual values passed to the function when it is invoked. These values are assigned to the corresponding parameters in the parameter list.
    
- **Return Value**: The result that a function provides after completing its task. It is the output of the function, sent back to the caller.
    
- **Data Type of Return Value (Return Type)**: The type of data the function is expected to return, such as `int`, `string`, or `void` (if no value is returned). This is specified in the function's signature.
# Control Structures
*just check RassUp if I need to see something in action*
## if/ else (else if)
Executes a block of code if a condition is true, else it executes other block of code
```cs
if (condition)
{
	/* code */
} else if (another condition)
{
	/* code */
} else 
{
	/* code */
}
```

## switch
Tests a variable against a list of possible values ('case') and executes the corresponding block of code
always have a default (fallback) if none of the cases match
```cs
switch (value) {
	case 1: /* code */ break;
	case 2: /* code */ break;
	default: /* code */ break;
}
```

## Ternary Conditional Operator (?:)
A shorthand for 'if-else', evaluates a condition and returns one of two values based on the result
```cs
result = (condition) ? valueIfTrue : valueIfFalse;
```

## for 
Repeats a block of code a specified number of times
Used when we know the exact number of times the code should be executed
```cs
for (int i = 0; i < limit; i++) { /* code */ }
```

## foreach
Iterates over elements in a collection (like arrays or lists) and executes a block of code for each element
Used when **we don't know how many times** the code should get executed, good when amount of times **changes**
```cs
foreach (var item in collection) { /* code */ }
```

## while 
Repeats a block of code while the condition is true 
checks if condition is true **before** executing the code for the first time
```cs
while (condition) { /* code */ };
```

## do while
Like while, but executes the code once before checking the condition, so the minimum times the code gets executed is **once**
```cs
do { /* code */ }
while (condition);
```

# Code quality
*thx chat gbt uwu*
- **Code Quality in Teams**: Developing in teams requires attention to code quality, including consistency, readability, and maintainability, with challenges like differing styles but opportunities for peer review and shared standards.
    
- **Improving Code Quality**: Apply best practices such as proper structure, meaningful comments, and adherence to coding conventions to ensure clear, maintainable code.
    
- **Forms of Comments in C#**:
    
    - **Single-line** (`//`): For brief comments on a single line.
    - **Multi-line** (`/* */`): For longer comments spanning multiple lines.
    - **XML Documentation Comments** (`///`): For generating documentation with detailed summaries of methods, classes, etc.
- **Coding Conventions**: Follow established rules for naming identifiers, consistent spacing, placement of braces, and proper line breaks to ensure readability and maintainability.
    
- **Setting Breakpoints and Debugging**: Use breakpoints in an IDE to pause execution and step through code, allowing precise inspection of the program’s flow and logic.
    
- **IDE Proficiency**: Use an IDE efficiently by utilizing features like automatic formatting, debugging tools, and code suggestions to improve productivity and accuracy.
    
- **Compiler and Runtime Errors**: Understand and handle common compiler errors (e.g., syntax errors) and runtime errors (e.g., null references) by following clear error messages and debugging the code to resolve issues.