# Functional programming

**The basic premise is that you can threat functions as a value**

[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function) in JavaScript
is technically a type of object, so you can use it as one

```js
// Function saved into a variable
const greeting = function(name) {
    console.log(`Hello ${name}!`);
}

// Function taken as a parameter and then called
const callFunction = function(fun, arg) {
    fun(arg);

    // Function returned as a value
    return fun;
}

// Function passed as a parameter 
callFunction(greeting, 'Henry');
```

## [Arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)

Used for convenience (added in ES2015)

```js
// Short definition
const f1 = () => {};

// With possible parameters and return value
const f2 = x => {
    return x;
};

// Or multiple ones
const f3 = (x, y) => {
    return x + y;
};

// Also with short definition of a single line return value
const f4 = (x, y) => x + y;
```

_Be careful about behavior of `this`!_
