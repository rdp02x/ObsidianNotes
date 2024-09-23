### Let's go
- **JavaScript** is a programming language used to make websites interactive.
- It runs directly in web browsers, allowing dynamic content like animations, forms, and games.
- JavaScript can update and change both HTML and CSS on a webpage.
- It is widely used for front-end development (what users see) and can also be used for back-end development (server-side) with Node.js.
- JavaScript is essential for creating responsive, user-friendly web experiences.
- It is easy to learn for beginners but powerful enough for complex applications.
### var vs const
- Both are ways to declare a variable.
- `var` declares the variable that can change it's value as and when needed.
- `const` declares the type variable that remains constant during the whole program execution.
### Hoisting
- Hoisting is basically when we use the variable/functions before declaring it.
- The declaration part of the variable/method moves to the top of the code
- This can be proved via this example:
  If the variable/function is not in whole code, it gives the error _Not Defined_
  whereas if it is defined anywhere in the code, but used before it, it give the value as _Undefined_.
```JavaScript
console.log(a); // This will give error 'Not-defined'
console.log(b); // This will print the value as 'undefined'
var b = 5;
```
### Data types in JavaScript 
There are 2 basic Datatypes in JavaScript:

1. Primitive Type:
	- **String:** Represents text.
	  Example -"Hello"
	- **Number:** Represents numeric values.
	  Example - 42
	- **Boolean:** Represents true or false values.
	  Example - `true`
	- **Undefined:** Represents a variable that has been declared but not assigned a value.
	- **Null:** Represents the intentional absence of any value.


1. Reference Type:
	- **Object:** A collection of key-value pairs.
	  Example - `var obj = { name: "John", age: 30 }`
	- **Array:** An ordered collection of values.
	  Example - `var arr[] = [1, 2, 3]`
	- **Function:** A block of code designed to perform a particular task.
	  Example - `function add(a, b) { return a + b; }`

| Primitive Types                             | Reference Types                                      |
| ------------------------------------------- | ---------------------------------------------------- |
| Basic data types with direct value storage. | Complex data types with reference storage.           |
| Stored in stack memory.                     | Stored in heap memory with a reference in the stack. |
| Immutable.                                  | Mutable.                                             |
| Copies the actual value.                    | Copies the reference to the object.                  |
| Compared by value.                          | Compared by reference.                               |
| Default values are predefined.              | Default value is `null`.                             |
| Automatically converted as needed.          | Requires explicit conversion.                        |
### Conditionals
- This thing include `if`, `else` and `else-if`. 
- There are parenthesis after `if` that can contain the condition i.e. true/false.
  If the condition is true, the 'if' part of the code will execute else the 'else' part of the code will execute.
```Syntax
if(true or false) {
	// code if true
} else {
	// code if false
}
```
### Loops
Something that repeats itself over and over again. It can be anything like a function or a block of code or a variable, anything.

There are 2 different loops in JavaScript - for loop & while loop.

| **`for` Loop**                                                                                   | **`while` Loop**                                                                               |
| ------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------- |
| Typically used when the number of iterations is known.                                           | Used when the number of iterations is not known beforehand.                                    |
| Syntax includes initialization, condition, and iteration expressions all in one line.            | Syntax includes only the condition; initialization and iteration are handled separately.       |
| Example: <br>`for (let i = 0; i < 5; i++) { console.log(i); }`                                   | Example: <br>`let i = 0; while (i < 5) { console.log(i); i++; }`                               |
| Executes the loop body as long as the condition is true, then increments/decrements the counter. | Executes the loop body as long as the condition is true; requires manual counter update.       |
| Easier to read and maintain when the loop logic is straightforward and related to a counter.     | More flexible; can be used for more complex conditions beyond simple counter-based iterations. |
| Best suited for situations where you need to run the loop a specific number of times.            | Best suited for situations where the loop should continue until a certain condition is met.    |
### Functions
- Functions are basically reusing a block of code. 
- A block of code is encapsulated in something we call function and give it a name. And when it is called it executes the code.
- Example: 
```javascript
function functionName(Arguments) {
	// function body
	// return statement
}
```

> [!Note]
> In any function, if there is a return statement, the function gets over there and does not execute anything coded further.
### Arguments & Parameters
- Arguments are the ones that are given in parenthesis during the function declaration. Parameter are the ones that are given at the time of function calling.
- Giving as arguments is not mandatory but if it is given, then parameter must also be given during the function call.
### Array
- Array is something that hold more than one value of same datatype in a single variable.
- An array in JavaScript can hold multiple data of different datatypes unlike other languages.
```JavaScript
var arr[] = [23, 32, 12, 44, 53, 63, 9812]; // Declaration

// Accessing elements of an array. (Index starts from zero)
arr[1] // 32
arr[4] // 53
```

>[!NOTE]
>To add or remove elements from an array whose total elements are unknown, we use different built-in functions that can add elements at beginning or at end.
### Push Pop Shift Unshift
- **`push()`** - Adds one or more elements to the end of an array.
  Example: `arr.push(4); // [1, 2, 3, 4]`
  
- **`pop()`** - Removes the last element from an array.
  Example: `arr.pop(); // [1, 2, 3]`

- **`shift()`** - Removes the first element from an array.
  Example: `arr.shift(); // [2, 3]`

- **`unshift()`** - Adds one or more elements to the beginning of an array.
  Example: `arr.unshift(0); // [0, 1, 2, 3]`
### Objects
- A datatype that holds multiple data in key value pairs.
- For Example: If I want to store all information about a person I can do it in object in JavaScript.
```JavaScript
// This object is filled object that is storing data inside it.
var obj = {
	name: "Rishabdev Panchal",
	age: 19,
	city: "Vadodara"
};

var obj1 = {}; 
// This is a blank object that has no data stored in it.

// Data inside the objects can be accessed via:
obj.name = "Rishabdev K. Panchal"; // This will change the name value.
```
- Objects are very similar to _Dictionary_ datatype in Python.