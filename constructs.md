# Common JS Constructs

## Comments
these are bits of text that are ignored by the compiler in source files. They effectively do nothing but are used to explain complex code or to provide documentation.
```javascript
// I am a comment
"I am not a comment, I am a string literal"
```

## Variables
A varable is a placeholder string for a piece of data.

In JS, varables are loosely-typed - this mean that any datatype can be given to a variable and it can be changed on the fly. I.G. you should avoid doing that.

```javascript
// old way
var someValue = "I am a string";
// you can assign to variables with any datatype
someValue = 42.0;
// es5 way (the modern way you should do it)
// functionally identitcal to the previous except for some complicated scope stuff
let someValue = 42;
// constants added in es5
const someValue = `I am a template string literal`;
// assignment to a constant is invalid (error)
someValue = 42;
```

## Operators
these are things can do a bunch things like add subtract, assign, etc.

```javascript
// assignment changes the value in a variable if it isn't a constant
let thing = 42;
console.log(thing); // 42
thing = 21;
console.log(thing); // 21

// add
2 + 1; // 3
// subtract
2 - 1; // 1
// multiply
3 * 2; // 6
// divide (no integer division)
3 / 2; // 1.5
// exponentiation (es6 or later)
3 ** 3; // 27
```

## Data Types
Javascript takes what I'd call a "fuck it" approach to data types. If you can think of something dumb and weird js will probably just lete you do it no questions asked.

```javascript
// strings
'single quoted string';
"double quoted string";
"double quoted string with quotes: \"\" inside";
// template literals
`this is basically a string but I can put ${variables} inside it`;
// numbers (in js all ints are floats so deal with it)
1 === 1.0; // true
1e10;
1e-10;
// arrays (groups of data that can be of different datatypes because JS)
["fish", "fosh", 1, true, null]
```

## Functions
A function is a group of code that can be invoked in multiple other places. They are a core part of DRY (Don't Repeat Yourself) which is one of the fundamental pillars of programming.

```javascript
function doStuff() {
    console.log("stuff");
}

doStuff(); // prints stuff
doStuff(); // prints stuff again
```

## Objects
Stores data in the form of key-pair values

```javascript
const car = {
    type: "Fiat",
    model: 500,
    color: "white",
};

console.log(car.type); // prints "Fiat"
console.log(car.model); // prints 500
```

## Conditionals
runs one bit of code or another based on something that you define

```javascript
const data = 42;
// comparison operators
data > 41; // true
data < 42; // false
data >= 42; // true
data <= 42; // true
data == 42; // true
data != 42; // false

if (data == 42) {
    // do some stuff
} else if (data > 10) {
    // do something else
} else {
    // do this other thing
}
```

## Loops
Another core pillar of DRY is to avoid repeating code

```javascript
// for loop
for (let i = 0; i < 10; i++) {
    console.log(i);
}

while (i > 10) {
    console.log(i);
}
```