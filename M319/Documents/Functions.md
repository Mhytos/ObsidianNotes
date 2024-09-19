> Procedural programming supplements the imperative concept of successive commands with the approach of breaking down an algorithm into manageable parts. Depending on the programming language, these parts are called subroutine, routine, procedure or function.
> 
> _Source: [Wikipedia](https://de.wikipedia.org/wiki/Prozedurale_Programmierung)_

Functions are thus a means of **breaking down an algorithm into manageable parts**. The terms _subroutine_, _routine_ or _procedure_ are rather uncommon in C#. Functions are also rather exotic language constructs in C#. Typically, applications are developed with C# using an object-oriented or class-based approach. Here, "functions" are written within a _class_ and are therefore referred to as _methods_.

For the moment - without more detailed knowledge of object-oriented programming - this terminology is not particularly relevant. For the time being, it is sufficient to know that _functions_ and _methods_ are "the same" constructs, which are referred to differently depending on where they are defined. It is also helpful to know that all knowledge about _functions_ can later be applied directly to _methods_.

## [](#definition-of-function)Definition of function

A function can be defined by combining instructions into a code block and naming them. Each function therefore has a **name**. In addition to this name, the **type of the return value** and a **parameter list** can be defined for a function. The actual content of the function, the instructions, are written between curly braces.

```
<type of return value> <name of function>(<parameter list>)
{
    <instructions>   // content of function, also called "body"
}
```

The three components that are listed before the content of the method, type of return value, function name and parameter list, are collectively referred to as **signature**.

### [](#type-of-return-value)Type of return value

A function can, but does not have to, return a value. The return of a value is done by a statement which is introduced with the keyword `return`. If a value is returned, the data type of this return value must be listed in the signature. This indicates that each call to this function will result in the return of a value of the specified data type. If the function returns _no value_, the keyword `void` is listed instead of a data type.

> You can regard the return value of a function as an _answer_. Calling this function then corresponds to a question. This question is answered with an answer in a specific form (data type). There are also special “questions” (or: orders) that do not require an answer. These functions are labeled with `void`.

### [](#function-name)Function name

The name of the function is basically freely selectable. The same rules apply as for all other _identifiers_ (for example, also for the names of variables). Valid characters include upper and lower case letters, numbers and the underscore (`_`). The name must begin with a letter. Because _methods_ are written _uppercase_ according to common convention (_PascalCase_), this convention can also be applied to _functions_.

Further conventions for the choice of function names:

- The use of verbs is common: `CalculateAverage`, `ShowResult`, `SendMessage`, ...
- Prefix `Is` or `Has` for methods with a return value of the data type `boolean`: `HasBirthday`, `IsBiggerThanAverage`, ...

### [](#parameter-list)Parameter list

A list of parameters, possibly empty, is given for each function. Each parameter in this list is defined by a data type and a name. The value of a parameter is specified when the function is called and can be used within the function by naming the corresponding parameter name. The names of the individual parameters within the parameter list must be unique. There are no restrictions regarding the data types - any number of parameters of each data type may be used. The order of the parameters is freely selectable when defining the function - however, when calling the function, the order according to the parameter list must be adhered to.

## [](#calling-a-function)Calling a function

A function is called by stating its function name and specifying values for all (non-optional) parameters. These values are then called _arguments_. The order of the arguments and their data types according to the function definition must match.

Any return value of the function can be used for an assignment or within an expression.

## [](#examples)Examples

In the following code example, some functions are defined and called.

```cs
// Function without return value (void) and three parameters.
void PrintAverage(int a, int b, int c)
{
    float average = (a + b + c) / 3.0f;
    Console.WriteLine($"Average of {a}, {b} and {c} is: {average}");
}

// Call function PrintAverage
PrintAverage(2, -4, 8); // Average of 2, -4 and 8 is: 2

// Function which returns a boolean value and takes two parameters.
bool IsAboveAverage(int valueToCheck, int[] numbers)
{
    float average = 0;
	for (int i = 0; i < numbers.Length; i++)
	{
		average += numbers[i] / (float)numbers.Length;
	}
	
	return valueToCheck > average;
}

int myFavoriteNumber = 9;

// The return value of the function is used as the condition.
if (IsAboveAverage(myFavoriteNumber, new int[] {2, 8, -1, 19, 3}))
{
    Console.WriteLine($"Yeah, {myFavoriteNumber} is above average!");
}
```