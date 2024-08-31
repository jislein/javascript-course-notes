## Create Strings in JavaScript

We can create strings in 3 ways:

```js
const product = "20 inches Monitor"
const product2 = String('24 inches Monitor')

// The third way is less common but it is good to know it exist.
const product3 = new String('27 inches Monitor')
```

In case we need to use a `"` inside a `" "` or a `'` in a `' '` we use the [escape character](https://www.tutorialstonight.com/javascript-escape-quotes) `\`.

| Code                                         | Result                                  | Description                 |
| -------------------------------------------- | --------------------------------------- | --------------------------- |
| `'I\'m going to be a JavaScript developer.'` | I'm going to be a JavaScript developer. | Escaped single quote (`\'`) |
| `"The book \"World\" is on the table."`      | The book "World" is on the table.       | Escaped double quote (`\"`) |

## Strings: includes and length

To know how long is a string variable we use the `length` property.

```js
const product = "20 inches Monitor";
console.log(product);
console.log(product.length);
```

![[./images/Pasted_image_20240827105005.png]]

If we want to search for a specific string or in this case the *index* where that string starts we use the `indexOf()` method.

```js
const product = "20 inches Monitor";

// The indexOf(string) method return the index of the first character of the string.
// If it doesn't find a coincidence it return -1
console.log(product.indexOf("Monitor")); // prints 10
console.log(product.indexOf("Tablet")); // prints -1
```

![[./images/Pasted_image_20240827111426.png]]

Another method to search in a string is `includes()`.

```js
// The 'includes(string)' method searches for the string and returns true if found and false if it isn't found.
// As you can see in the third statement the method is case sensitive.
console.log(product.includes("Monitor")); // prints true
console.log(product.includes("Tablet")); // prints false
console.log(product.includes("monitor")); // prints false

```

## Concatenate a String and Template Strings

We can concatenate a string using various methods.

We can use the `concat()` function:

```js
const product = "20 inches Monitor ";
const price = "30 USD ";

console.log(product.concat(price));
console.log(product.concat('in Sale.'));
```

![[./images/Pasted_image_20240827124135.png]]

We can use `+` sign:

```js
const product = "20 inches Monitor ";
const price = "30 USD ";

console.log(product + " whit a price of: " + price);
console.log("The product " + product + "has a price of " + price);
```

![[./images/Pasted_image_20240827131219.png]]

Now days the most recommended way to concatenate string is using Template String. For this one we must use backticks (\`) instead of single (') or double (") quotes to create the string. and put the variable inside the string with the fallowing format: `${variable}`. We can also make any kind of operation or even call a function inside the keys ({).

```js
const product = "20 inches Monitor ";
const price = "30 USD ";

console.log(`The product ${product} has the price of ${price}`);
```

![[./images/Pasted_image_20240827132904.png]]

## Cut white spaces from a String

In case we need to delete spaces at the beginning and at the end of a string we use `trimStart()` and `trimEnd()`.

```js
const product = "       20 inches Monitor          ";

console.log(product);
console.log(product.length);

//Remove spaces at the beginning.
console.log(product.trimStart());

//Remove spaces at the end.
console.log(product.trimEnd());
```

![[./images/firefox_l2dZBi1ZY1.gif]]

As you could see when we executed `trimEnd()` the spaces at the beginning stayed there.

To solve that we can chain the methods like this:

```js 
console.log(product.trimStart().trimEnd());
```

That's a recent way for trimming spaces from the beginning and the end of a String. But those are more used for each individual side. 

For trimming both sides the `trim()` method is more commonly used.

## String Methods 

### Replace, Slice and Substring

To change a string or a portion of a string and replace it with another we use the `replace()` method.

Usage: `variable.replace(string_to_replace, new_string)`

```js
const product = "20 inches Monitor";

console.log(product);
console.log(product.replace('inches', '"'));
console.log(product.replace("Monitor", "Curved Monitor"));
```

![[./images/Pasted_image_20240827182248.png]]

Another method is `slice()`. We can use `slice()` to cut from a given index to a given index.

```js
const product = "20 inches Monitor";

console.log(product);
console.log(product.slice(0, 10)); // prints '20 inches '

// If we only pass one parameter it will start from that position to the end of the string.
console.log(product.slice(10)); // prints Monitor

// If the first intex is grater than the second one it wont cut anything and return an empty string
console.log(product.slice(2, 1));
```

![[./images/Pasted_image_20240827195500.png]]

The `substring()` method is an alternative to `slice()`.

>[!important]
>Their main difference is that when `substring()` detects that the first parameter is greater than the second parameter, internally it swaps their position. Different than `slice()` that when it detects that situation it just do nothing and return an empty string.

```js
const product = "20 inches Monitor";

console.log(product.substring(0, 10)); // prints '20 inches '

// Since the starting index is greater than the ending index the function will swap their places and run (1, 2) instead.
console.log(product.substring(2, 1));
```

![[./images/Pasted_image_20240827200849.png]]

If we want to cut at an specific index of the string we can use the `charAt()` method.

```js
const user = 'Perensejo'
console.log(user.charAt(0)); // prints 'P'
```

### Repeat and Split

The `repeat()` method is used to repeat a string multiple times based on the indicated parameter.

```js
const product = "20 inches Monitor";

// .repeat(amount) allows you to reapeat a string multiple times.
const text = ' on SALE'.repeat(3);

console.log(text);
console.log(`${product} ${text} !!!`);
```

![[./images/Pasted_image_20240827205220.png]]

>[!important]
>If you pass a **number with decimals** as a parameter the method will floor it.
>
>```js
>const text = ' on SALE'.repeat(2.4);
>
>console.log(text); // prints 'on SALE on SALE'
>```

The `split()` method allow us to divide a string based on a character we define as the separador and return them in an array.

Usage: `string_variable.split(separator)`

```js
const activity = "I'm learning JavaScript";
console.log(activity.split(" "));

const hhobbies = 'Read, walk, listen to music, write, learn to program';
console.log(hobbies.split(", "));
```

![[./images/Pasted_image_20240827211102.png]]

### Convert to Uppercase or Lowercase

We use the `toUpperCase()` and `toLowerCase()` methods to convert all characters of a string to uppercase or lowercase respectively.

```js
const product = "20 inches Monitor";
console.log(product.toUpperCase());

console.log(product.toLowerCase());
```

![[./images/Pasted_image_20240827234253.png]]

### Convert a Number to String

We can use the `toString()` method to convert a number to a string.

```js
const price = 300;
console.log(price);
console.log(price.toString());
```

![[./images/Pasted_image_20240827234604.png]]

We can differentiate the types on the console knowing that number variables are colored green and strings are colored black.