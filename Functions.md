# 📘 Functions in JavaScript

Functions in JavaScript are **reusable blocks of code** designed to perform specific tasks.  
They allow you to **organize, reuse, and modularize code**. Functions can take inputs, perform actions, and return outputs.

---

## 🔎 Understanding Functions

- **Parameter** → A placeholder defined in the function.  
- **Argument** → The actual value you pass when calling the function.

### Example
```js
function greet(name) {   // 'name' is a parameter
  console.log("Hello " + name);
}

greet("Alice");  // "Alice" is the argument
```

---

## 🎯 Default Parameters
**Definition**: Default parameters are values automatically assigned to function parameters if no argument is provided.  

```js
function greet(name = "Guest") {
  console.log("Hello, " + name);
}

greet();        // Hello, Guest
greet("Aman");  // Hello, Aman
```

---

## 📤 Return Statement
**Definition**: The `return` statement sends a result back from a function and stops execution at that point.  

```js
function add(a, b) {
  return a + b;
}

let result = add(5, 10);
console.log(result); // 15
```

---

# 🧩 Types of Functions in JavaScript (with Definitions)

### 1. Named Function  
**Definition**: A function declared with a name. Easy to reuse and debug.  
```js
function greet() {
  return "Hello!";
}
console.log(greet()); // Hello!
```

### 2. Anonymous Function  
**Definition**: A function without a name, often used as a callback or assigned to a variable.  
```js
const greet = function() {
  return "Hi there!";
};
console.log(greet()); // Hi there!
```

### 3. Function Expression  
**Definition**: A function (named or anonymous) assigned to a variable.  
```js
const add = function(a, b) {
  return a + b;
};
console.log(add(2, 3)); // 5
```

### 4. Arrow Function (ES6)  
**Definition**: A concise function syntax using `=>`. Does not have its own `this`.  
```js
const square = n => n * n;
console.log(square(4)); // 16
```

### 5. Immediately Invoked Function Expression (IIFE)  
**Definition**: A function that runs immediately after its definition.  
```js
(function () {
    console.log("This runs immediately!");
})();
```

### 6. Callback Function  
**Definition**: A function passed as an argument to another function, executed later.  
```js
function num(n, callback) {
    return callback(n);
}
const double = (n) => n * 2;
console.log(num(5, double)); // 10
```

### 7. Constructor Function  
**Definition**: A function used with `new` to create objects.  
```js
function Person(name, age) {
  this.name = name;
  this.age = age;
}
const user = new Person("Neha", 22);
console.log(user.name); // Neha
```

### 8. Async Function  
**Definition**: A function declared with `async` that returns a Promise.  
```js
async function fetchData() {
  return "Data fetched!";
}
fetchData().then(console.log); // Data fetched!
```

### 9. Generator Function  
**Definition**: A function declared with `*` that can pause and resume using `yield`.  
```js
function* numbers() {
  yield 1;
  yield 2;
  yield 3;
}
const gen = numbers();
console.log(gen.next().value); // 1
```

### 10. Recursive Function  
**Definition**: A function that calls itself until a condition is met.  
```js
function factorial(n) {
  if (n === 0) return 1;
  return n * factorial(n - 1);
}
console.log(factorial(5)); // 120
```

### 11. Higher-Order Function  
**Definition**: A function that takes another function as input or returns one.  
```js
function multiplyBy(factor) {
  return function(num) {
    return num * factor;
  };
}
const double = multiplyBy(2);
console.log(double(5)); // 10
```

### 12. Nested Function  
**Definition**: A function defined inside another function, with access to the parent’s scope.  
```js
function outerFun(a) {
    function innerFun(b) {
        return a + b;
    }
    return innerFun;
}
const addTen = outerFun(10);
console.log(addTen(5)); // 15
```

### 13. Pure Function  
**Definition**: A function that always returns the same output for the same inputs and has no side effects.  
```js
function pureAdd(a, b) {
    return a + b;
}
console.log(pureAdd(2, 3)); // 5
```

### 14. Default Parameter Function  
**Definition**: A function with parameters that have default values.  
```js
function greet(name = "Guest") {
  return "Hello, " + name;
}
console.log(greet());      // Hello, Guest
```

### 15. Rest Parameter Function  
**Definition**: A function that uses `...` to collect multiple arguments into an array.  
```js
function sum(...nums) {
  return nums.reduce((a, b) => a + b, 0);
}
console.log(sum(1, 2, 3, 4)); // 10
```

---
