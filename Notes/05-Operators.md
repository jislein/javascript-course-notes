## "Greater than" and "Lower than" Operators

To compare if a value is greater than other we use `>` and to compare if a value is lower than the other we use `<`.

```js
const num1 = 20;
const num2 = "20";
const num3 = 30;

// Greater than...
console.log(num1 > num3); // prints false
console.log(num3 > num1); // prints true

// Lower than...
consle.log(num1 < num3); // prints true
```

![[Pasted image 20240829143552.png]]

## Compare two values

To compare if two values are equal we can use `==`.

```js
const num1 = 20;
const num2 = "20";
const num3 = 30;

console.log(num1 == num3); // prints false
console.log(num1 == num2); // prints true
```

![[Pasted image 20240829171706.png]]

We can see how in the last statement when comparing a number and a string the value returned is `true` that is because JavaScript does not differentiate the `type` and just see that both variables have a 20. That is because `==` is a **non-strict comparator**.

If we would like to compare the values in a strict way we must use `===`.

```js
const num1 = 20;
const num2 = "20";

// Strict comparator
console.log(num1 === num2);
console.log(typeof num1);
console.log(typeof num2);
```

![[Pasted image 20240829173243.png]]

As we could see using the strict comparator `===` also takes into account the `type` of the variable.

Remember that we can use `parseInt()` to convert a string to a number in case the value that we are comparing is a number but it is given to us as a string.

```js
console.log(num1 === parseInt(num2)); // prints true
```

![[Pasted image 20240829174046.png]]

---

To compare if two values are different we use `!=`.