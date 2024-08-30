## Math Object

`Math` is an object in JavaScript that contains several functions and constants to do various complex math operations.

For more detailed information about the object properties and methods you can check [JS Math in W3 Schools website](https://www.w3schools.com/js/js_math.asp).

```js
let result;

// PI
result = Math.PI;

// Round
result = Math.round(2.8); // Rounds upward, prints 3
result = Math.round(2.2); // Rounds downward, prints 2
result = Math.round(2.6); // Rounds upward, prints 3
result = Math.round(2.5); // Rounds upward, prints 3
result = Math.round(2.4); // Rounds downward, prints 2

// Round upwards
result = Math.ceil(2.1); // prints 3

// Round downwards
result = Math.floor(2.9); // prints 2

// Square root
result = Math.sqrt(144); // prints 12

// Absolute
result = Math.abs(-500); // prints 500

// Power
result = Math.pow(2, 4); // prints 16

// Minimum
result = Math.min(3, 5, 1, 12, -3); // prints -3

// Maximum 
result = Math.max(3, 5, 1, 12, -3); //prints 12

// Random, by itself rarely returns an integer above 0.
// If we multiply it by an integer we will get a random decimal from 0 to that number
result = Math.random() * 20;

// Random within a range
result = Math.floor(Math.random() * 30); // This returns numbers between 0 and 30.

console.log(result);
```

## Convert Strings to Number

We can use `Number.parseInt(string)`  to convert a string to an **integer**

```js
const num1 = "20";

console.log(num1);
console.log(Number.parseInt(num1));
```

![[Pasted image 20240828195545.png]]

We can use `typeof` in front of a variable to get its type.

```js
const num1 = "20";

console.log(typeof num1);
console.log(typeof Number.parseInt(num1));
```

![[Pasted image 20240828200807.png]]

We can also use `Number.parseFloat()` to convert string numbers with decimals.

```js
const num2 = "20.2";

console.log(num2);
console.log(Number.parseFloat(num2));
```

![[Pasted image 20240829104857.png]]

If we try to parse a string that is not a number we get a `NaN`. This value means "Not a Number".

```js
const num3 = "One";

console.log(Number.parseInt(num3));
```

![[Pasted image 20240829105452.png]]

We can ask if a number is an integer or not with the `Number.isInteger()` method.

```js
const num2 = 20.2;
const num3 = "One";
const num4 = 20

console.log(Number.isInteger(num3));
console.log(Number.isInteger(num4));
console.log(Number.isInteger(num2));
```

![[Pasted image 20240829105932.png]]

