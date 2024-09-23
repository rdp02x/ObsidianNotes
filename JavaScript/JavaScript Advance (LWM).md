### The Difference between `var`, `let`, and `const`

| var                               | let / const                       |
| --------------------------------- | --------------------------------- |
| Thing from JavaScript ES5 version | Thing from JavaScript ES6 version |
| Function Scoped                   | Braces Scoped                     |
| Adds itself to the window object  | Dosen't adds to the window object |
### Window Object
- All the features that are not the part of JavaScript but we still use that, we use are from something we call a Window Object. 
- The Window is something from which JavaScript uses the features that it doesn't have, it borrows it from the **Browser**.
- Eg. AlertBox, Console, etc.
- To check all the things that are not the part of JavaScript, we can go to Console, and type the command `window`. I'll display all the thing that are not part of JavaScript.

### Browser Context API
Browser basically provides three things:
  1. Window (Object)
  2. Stack (Memory)
  3. Heap (Memory)
#### Stack
The order in which the things execute.
#### Heap
The variable/intermediate data that takes the storage is in **Heap Memory**.

### Execution Context and Lexical Environment
It is an imaginary box that is being created when a function is called after it's creation. It contains 3 thing:
1. Variables of that function
2. Other functions that this parent function has
3. Lexical Environment
#### Lexical Environment
Its something that tell the function what thing are accessible and what things are not. Basically, holds the scope chain.

### How to copy Reference Values
```JavaScript
var a = [1, 2, 3];
var b = [...a]; 

// [1, 2, 3] becomes that value of variable b.
// ...  is the spread operator.
// This format is applicable for objects also.
```

### Truthy and Falsy
- Everything is JavaScript belongs to 2 things - **Truthy** or **Falsy**.
- Falsy Values (values that eventually get converted to `false`):
  - 0
  - false
  - undefined
  - null
  - NaN (Not a Number)
  - document.all
- Truthy Values (values that eventually get converted to `true`):
  Everything else other than falsy.

### Foreach and ForIn loops
##### forEach()
- This loop is generally used while iterating over an array.
- This loop by default doesn't makes changes in the original array, instead it makes changes in a temp array that is created.
```JavaScript
var arr = [1, 2, 5, 5, 1, 7, 6, 5];

arr.forEach(function(val) {
	console.log(val);
});
```

##### forin()
- This loop is used to iterate over objects
```JavaScript
var obj = {
	Name: "Rishabdev",
	Age: 20,
	City: "Vadodara"
};

for(var key in obj) {
	console.log(key, obj[key]);
}

// 'key' variable prints the object's key.
// 'obj[key]' prints the value of the key.
```

### Callback Functions
- A block of code that wants executes after it completing its task, then the **callback function** informs it to execute.
```JavaScript
setTimeout(function () {
	console.log("Hello, I was called by a Callback Function");
}, 3000);

// This block of code will execute after 3000 miliseconds (3 sec)
```

> [!NOTE] Note
> This is a part of Asynchronous JavaScript.

### First Class Functions
- Functions in JavaScript can also be treated as variable values, and hence can be used as parameters of another functions
- For Example
  ```JavaScript
  function sample(demo) {
	  demo();
  }

  sample(function demo() {
	  console.log("This is first-class functions example");
  })
```

