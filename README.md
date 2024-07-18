Sure! Below is a `README.md` file format that covers all your topics in a question-answer format with "View Example" buttons for easy navigation.

```markdown
# JavaScript Concepts

This document covers various fundamental concepts in JavaScript through a series of questions and answers.

## Table of Contents
1. [Detecting Primitive vs Non-Primitive Data Types](#1-detecting-primitive-vs-non-primitive-data-types)
2. [Different Data Types](#2-different-data-types)
3. [Key Features of JavaScript](#3-key-features-of-javascript)
4. [Difference Between `var`, `let`, and `const`](#4-difference-between-var-let-and-const)
5. [Arrow Functions](#5-arrow-functions)
6. [Hoisting](#6-hoisting)
7. [Strict Mode](#7-strict-mode)
8. [NaN](#8-nan)
9. [Static vs Dynamic Typing](#9-static-vs-dynamic-typing)
10. [Difference Between `null` and `undefined`](#10-difference-between-null-and-undefined)
11. [The `this` Keyword](#11-the-this-keyword)

## 1. Detecting Primitive vs Non-Primitive Data Types
**Q:** How do you detect if a value is primitive or non-primitive in JavaScript?
**A:** By using the `typeof` operator.
```javascript
let obj = { name: "Gautam" };
console.log(typeof obj); // object

let x = null;
console.log(typeof x); // object (even though null is a primitive data type)
```
[View Example](#1-detecting-primitive-vs-non-primitive-data-types)

## 2. Different Data Types
**Primitive:**
- Number
- String
- Boolean
- Null
- Undefined
- Symbol

**Non-Primitive:**
- Object
- Array
- Date
- RegExp

[View Example](#2-different-data-types)

## 3. Key Features of JavaScript
- `let` and `const`
- Default Parameters
- Arrow Functions
- Classes
- Modules
- Multiline Strings
- Template Literals
- Promises
- Async/Await
- Destructuring Objects

[View Example](#3-key-features-of-javascript)

## 4. Difference Between `var`, `let`, and `const`
1. **`var`**:
   - Function scoped
   - Hoisted and initialized with `undefined`
   - Can be accessed before initialization

2. **`let`**:
   - Block scoped
   - Hoisted but not initialized
   - Cannot be redeclared

3. **`const`**:
   - Block scoped
   - Hoisted but not initialized
   - Cannot be reassigned

[View Example](#4-difference-between-var-let-and-const)

## 5. Arrow Functions
**Q:** What are arrow functions in JavaScript?
**A:** A concise way to write functions using `=>` syntax.
```javascript
const add = (a, b) => a + b;
console.log(add(10, 20)); // 30
```
[View Example](#5-arrow-functions)

## 6. Hoisting
**Q:** What is hoisting in JavaScript?
**A:** Hoisting is the process where the interpreter moves the declaration of functions, classes, or variables to the top of their scope before execution.
```javascript
console.log(a); // undefined
var a = 10;
console.log(a); // 10
```
[View Example](#6-hoisting)

## 7. Strict Mode
**Q:** What is strict mode?
**A:** Strict mode is a feature that allows you to write secure JavaScript code by catching silent errors and preventing unsafe actions.
```javascript
"use strict";
var x = 3.14;
function myFunction() {
  "use strict";
  y = 3.14; // Error because y is not declared
}
```
[View Example](#7-strict-mode)

## 8. NaN
**Q:** What is `NaN` in JavaScript?
**A:** `NaN` stands for "Not-a-Number" and is a result of an invalid mathematical operation.
```javascript
let result = "hello" - 1; // NaN
console.log(result); // NaN
```
[View Example](#8-nan)

## 9. Static vs Dynamic Typing
**Q:** Is JavaScript statically or dynamically typed?
**A:** JavaScript is dynamically typed because variable types are checked at runtime and do not need to be declared explicitly.
```javascript
let a = 10; // Number
a = "Gautam"; // String
```
[View Example](#9-static-vs-dynamic-typing)

## 10. Difference Between `null` and `undefined`
**Q:** What is the difference between `null` and `undefined`?
**A:** 
- `null`: Explicitly indicates the absence of an object value.
- `undefined`: Indicates a variable has been declared but not assigned a value.
```javascript
let car = {
  brand: "Toyota",
  model: null,
};
console.log(car.brand); // "Toyota"
console.log(car.model); // null
console.log(car.year); // undefined
```
[View Example](#10-difference-between-null-and-undefined)

## 11. The `this` Keyword
**Q:** Explain the `this` keyword in JavaScript.
**A:** `this` refers to the object that is executing the current piece of code. Its value depends on the context in which it is called.
### Method Invocation
```javascript
let user = {
  name: "Gautam",
  getName: function () {
    return this.name;
  }
};
console.log(user.getName()); // "Gautam"
```
### Constructor Invocation
```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
}

let person1 = new Person("Gautam", 25);
console.log(person1.name); // "Gautam"
console.log(person1.age); // 25
```
[View Example](#11-the-this-keyword)

---

## Examples

### 1. Detecting Primitive vs Non-Primitive Data Types
```javascript
let obj = { name: "Gautam" };
console.log(typeof obj); // object

let x = null;
console.log(typeof x); // object (even though null is a primitive data type)
```

### 2. Different Data Types
```javascript
// Primitive types
let num = 42;
let str = "Hello";
let bool = true;
let n = null;
let u = undefined;
let sym = Symbol("sym");

// Non-primitive types
let obj = { name: "Gautam" };
let arr = [1, 2, 3];
let date = new Date();
let regex = /abc/;
```

### 3. Key Features of JavaScript
```javascript
// let and const
let a = 10;
const b = 20;

// Default parameter
function greet(name = "stranger") {
  console.log(`Hello, ${name}!`);
}

// Arrow function
const add = (a, b) => a + b;

// Classes
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}

// Module (ES6)
export const pi = 3.14;

// Multiline string
const multiLine = `This is a
multiline string`;

// Template literals
const greeting = `Hello, ${name}`;

// Promise
const promise = new Promise((resolve, reject) => {
  resolve("Success!");
});

// Async/await
async function fetchData() {
  let response = await fetch("url");
  let data = await response.json();
}

// Destructuring object
const { name, age } = person;
```

### 4. Difference Between `var`, `let`, and `const`
```javascript
// var
console.log(a); // undefined
var a = 10;
console.log(a); // 10

// let
let b = 20;
{
  let b = 30;
  console.log(b); // 30
}
console.log(b); // 20

// const
const c = 40;
console.log(c); // 40
```

### 5. Arrow Functions
```javascript
const add = (a, b) => a + b;
console.log(add(10, 20)); // 30
```

### 6. Hoisting
```javascript
console.log(a); // undefined
var a = 10;
console.log(a); // 10

console.log(b); // ReferenceError
let b = 20;
```

### 7. Strict Mode
```javascript
"use strict";
var x = 3.14;
function myFunction() {
  "use strict";
  y = 3.14; // Error because y is not declared
}
```

### 8. NaN
```javascript
let result = "hello" - 1; // NaN
console.log(result); // NaN
```

### 9. Static vs Dynamic Typing
```javascript
let a = 10; // Number
a = "Gautam"; // String
```

### 10. Difference Between `null` and `undefined`
```javascript
let car = {
  brand: "Toyota",
  model: null,
};
console.log(car.brand); // "Toyota"
console.log(car.model); // null
console.log(car.year); // undefined
``

`

### 11. The `this` Keyword
```javascript
// Method invocation
let user = {
  name: "Gautam",
  getName: function () {
    return this.name;
  }
};
console.log(user.getName()); // "Gautam"

// Constructor invocation
function Person(name, age) {
  this.name = name;
  this.age = age;
}

let person1 = new Person("Gautam", 25);
console.log(person1.name); // "Gautam"
console.log(person1.age); // 25
```
```

This `README.md` provides a clear and concise overview of key JavaScript concepts along with examples for each. The table of contents and "View Example" buttons help navigate through the document easily.