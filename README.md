# IMP-JS-INTERVIEW_QUESTION


# JavaScript Execution Concepts

1. **Global Execution Context**  
   This is the default environment where your JavaScript code runs. When you first run a script, the global execution context is created.

2. **Execution Context**  
   An execution context is created whenever a function is invoked. It contains everything needed to execute that function, like variables, the function itself, and the scope.

3. **Call Stack**  
   This is a stack data structure that keeps track of all the execution contexts. It allows JavaScript to manage function calls, making sure the right code runs in the right order.

4. **Memory Allocation**  
   JavaScript allocates memory to store variables, functions, and objects during code execution. This happens when you declare variables or create objects.

5. **Code Execution**  
   Code execution refers to the process of running JavaScript code. It happens line by line, from top to bottom, unless interrupted by functions, loops, or other control flow mechanisms.

## Trick to Remember:
- **G**lobally **E**veryone **C**an **C**all **M**any **C**ode-lines
  - G = Global Execution Context
  - E = Execution Context
  - C = Call Stack
  - M = Memory Allocation
  - C = Code Execution

---
---
# What is Currying?
Currying is a way of writing a function so that it takes one argument at a time, instead of taking all arguments at once. Each function returns another function that takes the next argument, and so on, until all arguments have been provided.

## Simple Example
Imagine you have a function that adds three numbers together.

## Normal Function:

Here's how you might write a normal function to add three numbers:
```javascript
function add(a, b, c) {
  return a + b + c;
}

console.log(add(1, 2, 3)); // 6
```

### Curried Function:

```javascript
function curriedAdd(a) {
  return function(b) {
    return function(c) {
      return a + b + c;
    };
  };
}

console.log(curriedAdd(1)(2)(3)); // 6

```

### Summary
Currying transforms a function so that it takes arguments one at a time. It makes functions more flexible and reusable by allowing you to fix some arguments and create new functions with fewer arguments.


---
---
---

# Destructuring

Destructuring in JavaScript is a convenient way of extracting values from arrays or properties from objects and assigning them to variables. It allows for cleaner and more concise code.

## Destructuring Arrays

```javascript
// Without destructuring
let arr = [1, 2, 3];
let a = arr[0];
let b = arr[1];
let c = arr[2];

// With destructuring
let [x, y, z] = arr;
console.log(x, y, z); // 1 2 3


Another Example:
let arr = [1, 2, 3, 4];
let [a, , b] = arr;
console.log(a, b); // 1 3

```



---
---
---
