# Error Handling

Error-handling is important in JavaScript, the major reason been that most javascript errors happens at run-time.
The most popular way to handle potential error prone codes is to wrap them in a try-catch block

```js
try {
  //...potential error prone codes
}catch (error) {
  //...do something with caught error
}
```
For example, assuming we are creating a calculator project that has some operation that could raise errors,
we can wrap the operations in a try and catch block.

```js
try {
    var result  =  Sum(10, 20); // assuming Sum is not defined yet
}
catch(ex) {
    document.getElementById("errorMessage").innerHTML = ex;
}
```
