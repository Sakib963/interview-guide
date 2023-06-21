[![MasterHead](https://github.com/Sakib963/bistro-boss-server/assets/66853064/51508d0e-6e5d-47bb-892c-433205f28283)](https://github.com/Sakib963)

<h1 align="center">👀 JAVASCRIPT INTERVIEW QUESTIONS AND ANSWERS 👀 </h1>

## 1. What is JavaScript?
JavaScript is a very powerful client-side scripting language.

## 2. What are the different data types present in javascript?
Initially, There are two types of data present in JavaScript.
1. Primitive Types: It represents a single value like number, string, character etc.
2. Non-Primitive Types: It represents a set of values like object & arrays.

## 3. Explain Hoisting in javascript.
Hoisting is the default behavior of moving all declaration to the top. 
```javascript
hoistedVariable=3;
console.log(hoistedVariable) // outputs 3 even when the variable is declared after it is initialized.
var hoistedVariable;
```

## 4. Difference between “ == “ and “ === “ operators.
Both are comparison operator. The difference between the operators is that the “ == “ operator will compare values whereas, the “ === “ operator will compare values and data types.

## 5. Difference between var and let keyword in javascript.
Some differences are:
1. From the beginning the var keyword was used in javascript whereas, the let keyword is added just in 2015.
2. The keyword var has a function scope. Anywhere in the function, the variable declared with var keyword is accessible. Butt in let, the scope of a variable declared with the let keyword is limited to the block in which it is declared.

## 6. What is Implicit Type Coercion in Javascript?
Implicit Type Coercion in javascript is the automatic conversion of value from one data type to another. It takes place when the operands of an expression are different data types.
```javascript
const x = 3;
const y = '3';
const result = x+y; // output: '33'
```

## 7. How many ways we can pass values?
We can pass values in two ways. One is pass by value and other one is pass by reference.
```js
const x = 'data';
const y = x;
```

## 8. What is ES6?
ES6 or the ECMAScript 2015 is the 6th and major edition of ECMAScript language. ES6 comes with significant changes in JS.

## 9. What are the popular features of ES6?
* let and const keywords
* Arrow Functions
* Multi line strings
* Default parameters
* Template Strings
* Destructuring
* Promises
* Classes
* Modules


## 9. What is an Arrow Function?
Arrow function is one of the features in ES6. It allows us to create functions in a cleaner way compared to regular functions.
```js
//function expression
let x = function (a, b) {
    return a * b;
}

// arrow function
let x = (a, b) => a * b;
```

## 10. What is Default Parameter?
Default function parameters allow named parameters to be initialized with default values if no values or undefined is being passed.
```js
const multiply = (a, b = 1) => a * b;

multiply(3, 2) // output: 6
multiply(5) // output: 5
```

## 11. What is Destructuring?
Destructuring is one of the most popular feature in ES6. The destructuring is an expression that makes it easy to extract values from arrays or properties of objects into distinct variables.
```js
// Array Destructuring
const fruits = ['apple', 'banana'];
const [a, b] = fruits;
console.log(a, b) // output: apple banana

// Object Destructuring
const person = {name: "peter", age: 28};
const {name, age} = person;
console.log(name, age) // output: peter 28
```

## 12. What is anonymous function?
An anonymous function is a function without name, typically supplied as an argument.
```js
setTimeout(() => {
    console.log('Execute after 1 second');
}, 1000);
```

## 13. What is Closure in JavaScript?
Closures are an ability of a function to remember the variables and functions that are declared in its outer scope.

## 14. What are callbacks?
A callback is a function that will be executed after another function gets executed. In javascript, functions are treated as first-class citizens, they can be used as an argument of another function, can be returned by another function, and can be used as a property of an object.

## 15. What is DOM?
DOM stands for Document Object Model.  DOM is a programming interface for HTML and XML documents. When the browser tries to render an HTML document, it creates an object based on the HTML document called DOM. Using this DOM, we can manipulate or change various elements inside the HTML document.

## 16. What do you mean by BOM?
Browser Object Model is known as BOM. It allows users to interact with the browser.

## 17. What is the spread operator?
The spread operator is used to spreading an array, and object literals. We can clone an array with some other values by spread operator.
```js
const person = {name: "peter", age: 27};
const anotherPerson = {...person, profession: 'Teacher'};
```

## 18. What is the use of promises in javascript?
Promises are used to handle asynchronous operations or server requests in javascript.

## 19. How does javascript works?
Javascript has no compilation step. Instead, an interpreter in the browser reads over javascript code, interprets each line and runs it.

More modern browsers use a technology known as JIT (Just In Time) compilation. Which compiles javascript to executable bytecode just as it is about to run.

## 20. How many types of Data Structure are there?
There are two types of data structure. 
1. Linear
2. Non Linear

## Explain basic algorithm for binary search tree.
1. If the tree is empty, then target is not in the tree, end search.
2. If the tree is not empty, then the target is in the tree.
3. Check if the target is in the root item.
4. If target is not in the room item then check item is smaller than the root or not.
5. If target is smaller, then search left sub tree, otherwise search right sub tree.
