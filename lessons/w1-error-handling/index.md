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

## Properties of Error
In JavaScript, error properties can be categorized into two: **Standard error properties and custom properties**.
The standard error properties are:
- name: This is also attached with the reason for an error.
- message: provides additional details for the cause of the error
- stack: traces code history that trigered the error.

Custom error properties include any other properties aside the three mentioned. It is totally dependent on the developer to determine their name.
One popular one is `errorCode`.

![stack-trace-example](https://user-images.githubusercontent.com/51183064/178091213-c085f537-0a43-4748-9938-772246a99b8b.png)
(*image src: https://assets.digitalocean.com/articles/alligator/js/stack-trace/stack-trace-example.png*)

The Error: `ReferenceError: notDefined is not defined` can be interpreted as `Error_Name: Error_Message`. Remember, we've explained standard properties of name and message above.

## Difference between Error and Exceptions
Do you know error is different from exceptions 🤨?<br>
Usually, what we call errors aren't in the real sense, they are exceptions. Exceptions are almost expected and are prepared for.
The opposite is errors, which are almost never envisaged.

```js
try {
 connect(database)
}catch (e) {
 // catches the exception (not error)
}
```

>An exception is an error object that has been thrown.

Examples of error include OutOfMemoryError, StackOverflowError etc. These are unthrownable or uncatered for: almost impossible to cater for them. Even if they can be catered for, it is better to make them crash the code.
