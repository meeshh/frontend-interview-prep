### What are Higher order functions?

In JavaScript, a higher-order function is a function that either takes another function as an argument, returns a function, or both. Essentially, it's a function that operates on other functions by either accepting them as arguments or returning them as results.

Here are two common use cases for higher-order functions:

1. Accepting a Function as an Argument:
Higher-order functions can take other functions as arguments, allowing for more flexible and reusable code. This pattern is often used for callbacks and event handling.

```javascript
// Example: Higher-order function accepting a function as an argument
function performOperation(callback, x, y) {
  return callback(x, y);
}

function add(x, y) {
  return x + y;
}

function multiply(x, y) {
  return x * y;
}

console.log(performOperation(add, 2, 3)); // Output: 5
console.log(performOperation(multiply, 2, 3)); // Output: 6
```

2. Returning a Function:
Higher-order functions can also return functions as results. This pattern is often used for function factories or currying.

```javascript
// Example: Higher-order function returning a function
function createMultiplier(factor) {
  return function (x) {
    return x * factor;
  };
}

const double = createMultiplier(2);
console.log(double(3)); // Output: 6

const triple = createMultiplier(3);
console.log(triple(3)); // Output: 9
```

Higher-order functions enable powerful functional programming techniques in JavaScript, such as function composition, partial application, and asynchronous programming with callbacks and promises. They promote code reusability, modularity, and maintainability by allowing functions to be composed and manipulated like any other data type. Understanding and using higher-order functions effectively can lead to more concise, expressive, and flexible code in JavaScript.