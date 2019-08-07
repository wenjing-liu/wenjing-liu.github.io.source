---
title: "JavaScript—2018 知识框架"
catalog: true
toc_nav_num: true
date: 2018-05-12
subtitle: "Keep with new"
header-img: "/img/article_header/article_header.png"
tags:
- JavaScript
catagories:
- JavaScript

---
> 写在前面的话： 发现自己的记忆力不好，希望通过总结JavaScript的知识，强化记忆。最近趁着项目不忙，系统的学习了一下，让自己有个全面的知识体系，以及跟进JavaScript的发展步伐。(内容是中英文混杂，有时间后续会重写，有错误不全的地方请指正)


### 一、基础JavaScript
* Variable and Datatypes & variable mutation and type coercion
* Operators
* if/ else statements
* Boolean logic and Switch statements
* Functions
* Statements and Expressions
* Arrays
* Objects and Properties
* Object and Methods
* Loop and Iteration
* ES5, ES6/ ES2015 and ES2016
***
### 二、JavaScript运行原理
* how code executed: JavaScript Parsers and Engines
* Execution Contexts and Execution Stack
* Execution Contexts in Detail: Creation and Execution Phases and Hoisting, hositing in practice
* Scoping and the Scope Chain
* 'this' keyword and 'this' in practice

***
### 三、浏览器中的JavaScript: DOM操作和事件
* The DOM and DOM Manipulation
* Math.random, Math.floor
  * document.querySelector().textContent =
  * document.querySelector().innerHTML =
  * document.querySelector().style.display =
  * document.querySelector().addEventListener(eventName,  function () {})
  * document.querySelector().src
  * document.getElementById()
  * document.querySelector().classList.remove(className)
  * document.querySelector().classList.add(className)
  * document.querySelector().classList.toggle(className), if has class, delete, if not , add class
* HTML and CSS crash course
* Event and Event Handling: Rolling the Dice
  * 事件只能在执行栈为空的时候来处理
***
### 四、高级JavaScript：Object和Function
* Everything is an Object: Inheritance and the Prototype Chain
  * primitives(number, string, boolean, undefined, null) and Objects
  * constructors and instances
  * inheritance
  * prototypes and prototype chains
  * every JavaScript object has a prototype property, which makes inheritance possible in JavaScript
  * The prototype property of an object is where we put methods and properties that we want other objects to inherit
  * The constructor's prototype property is NOT the prototype of the Cosntructor itself, it's the prototype of ALL instances that are created through it
  * When a certain method (or property) is called, the search starts in the Object itself, and if it cannot be found, the search moves on to the objects's prototype. This continues until the mehtod is found: prototype chain.
* Creating Objects: Function Constructors
* The prototype Chain in the console
  * \__proto__  and prototype
  * objectName.hasOwnProperty(propertyName)
  * objectName instanceof Constructor
  * console.info(objectName)
 * Creating Objects: Object.create
  * Object.create(objectPrototype)
  * Object.create(objectPrototype, obj), obj = { arr1: {value: 'attr'}, attr2: { vlaue: 'attr2'} }
* Primitives vs Objects
 * primitives contain the values
 * objects point to the values
* First Class Function: Passing Functions as Arguments
 * A function is an instance of the Object type
 * A function behaves like any other object
 * We can store function in a variable
 * We can pass a function as an argument to another function
 * We can return a function from a function
 * Above all we see in js, first-class functions
* First Class Function: Functions Returning Functions
* Immediately Invkoed Function Expression(IIFE)
 * 隔离作用域
 * 写惰性载入（惰性函数) : 例如浏览器的环境监测只需要执行一次，可以用这个
* Closures
 * An inner function has always access to the variables and parameters of its outer function, even after the outer function has returned
* Bind, Call and Apply
 * call(thisObj, otherArguments1, arguments2)
* apply(thisObj, otherArgumentsArray)
* bind(thisObj， arguments1), 不是立即调用，而是返回函数，参数可以分开设置，调用的时候在设第二个，函数curring
***
### 五、下一代JavaScript：ES6/ES2015
* Variable Declarations with let and const
 * var , function scope
 * let, const , block scope, temporal dead zone
   * accessing a let or constbefore it is declared throws ReferenceError
* Blocks and IIFEs
* String in ES6/ ES2015
  * template literals (backtick (``) )
  * string method
    * str.startsWith('test')
    * str.endsWith('test')
    * str.includes('test')
    * str.repeat(5)
* Arrow Functions: Basics, Lexical 'this' keyword
  * method call 'this' point to the object, function call 'this' point to the global object 'window'
  * arrow function. sharing 'this' keywords with its surrounding
* Destructuring
  * [firstName, age] = ['claire', 20]
  * {firstName, age } = { firstName: 'claire', age: 20}
  * {firstName: a, age: b} = { firstName: 'claire', age: 20}
* Arrays in ES6/ ES2015
  * Array.from()
  * el.className
  * for ( el of arr)可以使用continue 和break
  * forEach，map， continue，break不生效
  * arr.findIndex(cur => cur > 18)
  * arr.find(cur => cur > 18)
* The spread operator
  * ...[1, 3, 4]
* Rest parameters
* Default parameters
* Maps
  * new Map()
  * map.set(key, value)
  * map.get(key)
  * map.size
  * map.delete(key)
  * map.has(key)
  * map.clear()
  * map.forEach
  * for( let key of map)
  * map.entries()
* Classes
  * static method in class
  * class is no hosited, must first declared, then use
  * only add method to class, not properties
* Classes with Subclasses
  * inheritance

***
### 六、异步JavaScript：Promise, Async/Await和Ajax
* UnderStanding Asynchronous JavaScript: The Event Loop
  * Event Loop
* The Old Way: Asynchronous JavaScript with Callbacks
* From Callback hell to Promises
 * Promise
   * Object that keeps track about whether a certain event has happened already or not
   * Determines what happens after the event has happened.
   * Implements the concept of a furture value that we're expecting
   * Promise state: pending-> settled/resolved--> fulfilled(rejected)
* From Promises to Async/Await
  * Async/Await is used to consume Promise
  * Async function 总是返回Promise
  * Promise vs Generator Function vs Async Await
* Ajax and APIs
  * Ajax: Asynchronous javascript and xml
    * api: application programming interface own API, for data coming from you own server
    * 3rd-party APIs:
      * Google Maps
      * Embed Youtube videos
      * Weather data
      * Movies data
      * Send email or SMS
.....
   * 好用的跨域工具：https://crossorigin.me/: for cors when practice
* Making Ajax Calls with Fetch and Promises, and Fetch and Async/Await
   * fetch vs 传统Ajax(XMLHttpRequest)
     * Fetch 优点主要有：
       * 语法简洁，更加语义化
       * 基于标准 Promise 实现，支持 async/await
       * 同构方便，使用 isomorphic-fetch
     * Fetch 常见坑
       * Fetch 请求默认是不带 cookie 的，需要设置 fetch(url, {credentials: 'include'})
     * 服务器返回 400，500 错误码时并不会  reject，只有网络错误这些导致请求不能完成时，fetch 才会被 reject。
***
### 七、现代JavaScript: 使用ES6, NPM, Babel and Webpack
* A modern Setup: configuring webpack
* A modern Setup: the webpack Dev Server
* A modern Setup: Babel
* Planning Project with MVC
* How ES6 Modules work
* Implementing Persistent Data with localStorage
