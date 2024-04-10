### What is a Higher Order Component (HOC)

Higher-order components (HOCs) in React can be considered a type of [higher-order function](../JavaScript/Higher%20order%20functions.md). Like traditional [higher-order functions](../JavaScript/Higher%20order%20functions.md) in JavaScript, higher-order components are functions that take a component as input and return a new component as output.

Here's a brief overview of how higher-order components work in React:

1. Accepting a Component as an Argument:
   Higher-order components in React accept a component as an argument and return a new component with additional props or behavior.

```javascript
// Example: Higher-order component accepting a component as an argument
const withLoadingIndicator = (WrappedComponent) => {
  return (props) => {
    if (props.isLoading) {
      return <div>Loading...</div>;
    }
    return <WrappedComponent {...props} />;
  };
};

// Usage:
const MyComponent = ({ data }) => {
  return <div>{data}</div>;
};

const MyComponentWithLoading = withLoadingIndicator(MyComponent);
```

2. Returning a Component:
   Higher-order components return a new component that wraps or enhances the original component with additional functionality or behavior.

```javascript
// Example: Higher-order component returning a new component
const withLogProps = (WrappedComponent) => {
  return (props) => {
    console.log("Props:", props);
    return <WrappedComponent {...props} />;
  };
};

// Usage:
const MyComponentWithLog = withLogProps(MyComponent);
```

Higher-order components are commonly used in React for cross-cutting concerns such as authentication, data fetching, and code reusability. They allow developers to encapsulate and reuse logic across multiple components, making it easier to manage complex behavior and maintain clean and modular code. While they operate on React components rather than plain JavaScript functions, higher-order components exhibit similar characteristics to [higher-order functions](../JavaScript/Higher%20order%20functions.md) in JavaScript.
