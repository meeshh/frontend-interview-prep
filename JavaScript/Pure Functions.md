### What are Pure Functions?

These are functions that given the same input they always return the same output. No hidden dependencies or side effects
A pure function never modify any state outside of its scope such as changing global variables, modifying parameters, or performing I/O operations

#### Example

```javascript
function add(a, b) {
  return a + b;
}
```

This `add` function takes two numbers as input and returns their sum. It's deterministic because calling `add(2, 3)` will always return `5`, and it has no side effects because it doesn't modify any external state.

Pure functions have several benefits:

- **Predictability:** Since they always produce the same output for the same input, pure functions are easier to reason about and test.
- **Immutability:** Pure functions encourage immutability, which means that data is not modified in place. Instead, new values are created, making it easier to track changes and reason about the code.
 
> [!TIP]
> A React component is a typical example of a Pure function	

- **Concurrency:** Pure functions are inherently thread-safe and can be safely executed in parallel, which is particularly beneficial in concurrent or distributed systems.
- **Memoization:** Because pure functions always produce the same output for the same input, the results can be cached (memoized) to improve performance.


#### What are non Pure Functions then?

```javascript
let total = 0;

function addToTotal(number) {
	total += number;
}
```

This function modifies the external state (`total`) every time it's called, and its output depends not only on its inputs but also on the current value of `total` Therefore, it's not considered a pure function.