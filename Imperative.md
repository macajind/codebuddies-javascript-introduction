# Four pillars of imperative programming

Starting point for all programmers in many programming languages.

## 0. [Comments](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Comments)

A first useful thing, so you can write notes to your code.

```js
// One line comment

/*
Multiple
line
comment
*/
```

## 1. [Variables](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Declarations)

### Declarations

```js
var x;

let y;

const z = 5;
```

### [Data types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Data_structures_and_types)

#### Basic types

- `String` - `"text"`, `'text'`, ``` `text` ```
- `Number` - `1`
- `BigInt` - `1n`
- `Boolean` - `true`, `false`
- `Symbol` - `Symbol('Sym')`

#### Other types

- `undefined`
- `null`
- `Function`
- `Object` - _Almost everything is an object!_

Empty values: `NaN`, `null`, `undefined`, empty

### [Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)

## 2. [Conditions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else)

```js
if (true/false) {
    // Some code
} else {
    // Some other code
}
```

## 3. [Loops](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration)

```js
while(true/false) {
    // Some code to repeat
}

do {
    // Some code to repeat
} while (true/false);

for (initial_expression;true/false,every_loop) {
    // Some code to repeat
}

// Concrete example:
for (let i = 0; i < 10; ++i) {
    // Some code to repeat 10 times
}
```

## 4. [Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

```js
const array = [1,2,3,4,5];

console.log(array[0]);

array[1] = 'Hello!';
```

## + [Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)

```js
// Function definition
function name(argument) {
    // Body of a function
    return value;
}

// Usage / Call of the previously defined function
name(value);
```

Functions in JS can be particularly tricky
because of dynamic data types and `undefined` values. 

## Bonus: [Output](https://developer.mozilla.org/en-US/docs/Web/API/Console/log)

```js
console.log('Hello World!');
```
