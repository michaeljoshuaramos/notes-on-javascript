```js
// Create an alias for console.log
const log = console.log;

// Basic Data Types in JS
log("------------ Basics ------------");
const aNumber = 42;
const aString = "Hello";
const aBoolean = true;

let anUndefined;

log(typeof aNumber); // Output: number
log(typeof aString); // Output: string
log(typeof aBoolean); // Output: boolean
log(typeof anUndefined); // Output: undefined

// Strings
log("------------ Strings ------------");
const message = "Mathematics";

// String Methods
// length - returns the number of characters in a string
log(message.length); // Output: 11

// charAt - returns the character at the specified index
log(message.charAt(2)); // Output: t

// indexOf - returns the index of the first occurrence of a specified value
log(message.indexOf("e")); // Output: 4

// lastIndexOf - returns the index of the last occurrence of a specified value
log(message.lastIndexOf("a")); // Output: 5

// slice - extracts a section of a string and returns it as a new string
log(message.slice(0, 4)); // Output: Math

// toUpperCase() and toLowerCase() - convert string to uppercase/lowercase
log(message.toUpperCase()); // Output: MATHEMATICS
log(message.toLowerCase()); // Output: mathematics

// includes() - checks if a string contains a specified value
log(message.includes("Math")); // Output: true
log(message.includes("science")); // Output: false

// split() - splits a string into an array of substrings
const words = "Learn JavaScript String Methods";
log(words.split(" ")); // Output: ['Learn', 'JavaScript', 'String', 'Methods']

// Numbers
log("------------ Numbers ------------");
const myNumber = 42;
let myFloat = 42.01;
const myString = "42";

log(myNumber === myFloat); // Output: false

myFloat = 42.0;
log(myNumber === myFloat); // Output: true

log(myString + 3); // Output: "423" (String concatenation)
log(Number(myString) + 3); // Output: 45 (String converted to number and added)
log(Number("Michael")); // Output: NaN (Not a number)
log(Number(true)); // Output: 1 (true is converted to 1, false to 0)

// Number Methods
// isInteger - checks if a value is an integer
log(Number.isInteger(myNumber)); // Output: true
log(Number.isInteger(myFloat)); // Output: true

// parseFloat - converts a string to a floating-point number
log(parseFloat("42.56")); // Output: 42.56
log(parseFloat("42")); // Output: 42 (converted to a float)

// parseInt - converts a string to an integer
log(parseInt("42.56")); // Output: 42 (ignores decimal part)

// toFixed - formats a number to a fixed number of decimal places
log(myFloat.toFixed(2)); // Output: "42.00" (two decimal places)
log(Number(42.155).toFixed(2)); // Output: "42.16" (two decimal places)

// toString - converts a number to a string
log(myNumber.toString()); // Output: "42"
log(typeof myNumber.toString()); // Output: "string"

// isNaN - checks if a value is NaN (Not a Number)
log(Number.isNaN(Number("Michael"))); // Output: true
log(Number.isNaN(42)); // Output: false

// Math Methods
log("------------ Math Methods ------------");
// trunc - removes the decimal part of a number
log(Math.trunc(4.9)); // Output: 4
log(Math.trunc(-4.9)); // Output: -4

// ceil - rounds a number up to the nearest integer
log(Math.ceil(4.1)); // Output: 5
log(Math.ceil(-4.1)); // Output: -4

// floor - rounds a number down to the nearest integer
log(Math.floor(4.9)); // Output: 4
log(Math.floor(-4.1)); // Output: -5

// pow - raises a number to the power of another number
log(Math.pow(2, 3)); // Output: 8 (2^3)
log(Math.pow(5, 2)); // Output: 25 (5^2)

// min - returns the smallest value in a list of numbers
log(Math.min(3, 5, 1, 8)); // Output: 1

// max - returns the largest value in a list of numbers
log(Math.max(3, 5, 1, 8)); // Output: 8

// random - generates a random decimal number between 0 (inclusive) and 1 (exclusive)
log(Math.random()); // Output: a random number between 0 and 1

// Example: generating a random integer between 1 and 10
log(Math.floor(Math.random() * 10) + 1); // Output: a random integer from 1 to 10

// Conditional Statements: If/Switch/Ternary
log("------------ Conditional Statements: If/Switch/Ternary ------------");

// 1. If Statement
const age = 20;

if (age < 18) {
  log("You are a minor.");
} else if (age < 65) {
  log("You are an adult.");
} else {
  log("You are a senior.");
}

// 2. Switch Statement
const day = 3;
let dayName;

switch (day) {
  case 1:
    dayName = "Monday";
    break;
  case 2:
    dayName = "Tuesday";
    break;
  case 3:
    dayName = "Wednesday";
    break;
  case 4:
    dayName = "Thursday";
    break;
  case 5:
    dayName = "Friday";
    break;
  case 6:
    dayName = "Saturday";
    break;
  case 7:
    dayName = "Sunday";
    break;
  default:
    dayName = "Invalid day";
}

log(`Today is ${dayName}.`);

// 3. Ternary Operator
const isLoggedIn = true;
const greetings = isLoggedIn ? "Welcome back!" : "Please log in.";
log(greetings);

// Loops
log("------------ Loops ------------");

// 1. For Loop
for (let i = 0; i < 5; i++) {
  log(`Iteration ${i + 1}`);
}

// 2. While Loop
let count = 0;
while (count < 5) {
  log(`Count is ${count}`);
  count++;
}

// 3. Do...While Loop
let num = 0;
do {
  log(`Number is ${num}`);
  num++;
} while (num < 5);

// 4. For...of Loop (for iterating over iterable objects like arrays)
const foods = ["Apple", "Pizza", "Ice Cream"];
for (const food of foods) {
  log(`Food: ${food}`);
}

// 5. For...in Loop (for iterating over object properties)
const human = { name: "John", age: 30, city: "New York" };
for (const key in human) {
  log(`${key}: ${human[key]}`);
}

// Functions
log("------------ Functions ------------");

// 1. Function Declaration
function greet(name) {
  return `Hello, ${name}!`;
}
log(greet("Alice")); // Output: Hello, Alice!

// 2. Function Expression
const add = function (a, b) {
  return a + b;
};
log(add(5, 3)); // Output: 8

// 3. Arrow Function
const multiply = (a, b) => a * b;
log(multiply(4, 7)); // Output: 28

// 4. Function with Default Parameters
function greetUser(name = "Guest") {
  return `Welcome, ${name}!`;
}
log(greetUser()); // Output: Welcome, Guest!
log(greetUser("Bob")); // Output: Welcome, Bob!

// 5. Returning a Function
function outerFunction() {
  return function innerFunction() {
    return "Inner Function!";
  };
}
const inner = outerFunction();
log(inner()); // Output: Inner Function!

// 6. Immediately Invoked Function Expression (IIFE)
(function () {
  log("This is an IIFE!");
})(); // Output: This is an IIFE!

// 7. Function as an Argument
function executeCallback(callback) {
  callback();
}
executeCallback(() => log("Callback executed!")); // Output: Callback executed!

// 1. Function Declaration: A named function that can be called before it is defined (hoisted).
// 2. Function Expression: A function defined as part of a larger expression, such as an assignment to a variable. It is not hoisted.
// 3. Arrow Function: A concise way to write functions using the => syntax. They do not have their own this, which is useful for certain contexts.
// 4. Default Parameters: Allow you to specify default values for function parameters if no value or undefined is passed.
// 5. Returning a Function: A function can return another function, which can then be called later.
// 6. Immediately Invoked Function Expression (IIFE): A function that runs as soon as it is defined. It's useful for creating a new scope.
// 7. Function as an Argument: Functions in JavaScript are first-class citizens, meaning you can pass them as arguments to other functions.

// Arrays
log("------------ Arrays ------------");
// 1. Creating an Array
const fruits = ["Apple", "Banana", "Cherry"];
log(fruits); // Output: [ 'Apple', 'Banana', 'Cherry' ]

// 2. Accessing Elements
log(fruits[1]); // Output: Banana

// 3. Array Length
log(fruits.length); // Output: 3

// 4. Adding Elements
fruits.push("Date"); // Adds to the end
log(fruits); // Output: [ 'Apple', 'Banana', 'Cherry', 'Date' ]

fruits.unshift("Elderberry"); // Adds to the beginning
log(fruits); // Output: [ 'Elderberry', 'Apple', 'Banana', 'Cherry', 'Date' ]

// 5. Removing Elements
fruits.pop(); // Removes from the end
log(fruits); // Output: [ 'Elderberry', 'Apple', 'Banana', 'Cherry' ]

fruits.shift(); // Removes from the beginning
log(fruits); // Output: [ 'Apple', 'Banana', 'Cherry' ]

// 6. Slicing an Array
const citrus = fruits.slice(1, 3); // Slices from index 1 to 3 (exclusive)
log(citrus); // Output: [ 'Banana', 'Cherry' ]

// 7. Iterating Over an Array
fruits.forEach((fruit) => {
  log(fruit);
});
// Output:
// Apple
// Banana
// Cherry

// 8. Mapping an Array
const uppercaseFruits = fruits.map((fruit) => fruit.toUpperCase());
log(uppercaseFruits); // Output: [ 'APPLE', 'BANANA', 'CHERRY' ]

// 9. Filtering an Array
const filteredFruits = fruits.filter((fruit) => fruit.startsWith("B"));
log(filteredFruits); // Output: [ 'Banana' ]

// 10. Finding an Element
const cherryIndex = fruits.indexOf("Cherry");
log(cherryIndex); // Output: 2

// 11. Checking if an Element Exists
const hasApple = fruits.includes("Apple");
log(hasApple); // Output: true

// 12. Sorting an Array
fruits.sort();
log(fruits); // Output: [ 'Apple', 'Banana', 'Cherry' ]

// 13. Reversing an Array
fruits.reverse();
log(fruits); // Output: [ 'Cherry', 'Banana', 'Apple' ]

// Objects
log("------------ Objects ------------");

// Define an object with properties and methods
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 30,
  hobbies: ["reading", "sports", "coding"],
  // Method inside the object
  fullName: function () {
    return this.firstName + " " + this.lastName;
  },
  greet: function () {
    log(`Hello, my name is ${this.fullName()}`);
  },
};

// Accessing properties
log(person.firstName); // Output: John
log(person["age"]); // Output: 30

// Calling a method inside the object
log(person.fullName()); // Output: John Doe
person.greet(); // Output: Hello, my name is John Doe

// Common Object Methods

// Object.keys - returns an array of the object's own property names
log(Object.keys(person));
// Output: ["firstName", "lastName", "age", "hobbies", "fullName", "greet"]

// Object.values - returns an array of the object's own property values
log(Object.values(person));
// Output: ["John", "Doe", 30, ["reading", "sports", "coding"], ƒ, ƒ]

// Object.entries - returns an array of the object's own [key, value] pairs
log(Object.entries(person));
// Output: [["firstName", "John"], ["lastName", "Doe"], ["age", 30], ["hobbies", Array(3)], ["fullName", ƒ], ["greet", ƒ]]

// Adding a new property to the object
person.email = "john.doe@example.com";
log(person.email); // Output: john.doe@example.com

// Deleting a property from the object
delete person.age;
log(person.age); // Output: undefined

// Checking if a property exists
log("hobbies" in person); // Output: true

// JSON
log("------------ JSON ------------");
// JSON is a lightweight data interchange format, commonly used to exchange data between a server and a web application.
// JSON is often represented as a string and resembles JavaScript objects.

// Converting JSON to JavaScript Object
// To work with JSON data in JavaScript, use JSON.parse() to convert a JSON string into a JavaScript object.
const jsonString = '{"name": "Alice", "age": 30, "isMember": true}';
const user = JSON.parse(jsonString);

log(user.name); // Output: Alice
log(user.age); // Output: 30
log(user.isMember); // Output: true

// Converting JavaScript Object to JSON
// To send or store JavaScript data in JSON format, use JSON.stringify() to convert a JavaScript object into a JSON string.
const userObject = {
  name: "Bob",
  age: 25,
  isMember: false,
};

const jsonStringified = JSON.stringify(userObject);
log(jsonStringified); // Output: '{"name":"Bob","age":25,"isMember":false}'

// Promises / Fetch / Async & Await
log("------------ Promises / Fetch / Async & Await ------------");

// A Promise represents a value that may be available now, or in the future, or never. Promises are used to handle asynchronous operations.

// Example of a basic Promise
const myPromise = new Promise((resolve, reject) => {
  let success = true;

  if (success) {
    resolve("Operation successful!");
  } else {
    reject("Operation failed.");
  }
});

// Handling the promise
myPromise
  .then((message) => {
    log(message); // Output: Operation successful!
  })
  .catch((error) => {
    log(error); // In case of failure: Operation failed.
  });

// The fetch API is used to make HTTP requests, and it returns a Promise. It allows you to fetch resources asynchronously.

// Fetch example to get data from an API
fetch("https://jsonplaceholder.typicode.com/posts/1")
  .then((response) => response.json()) // Converts the response to JSON
  .then((data) => {
    log(data); // Output: Post object data from API
  })
  .catch((error) => {
    log("Error fetching data:", error);
  });

// The async/await syntax makes working with Promises easier by allowing you to write asynchronous code that looks like synchronous code. The async keyword declares a function that returns a Promise, and await pauses the execution until the Promise is resolved or rejected.

// Async function example
async function fetchData() {
  try {
    // Await the fetch request
    const response = await fetch(
      "https://jsonplaceholder.typicode.com/posts/1"
    );

    // Await the JSON conversion
    const data = await response.json();

    log(data); // Output: Post object data from API
  } catch (error) {
    log("Error fetching data:", error);
  }
}

// Call the async function
fetchData();
```
