# JavaScript Basic Concepts

# Variables

# 4 Ways to Declare a JavaScript Variable:

- Using `var`
- Using `let`
- Using `const`
- Using nothing

## Operators

# Types of JavaScript Operators

There are different types of JavaScript operators:

- Arithmetic Operators
- Assignment Operators
- Comparison Operators
- String Operators
- Logical Operators
- Bitwise Operators
- Ternary Operators
- Type Operators

# JavaScript Arithmetic Operators

**Arithmetic Operators** are used to perform arithmetic on numbers:

# JavaScript Comparison Operators

| Operator | Description |
| --- | --- |
| == | equal to |
| === | equal value and equal type |
| != | not equal |
| !== | not equal value or not equal type |
| > | greater than |
| < | less than |
| >= | greater than or equal to |
| <= | less than or equal to |
| ? | ternary operator |

# JavaScript Strings

A string (or a text string) is a series of characters like "John Doe".

Strings are written with quotes. You can use single or double quotes:

# JavaScript String Comparison

All the comparison operators above can also be used on string

# JavaScript String Addition

The `+` can also be used to add (concatenate) strings:

# Adding Strings and Numbers

Adding two numbers, will return the sum, but adding a number and a string will return a string:

### Example

let x = 5 + 5;let y = "5" + 5;let z = "Hello" + 5;

# JavaScript Logical Operators

| Operator | Description |
| --- | --- |
| && | logical and |
| || | logical or |
| ! | logical not |
|  |  |

# JavaScript Types are Dynamic

JavaScript has dynamic types. This means that the same variable can be used to hold different data types:

# JavaScript Numbers

All JavaScript numbers are stored as decimal numbers (floating point).

Numbers can be written with, or without decimals:

# JavaScript Booleans

Booleans can only have two values: `true` or `false`.

# **Primitive data types:**

 ****The predefined data types provided by JavaScript language are known as primitive data types. Primitive data types are also known as in-built data types.

**Below is a list of Primitive Data Types with proper descriptions and examples:**

**1. [Number](https://www.geeksforgeeks.org/javascript-numbers/):** Number data type in javascript can be used to hold decimal values as well as values without decimals.

<script>
let x = 250;
let y = 40.5;
console.log("Value of x=" + x);
console.log("Value of y=" + y);
</script>

**[String](https://www.geeksforgeeks.org/javascript-strings/):** The string data type in javascript represents a sequence of characters that are surrounded by single or double quotes

<script>
let str = 'Hello All';
let str1 = "Welcome to my new house";
console.log("Value of str=" + str);
console.log("Value of str1=" + str1);
</script>

**3. [Undefined](https://www.geeksforgeeks.org/javascript-undefined-property/):** The meaning of undefined is ‘value is not assigned’.

<script>
console.log("Value of x=" + x);
</script>

1. 

**[Null](https://www.geeksforgeeks.org/null-in-javascript/):** This data type can hold only one possible value that is null.

- Javascript

`<script>`

`let x = **null**;`

`console.log("Value of x="` `+ x);`

`</script>`

---

**7. [Symbol](https://www.geeksforgeeks.org/javascript-symbol-method/):** This data type is used to create objects which will always be unique. these objects can be created using Symbol constructor.

- Javascript

**`var`** `sym = Symbol("Hello")`

`console.log(**typeof**(sym));`

`console.log(sym);`

---

## **Non-primitive data types**

The data types that are derived from primitive data types of the JavaScript language are known as non-primitive data types. It is also known as derived data types or reference data types.

Below is a list of Non-primitive data types.

Non-primitive Data Types

---

**[Object](https://www.geeksforgeeks.org/objects-in-javascript/)**

---

**[Array](https://www.geeksforgeeks.org/arrays-in-javascript/)**

---

**Below is a list of Non-primitive Data Types with proper descriptions and examples:**

**1. [Object](https://www.geeksforgeeks.org/javascript-objects/): An object** in Javascript is an entity having properties and methods. Everything is an object in javascript.

How to create an object in javascript:

- **Using Constructor Function to define an object:**

```
// Create an empty generic object
var obj = new Object();

// Create a user defined object
var mycar = new Car();
```

- **Using Literal notations to define an object:**

```
// An empty object
var square = {};

// Here a and b are keys and
// 20 and 30 are values
var circle = {a: 20, b: 30};
```

**Example:**

- Javascript

`<script>`

`// Creating object with the name person`

`let person = {`

`firstName: "Luiza",`

`lastName: "Shaikh",`

`};`

`// Print the value of object on console`

`console.log(person.firstName`

`+ "  "` `+ person.lastName);`

`</script>`

---

**2. [Array](https://www.geeksforgeeks.org/arrays-in-javascript/):** With the help of an array, we can store more than one element under a single name.

**Ways to declare a** **single-dimensional array:**

```
// Call it with no arguments
var a = new Array();

// Call it with single numeric argument
var b = new Array(10);

// Explicitly specify two or
// more array elements
var d = new Array(1, 2, 3, "Hello");
```

Array items are separated by commas.

The following code declares (creates) an array called `cars`, containing three items (car names):

### Example

const cars = ["Saab", "Volvo", "BMW"];

# JavaScript Functions

[❮ Previous](https://www.w3schools.com/js/js_datatypes.asp)[Next ❯](https://www.w3schools.com/js/js_objects.asp)

A JavaScript function is a block of code designed to perform a particular task.

A JavaScript function is executed when "something" invokes it (calls it).

let x = myFunction(4, 3);

function myFunction(a, b) {

// Function returns the product of a and b

return a * b;

}

# The () Operator

The () operator invokes (calls) the function:

### Example

Convert Fahrenheit to Celsius:

function toCelsius(fahrenheit) {  return (5/9) * (fahrenheit-32);}let value = toCelsius(77)

# Using a Classes and objects

When you have a class, you can use the class to create objects:

# The Constructor Method

The constructor method is a special method:

- It has to have the exact name "constructor"
- It is executed automatically when a new object is created
- It is used to initialize object properties

If you do not define a constructor method, JavaScript will add an empty constructor method.

class ClassName {

constructor() { ... }

method_1() { ... }

method_2() { ... }

method_3() { ... }

}

class Car {

constructor(name, year) {

this.name = name;

this.year = year;

}

age(x) {

return x - this.year;

}

}

const date = new Date();

let year = date.getFullYear();

const myCar = new Car("Ford", 2014);

document.getElementById("demo").innerHTML=

"My car is " + myCar.age(year) + " years old.";

# JavaScript Objects

You have already learned that JavaScript variables are containers for data values.

This code assigns a **simple value** (Fiat) to a **variable** named car:

let car = "Fiat";

Objects are variables too. But objects can contain many values.

This code assigns **many values** (Fiat, 500, white) to a **variable** named car:

const car = {type:"Fiat", model:"500", color:"white"};

# JavaScript Loops

Loops are handy, if you want to run the same code over and over again, each time with a different value.

Often this is the case when working with arrays:

### Instead of writing:

text += cars[0] + "<br>"; text += cars[1] + "<br>"; text += cars[2] + "<br>"; text += cars[3] + "<br>"; text += cars[4] + "<br>"; text += cars[5] + "<br>";

### You can write:

for (let i = 0; i < cars.length; i++) {   text += cars[i] + "<br>";}

# Different Kinds of Loops

JavaScript supports different kinds of loops:

- `for` - loops through a block of code a number of times
- `for/in` - loops through the properties of an object
- `for/of` - loops through the values of an iterable object
- `while` - loops through a block of code while a specified condition is true
- `do/while` - also loops through a block of code while a specified condition is true

# The For In Loop

The JavaScript `for in` statement loops through the properties of an Object:

### Syntax

for (key in object) {  // *code block to be executed*}

# The For Of Loop

The JavaScript `for of` statement loops through the values of an iterable object.

It lets you loop over iterable data structures such as Arrays, Strings, Maps, NodeLists, and more:

### Syntax

for (variable of iterable) {  // *code block to be executed*}

**variable** - For every iteration the value of the next property is assigned to the variable. *Variable* can be declared with `const`, `let`, or `var`.

**iterable** - An object that has iterable properties.