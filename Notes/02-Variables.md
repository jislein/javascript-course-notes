## How to declare and initialize variables in JavaScript

We can use three *reserved words* for creating a variable in JavaScript.

The first one is `var`.

```js
var variableName;
```

We can initialize multiple variables as by separating them with commas ( , ) and adding a semicolon ( ; ) at the end.

```js
var category = 'Computers',
	brand = "Popular brand",
	score = 5;
```

The second *reserved word* is `let`. We can apply everything that we use `var` for to `let`.

```js
let variableName;

let category = 'Computers',
	brand = "Popular brand",
	score = 5;
```

The third reserved word is `const`. The rule are almost the same.

### Difference between `let` and `const`

1. `const` can't be reassigned. It is a constant variable.

```JavaScript
//The code bellow will throw an error
const product = "Tablet";
product = "Monitor";
```

![[./images/Pasted_image_20240820201945.png]]

2. Must be initialized at creation.

	```js
	// The code bellow will throw an error.
	const product;
	console.log(product);
```

![[./images/Pasted_image_20240820202732.png]] 