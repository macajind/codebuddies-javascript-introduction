# Asynchronous programming 

## [Callbacks](https://developer.mozilla.org/en-US/docs/Mozilla/js-ctypes/Using_js-ctypes/Declaring_and_Using_Callbacks)

```js
function successCallback(result) {
    console.log("It succeeded with " + result);
}

function failureCallback(error) {
    console.log("It failed with " + error);
}

// Function callback
doSomething(successCallback, failureCallback);
```

_Callback hell_:
```js
doSomething(function(result) {
    doSomethingElse(result, function(newResult) {
        doThirdThing(newResult, function(finalResult) {
            console.log('Got the final result: ' + finalResult);
        }, failureCallback);
    }, failureCallback);
}, failureCallback);
```

## [Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises)

```js
const wait = ms => new Promise(resolve => setTimeout(resolve, ms));

wait(10000).then(() => saySomething("10 seconds")).catch(failureCallback);
```

```js
doSomething()
    .then(result => doSomethingElse(result))
    .then(newResult => doThirdThing(newResult))
    .then(finalResult => {
      console.log(`Got the final result: ${finalResult}`);
    })
    .catch(failureCallback);
```

## `async` / `await`

[async function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function) is a special kind of function that always returns a `Promise`.

You can than [await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await) for such `Promise`.

```js
async function foo() {
    try {
        let result = await doSomething();
        let newResult = await doSomethingElse(result);
        let finalResult = await doThirdThing(newResult);
        console.log(`Got the final result: ${finalResult}`);
    } catch(error) {
        failureCallback(error);
    }
}

foo().then(() => { /* … */ });
```

## [Events](https://developer.mozilla.org/en-US/docs/Web/Events)

Common thing in web client environment
on which you need to react asynchronously are **DOM Events**
