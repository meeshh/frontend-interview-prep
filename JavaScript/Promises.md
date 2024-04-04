### What are JavaScript Promises?

JavaScript promises are objects used to represent the eventual completion or failure of an asynchronous operation, typically a task that takes some time to complete, such as fetching data from a server, reading a file, or executing a long-running computation.

Promises have three states:

1. **Pending**: Initial state, neither fulfilled nor rejected.
2. **Fulfilled**: The operation completed successfully.
3. **Rejected**: The operation failed.

The basic syntax of a promise looks like this:

```javascript
const myPromise = new Promise((resolve, reject) => {   
// Perform an asynchronous operation   
// If successful, call resolve(value)   
// If an error occurs, call reject(error) 
});
```


Here's a breakdown of how promises work:

- **Creation**: You create a new promise object using the `Promise` constructor, passing a function with two parameters: `resolve` and `reject`. Inside this function, you perform your asynchronous operation. If the operation is successful, you call `resolve()` with the result; if it fails, you call `reject()` with an error.
    
- **Consumption**: Once you have a promise, you can use methods like `then()` and `catch()` to handle the result (either fulfillment or rejection) of the promise.
    
    - `then()`: This method is used to handle the fulfillment of the promise. It takes two optional arguments: a callback function to execute when the promise is fulfilled and a callback function to execute in case of rejection.
        
    - `catch()`: This method is used to handle promise rejections. It takes a single argument: a callback function to execute when the promise is rejected.
        

Here's an example demonstrating the usage of promises:

```javascript
const myPromise = new Promise((resolve, reject) => {
  // Simulate an asynchronous operation (e.g., fetching data from a server)
  setTimeout(() => {
    const randomNumber = Math.random();
    if (randomNumber < 0.5) {
      resolve(randomNumber); // Operation succeeded
    } else {
      reject(new Error('Operation failed')); // Operation failed
    }
  }, 1000);
});

myPromise.then((result) => {
  console.log('Promise fulfilled with result:', result);
}).catch((error) => {
  console.error('Promise rejected with error:', error);
});
```

In this example:

- The promise `myPromise` simulates an asynchronous operation by using `setTimeout()` to resolve or reject the promise after 1 second.
- Inside the `then()` method, we specify a callback function to handle the fulfillment of the promise (i.e., when `resolve()` is called).
- Inside the `catch()` method, we specify a callback function to handle promise rejections (i.e., when `reject()` is called).

Promises provide a cleaner way to handle asynchronous code compared to traditional callback-based approaches, making it easier to write and reason about asynchronous operations in JavaScript. Additionally, promises support chaining, allowing you to compose asynchronous operations sequentially.