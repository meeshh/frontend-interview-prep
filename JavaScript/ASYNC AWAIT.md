### What is async/await?

`async` and  `await` are extensions of [promises](./Promises.md) in JavaScript, introduced in ECMAScript 2017 (ES8), designed to make asynchronous code easier to write and read. They provide a more synchronous-looking syntax while still leveraging the underlying promise-based asynchronous operations.

Here's a breakdown of `async` and `await`:

- **`async`**: The `async` keyword is used to define a function that returns a promise. It allows you to write asynchronous code in a synchronous manner. When a function is declared with `async`, it automatically wraps its return value in a resolved promise.
    
- **`await`**: The `await` keyword is used inside an `async` function to pause the execution of the function until a promise is resolved. It allows you to wait for the completion of a promise and then retrieve its result. Using `await` makes asynchronous code look and behave more like synchronous code.
    

Here's how you use them together:

```javascript
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data'); // Await the completion of the fetch request
    const data = await response.json(); // Await the parsing of the response body as JSON
    console.log(data);
  } catch (error) {
    console.error('Error fetching data:', error);
  }
}

fetchData(); // Call the async function

```

In this example:

- The `fetchData` function is declared as `async`, which means it automatically returns a promise.
- Inside `fetchData`, `await` is used to pause the execution until the `fetch` operation is completed and the response is received. This ensures that the subsequent code does not execute until the promise returned by `fetch` is resolved.
- Similarly, `await` is used to wait for the parsing of the response body as JSON.
- Any errors that occur during the execution of the `async` function can be caught using a `try...catch` block.

#### Is there any difference between async/await and promises?

> [!NOTE]
> It's important to note that `async` and `await` are built on top of [promises](./Promises.md) and do not introduce new functionality. They provide a more concise and readable syntax for working with [promises](./Promises.md), making asynchronous code easier to write and understand.

### Summary 

In summary, `async` and `await` are syntactic sugar over [promises](./Promises.md), offering a more elegant way to handle asynchronous operations in JavaScript without changing the underlying behavior or functionality.