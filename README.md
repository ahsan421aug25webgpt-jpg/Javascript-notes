# 📘 JavaScript Notes (Basic → Advanced)

A structured JavaScript guide from beginner to advanced concepts — perfect for quick reference or interview prep.

---

## 1. Basics

* **What is JavaScript?**

  * Programming language for the web (runs in browser + Node.js).
  * Adds interactivity, logic, and dynamic behavior.

* **Hello World Example**

  ```js
  console.log("Hello, World!");
  ```

* **Variables**

  ```js
  var x = 10;   // function-scoped
  let y = 20;   // block-scoped
  const z = 30; // constant
  ```

* **Data Types**

  * Primitive → `String`, `Number`, `Boolean`, `null`, `undefined`, `Symbol`, `BigInt`
  * Non-Primitive → `Object`, `Array`, `Function`

---

## 2. Operators

* Arithmetic: `+ - * / % **`
* Comparison: `== === != !== > < >= <=`
* Logical: `&& || !`
* Ternary: `condition ? value1 : value2`

---

## 3. Control Flow

```js
if (age >= 18) {
  console.log("Adult");
} else {
  console.log("Minor");
}

switch(day) {
  case 1: console.log("Mon"); break;
  case 2: console.log("Tue"); break;
  default: console.log("Other");
}
```

* **Loops**

```js
for (let i = 0; i < 5; i++) console.log(i);

let j = 0;
while (j < 5) { console.log(j); j++; }

do { console.log(j); j++; } while (j < 5);
```

---

## 4. Functions

* **Normal Function**

```js
function add(a, b) {
  return a + b;
}
```

* **Arrow Function**

```js
const add = (a, b) => a + b;
```

* **IIFE (Immediately Invoked Function Expression)**

```js
(function() {
  console.log("IIFE runs instantly!");
})();
```

---

## 5. Arrays

```js
let arr = [1, 2, 3, 4];

arr.push(5);       // add
arr.pop();         // remove last
arr.shift();       // remove first
arr.unshift(0);    // add at start

arr.forEach(v => console.log(v));
let doubled = arr.map(v => v * 2);
let evens = arr.filter(v => v % 2 === 0);
let sum = arr.reduce((a,b) => a+b, 0);
```

---

## 6. Objects

```js
let user = {
  name: "Ahsan",
  age: 22,
  greet: function() { console.log("Hello " + this.name); }
};

console.log(user.name);
user.greet();
```

---

## 7. ES6+ Features

* **Template Literals**

```js
let name = "Ali";
console.log(`Hello, ${name}`);
```

* **Destructuring**

```js
let [a,b] = [10,20];
let {name, age} = user;
```

* **Spread & Rest**

```js
let nums = [1,2,3];
let more = [...nums, 4,5];

function sum(...values) {
  return values.reduce((a,b)=>a+b);
}
```

---

## 8. DOM Manipulation

```js
document.getElementById("demo").innerText = "Hello JS";

document.querySelector(".btn").addEventListener("click", () => {
  alert("Button Clicked!");
});
```

---

## 9. Asynchronous JS

* **Callbacks**

```js
setTimeout(() => console.log("After 1s"), 1000);
```

* **Promises**

```js
let promise = new Promise((resolve, reject) => {
  resolve("Success!");
});
promise.then(res => console.log(res));
```

* **Async/Await**

```js
async function fetchData() {
  let res = await fetch("https://api.example.com");
  let data = await res.json();
  console.log(data);
}
```

---

## 10. Advanced Topics

* **Closures**

```js
function outer() {
  let count = 0;
  return function inner() {
    count++;
    return count;
  }
}
let counter = outer();
console.log(counter()); // 1
console.log(counter()); // 2
```

* **Hoisting**

```js
console.log(a); // undefined
var a = 10;
```

* **This keyword**

```js
let obj = {
  name: "Ali",
  show: function() { console.log(this.name); }
};
obj.show();
```

* **Modules**

```js
// math.js
export function add(a,b){ return a+b; }

// main.js
import { add } from './math.js';
```

---

## 11. Interview / Deep Dive Topics

* Event Loop & Call Stack
* Prototypes & Inheritance
* Higher-Order Functions
* Currying & Partial Application
* Debounce & Throttle
* Memory Management & Garbage Collection

---

## ⭐ Resources

* [MDN JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
* [JavaScript.info](https://javascript.info/)

---

