# Object Oriented Programming (OOP)

## [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

An `Object` in JavaScript is implemented as dictionary of keys and values

Almost everything in JS is represented as an `Object` (except primitive types and `undefined`)

```js
const object = { key: value };
```

## [Class](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

For creating objects with same properties and functionality
we usually use classes (added in ES2015)

_In JS classes are just a syntactic sugar to "avoid" prototypes..._

```js
class MyClass extends OtherClass {
    static staticProperty;

    constructor(argument) {
        super();
        this.property = argument;
    }

    method(x) {
        // Body of a method
        return this.property;
    }

    static staticMethod(x) {
        // Body of a static method
        return MyClass.staticProperty;
    }
}
```

### Instance

```js
const instanceOfMyClass = new MyClass(value);
```

## Bonus: [Prototypes](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object_prototypes)

```js
var MyClass = function(argument) {
    OtherClass.call(this);
    this.property = argument;
}

// Extends via. prototype chain
MyClass.prototype = Object.create(OtherClass.prototype);

MyClass.prototype.method = function(x) {
    // Body of a method
    return this.property;
}

MyClass.staticProperty;

MyClass.staticMethod = function(x) {
    // Body of a static method
    return MyClass.staticProperty;
}

var instanceOfMyClass = new MyClass(value);
```
