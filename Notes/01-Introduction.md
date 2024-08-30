## How to add comments to your code

`//` - Is used to make single-line comments.
`/* */` is used to make multi-line comments.
* We must start the comment with `/*` and close it with `*/`.

Examples:
```js
// This is a single-line comment.
let randomVariable;

/*
This is
a multi-line
comment.
*/
```

## Console

Some useful console methods:

```js
console.log(parameter); // When executed, outputs `parameter` value into the console.
console.warn(parameter); // Used for adding a warning format to the output with a yellow colored background in the console.
console.error(parameter); // Used for adding a error format to the output with a reddish colored background in the console.
console.time(nameLabel); // Starts counting time. This can be used to test how much time (in ms) took a block of code to execute. The parameter 'nameLabel' is how we identify the execution of that timer.
console.timeEnd(nameLabel); // This is how we stop tracking the time. To stop it we must provide tha same 'nameLabel' we used to start it.
```

Example:
```js
console.log("Normal log message");
console.warn("Warning message");
console.error("Error message");  

console.time("Label");  

console.log("Message");
console.log("Message");
console.log("Message");
console.log("Message");
console.log("Message");
console.log("Message");
console.log("Message");
console.log("Message");
console.log("Message");  

console.timeEnd("Label");
```

![[Pasted image 20240820184607.png]]

