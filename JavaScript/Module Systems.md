  
JavaScript has evolved various module systems to organize and structure code. Some of the most common module systems include:

1. **CommonJS**: CommonJS is a module system primarily used in server-side environments like Node.js. It uses `require()` to import modules and `module.exports` or `exports` to export values from a module. CommonJS modules are synchronous and loaded at runtime.
    
    Example:
    
```javascript
// Exporting module
const data = [1, 2, 3];
module.exports = data;

// Importing module
const data = require('./data');

```
    
2. **AMD (Asynchronous Module Definition)**: AMD is primarily used for front-end development and supports asynchronous loading of modules. It requires a module loader like RequireJS. AMD uses `define()` to define modules and `require()` to import them.
    
    Example:
    
```javascript
// Define a module
define(['dependency1', 'dependency2'], function(dep1, dep2) {
    return function() {
        // Module code
    };
});

// Import a module
require(['module1', 'module2'], function(mod1, mod2) {
    // Module code
});
    
```
    
3. **ES6 Modules (ECMAScript Modules)**: ES6 introduced native support for modules in JavaScript, which is now widely used in both front-end and back-end development. ES6 modules use `import` and `export` statements to define dependencies and expose functionality. Unlike CommonJS, ES6 modules are statically analyzed and support asynchronous loading in browsers.
    
    Example:
    
```javascript
// Define a module
define(['dependency1', 'dependency2'], function(dep1, dep2) {
    return function() {
        // Module code
    };
});

// Import a module
require(['module1', 'module2'], function(mod1, mod2) {
    // Module code
});

```

Differences:

- **Syntax**: Each module system has its own syntax for defining and importing/exporting modules. For example, CommonJS uses `require()` and `module.exports`, AMD uses `define()` and `require()`, and ES6 modules use `import` and `export`.
    
- **Execution**: CommonJS and AMD modules are executed synchronously at runtime, while ES6 modules are executed asynchronously and can be statically analyzed by tools like bundlers.
    
- **Environment**: CommonJS is primarily used in server-side environments like Node.js, while AMD and ES6 modules are used in both client-side and server-side environments.
    
- **Support for Asynchronous Loading**: AMD is designed for asynchronous loading of modules, making it suitable for browser environments where network latency can be significant. CommonJS and ES6 modules also support asynchronous loading, but it's not their primary focus.
    
- **Static vs. Dynamic**: ES6 modules are statically analyzable, meaning dependencies can be determined at compile-time, whereas CommonJS and AMD modules are dynamically evaluated, making it harder to analyze dependencies at build time.
    

Overall, the choice of module system depends on the specific requirements of your project, the environment you're working in, and your preference for syntax and tooling.