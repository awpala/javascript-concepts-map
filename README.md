# JavaScript Concepts Map

## Overview

TO-DO

## Contents

- Programming Fundamentals
  * Fundamental Semantics
    * Values, Literals, and Data Types
    * Identifiers & Keywords
    * Operators & Precedence
    * Boolean Operators & Truthy vs. Falsy
    * Expressions
  * Program Organization: Statements & Control Structures
    * Conditionals
      * if/else
      * switch/case
    * Repetition
      * for Loops
      * while Loops
      * break and continue
    * Functions
    * Exception Handling
  * Program Organization: Objects & Object-Oriented Programming (OOP)
    * Object & Array Literals
    * Prototypal Inheritance
    * Classes (ES6)
  * ES6+ Features
- Native & Host Objects
  * Built-In Global Objects
    * Fundamental
    * Collections & Utilities
  * Web APIs
    * General Utilities
    * DOM Interaction
  * Asynchronous Programming
    * Web APIs
    * Built-In Global Objects
  * Exception Handling
- Third-Party Libraries: Full-Stack Web Applications
  * Frontend: React
  * Backend: Node.js & Express
  * Utilities
    * Axios
    * Massive
    * bcrypt

# Programming Fundamentals

TO-DO

## Fundamental Semantics

TO-DO

### Values, Literals, and Data Types

TO-DO

| Primitive Data Type | Representative Literal(s) | Description |
| :---: | :---: | :---: |
| Number | `5`, `3.14` , `NaN` | Represents numbers and used in arithmetic operations |
| String | `'Hello World'` | Represents text information |
| Boolean | `true`, `false` | Represents true/false values and used in control structures (discussed later) |
| Null | `null` | Semantically represents the *deliberate absence/omission* of a value |
| Undefined | `undefined` | Semantically represents an *unknown/indeterminate* value |

*(N.B. Symbol and BigInt are primitive data types also provided by JavaScript as of ES2020, however, these will not be considered further here. See [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures) for further discussion of primitive values.)*

### Identifiers & Keywords

TO-DO

| Category | Keywords |
| :---: | :---: |
| Control Structures | `break`, `case`, `continue`, `default`, `do`, `else`, `for`, `if`, `return`, `switch`, `while` |
| Classes & Objects | `delete`, `extends`, `get`, `new`, `set`, `static`, `super`, `this` |
| Declarations | `class`, `const`, `function`, `let`, `var` |
| Miscellaneous Operators | `in`, `instanceof`, `of`, `typeof`, `void` |
| Modules (ES6+) | `as`, `export`, `from`, `import` |
| Exception Handling | `catch`, `finally`, `throw`, `try` |
| Primitive Literals* | `false`, `null`, `true` |
| Miscellaneous Statements | `debugger`, `with` |
| Asynchronous Programming (ES8+) | `async`, `await` |
| Generators (ES6+) | `yield` |

\* N.B. The literals `NaN` and `undefined` are not keywords, as they are not identifiers but rather are properties/values of the global `Object` (see [this discussion](https://stackoverflow.com/questions/7173773/why-nan-and-undefined-are-not-reserved-keywords-in-javascript) for more information).

### Operators & Precedence

TO-DO

| Operation | L → R Associative Operators | L ← R Associative Operators | Result of Operation |
| :---: | :---: | :---: | :---: |
| Miscellaneous | `f(...)` (20), `,` (1) | `++` (18^), `--` (18^), `?:` (4^^^) | (Various) |
| Object Membership | `.` (20), `[...]` (20), `in` (12) | `delete` (17^) | Member access and/or modification |
| Boolean/Logical | `&&` (6), `\|\|` (5) | `!` (17^) | Returns a Boolean value |
| Arithmetic | `*` (15), `/` (15), `%` (15), `+` (14), `-` (14) | `+` (17^), `-` (17^), `**` (16) | Returns a numeric value |
| Comparison | `<` (12), `<=` (12), `>` (12), `>=` (12), `==` (11), `!=` (11), `===` (11), `!==` (11) | | Returns a Boolean value |
| Variable Assignment | | `=` (3), `**=` (3), `*=` (3), `/=` (3), `%=` (3), `+=` (3), `-=` (3) | Assign and/or update variable's stored value |

N.B. In the table above, precedence rank number is indicated in parentheses (where higher number has higher precedence), and furthermore with respect to the operands count, the annotation ^ denotes unary operators, ^^^ denotes the ternary operator, and all others denote/imply binary operators.

!TO-DO: `(...)` has highest precedence and can increase the precedence of its nested value or expression accordingly

### Boolean Operators & Truthy vs. Falsy

TO-DO

| `op1` | `op2` | `!op1` | `op1 && op2` | `op1 \|\| op2` |
| :---: | :---: | :---: | :---: | :---: |
| `true` | `true` | `false` | `true` | `true` |
| `true` | `false` | `false` | `false` | `true` |
| `false` | `true` | `true` | `false` | `true` |
| `false` | `false` | `true` | `false` | `false` |

N.B. In the table above, `op1` and `op2` denote arbitrary operands (which in general can be either values or expressions).

Falsy values:

| Primitive Data Type | Falsy Literals |
| :---: | :---: |
| Number | `0`, `-0`, `NaN` |
| String | `""` (empty string) |
| Boolean | `false` |
| Null | `null` |
| Undefined | `undefined` |

### Expressions

TO-DO

## Program Organization: Statements & Control Structures

TO-DO

| Book Analogy | Software Counterpart |
| :---: |  :---: |
| Book | Application Program |
| Chapters and References | Control Structures |
| Sentences | Statements |
| Phrases and Clauses | Expressions |
| Grammatical/Function Words | Operators |
| Lexical Words | Values |

### Conditionals

TO-DO

#### if/else

TO-DO

#### switch/case

TO-DO

### Repetition

TO-DO

#### for Loops

TO-DO

#### while Loops

TO-DO

#### break and continue

TO-DO

### Functions

TO-DO

### Exception Handling

TO-DO

## Program Organization: Objects & Object-Oriented Programmming (OOP)

TO-DO

### Object & Array Literals

TO-DO

### Prototypal Inheritance

TO-DO

### Classes (ES6)

TO-DO

## ES6+ Features

TO-DO

# Native & Host Objects

TO-DO

## Built-In Global Objects

TO-DO

### Fundamental

TO-DO - `Object`, `Function`

| Fundamental Object | Description | Representative Properties | Representative Methods | MDN Reference |
| :---: | :---: | :---: | :---: | :---: |
| `Object` | The base object from which all object/reference types inherit (via prototypal inheritance), and provides  a key/value storage collection | `obj.constructor`, `obj.__proto__` | `obj.assign()`, `obj.create()`, `obj.entries()`, `obj.is()`, `obj.keys()`, `obj.toString()`, `obj.values()` | [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) |
| `Function` | Routes inputs and outputs, and modularizes code | `fn.length`, `fn.name` | `fn.apply()`, `fn.bind()`, `fn.call()` | [Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function) |

### Collections & Utilities

TO-DO - `Array`, `Math`, `String`, `Set`, `RegExp`

| Collection/Utility Object | Description | Representative Properties | Representative Methods | MDN Reference |
| :---: | :---: | :---: | :---: | :---: |
| `Array` | An indexed ordered-list collection | `arr.length` | `arr.concat()`, `arr.every()`, `arr.filter()`, `arr.find()`, `arr.findIndex()`, `arr.forEach()`, `arr.includes()`, `arr.indexOf()`, `arr.join()`, `arr.keys()`, `arr.map()`, `arr.pop()`, `arr.push()`, `arr.reduce()`, `arr.reduceRight()`, `arr.reverse()`, `arr.shift()`, `arr.slice()`, `arr.some()`, `arr.sort()`, `arr.splice()`, `arr.unshift()` | [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) |
| `Map` | Collection of key-value pairs which remembers original insertion order of the keys | `map.size` | `map.clear()`, `map.delete()`, `map.forEach()`, `map.get()`, `map.has()`, `map.keys()`, `map.set()`, `map.values()` | [Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) |
| `Math` | Mathematical constants and functions | `Math.E`, `Math.LN2`, `Math.LN10`, `Math.LOG2E`, `Math.LOG10E`, `Math.PI`, `Math.SQRT1_2`, `Math.SQRT2` | `Math.abs()`, `Math.ceil()`, `Math.cos()`, `Math.exp()`, `Math.floor()`, `Math.log()`, `Math.max()`, `Math.min()`, `Math.pow()`, `Math.random()`, `Math.round()`, `Math.sin()`, `Math.sqrt()`, `Math.tan()`, `Math.trunc()` | [Math](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math) |
| `Set` | Collection of unique values which are iterable by insertion order | `set.size` | `set.add()`, `set.clear()`, `set.delete()`, `set.entries()`, `set.forEach()`, `set.has()`, `set.keys()`, `set.values()` | [Set](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set) |
| `String` | A wrapper around the primitive string which represents text information that can be modified | `str.length` | `str.charAt()`, `str.concat()`, `str.includes()`, `str.endsWith()`, `str.indexOf()`, `str.lastIndexOf()`, `str.match()`, `str.matchAll()`, `str.padEnd()`, `str.padStart()`, `str.repeat()`, `str.replace()`, `str.replaceAll()`, `str.search()`, `str.slice()`, `str.split()`, `str.startsWith()`, `str.substr()`, `str.substring()`, `str.toLowerCase()`, `str.toUpperCase()`, `str.trim()`, `str.trimStart()`, `str.trimEnd()` | [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `RegExp` | Text processing using regular expressions | `re.flags`, `re.dotAll`, `re.global`, `re.ignoreCase`, `re.multiline`, `re.source`, `re.sticky` | `re.compile()`, `re.exec()`, `re.test()` | [RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp) |

## Web APIs

TO-DO

### General Utilities

TO-DO - `Console`

| Utility Object | Description | Representative Properties | Representative Methods | MDN Reference |
| :---: | :---: | :---: | :---: | :---: |
| `Console` | Display information to the Web console | (*No properties*) | `console.clear()`, `console.debug()`, `console.dir()`, `console.error()`, `console.info()`, `console.log()`, `console.table()`, `console.time()`, `console.timeEnd()`, `console.trace()` | [console](https://developer.mozilla.org/en-US/docs/Web/API/console) | 

### DOM Interaction

TO-DO - `Window`, `Document`, `Element`, `Event`, `EventTarget`, `HTMLCollection`, `HTMLElement`, `Node`, `NodeList`

!TO-DO: `Window` [MDN Window](https://developer.mozilla.org/en-US/docs/Web/API/Window)

| DOM Object | Description | Representative Properties | Representative Methods | MDN Reference |
| :---: | :---: | :---: | :---: | :---: |
| `Document` | Represents the DOM tree of the Web page | `document.body`, `document.documentElement`, `document.head`, `document.links`, `node.childElementCount`, `node.children`, `node.firstElementChild`, `node.lastElementChild`, `document.onselectionchange`, `document.onvisibilitychange` | `document.addEventListener()`, `document.adoptNode()`, `document.createAttribute()`, `document.createElement()`, `document.createEvent()`, `document.getElementsbyClassName()`, `document.getElementsByTagName()`, `document.importNode()`, `document.getElementById()`, `document.querySelector()`, `document.querySelectorAll()` |[Document](https://developer.mozilla.org/en-US/docs/Web/API/document) |
| `Element` | The base class for elements in the `Document` object (e.g., `HTMLElement` and `SVGElement`) | `element.attributes`, `element.classList`, `element.className`, `element.id`, `element.innerHTML`, `element.outerHTML`, `element.tagName`, `element.onfullscreenchange` | `element.addEventListener()`, `element.dispatchEvent()`, `element.getAttribute()`, `element.getAttributeName()`, `element.getElementsByClassName()`, `element.getelementsByTagName()`, `element.hasAttribute()`, `element.hasAttributes()`, `element.hasPointerCapture()`, `element.insertAdjacentElement()`, `element.insertAdjacentHTML()`, `element.matches()`, `element.querySelector()`, `element.querySelectorAll()`, `element.removeAttribute()`, `element.removeEventListener()`, `element.setAttribute()`, `element.toggleAttribute()` | [Element](https://developer.mozilla.org/en-US/docs/Web/API/Element) |
| `Event` | An interaction (e.g., by user) with the DOM | `event.bubbles`, `event.cancelable`, `event.currentTarget`, `event.defaultPrevented`, `event.eventPhase`, `event.target`, `event.type`, `event.isTrusted` | `event.preventDefault()`, `event.stopImmediatePropagation()`, `event.stopPropagation()` | [Event](https://developer.mozilla.org/en-US/docs/Web/API/Event) |
| `EventTarget` | An object which can receive events and listeners (e.g., `Element`, `Document`, and `Window`)  | (*no properties*) | `target.addEventListener()`, `target.removeEventListener()`, `target.dispatchEvent()` | [EventTarget](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget) |
| `HTMLCollection` | An array-like collection of HTML elements in document order | `c.length` | `c.item()`, `c.namedItem()` | [HTMLCollection](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCollection) |
| `HTMLElement` | An object representing any HTML element | `element.contentEditable`, `elementisContentEditable`, `element.dir`, `element.hidden`, `element.innerText`, `element.itemId`, `element.itemRef`, `element.itemValue`, `element.style`, `element.title` | `element.addEventListener()`, `element.blur()`, `element.click()`, `element.focus()` | [HTMLElement](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement) |
| `Node` | A key base class for other DOM API objects representing a generic node in the DOM tree (which can be, for example, an `Element`) | `node.baseURI`, `node.childNodes`, `node.firstChild`, `node.lastChild`, `node.nextSibling`, `node.nodeName`, `node.nodeType`, `node.nodeValue`, `node.parentNode`, `node.parentElement`, `node.previousSibling`, `node.textContent` | `node.appendChild()`, `node.cloneNode()`, `node.contains()`, `node.getRootNode()`, `node.hasChildNodes()`, `node.inserBefore()`, `node.isEqualNode()`, `node.isSameNode()`, `node.removeChild()`, `node.replaceChild()` | [Node](https://developer.mozilla.org/en-US/docs/Web/API/Node) |
| `NodeList` | A collection of nodes | `nodeList.length` | `nodeList.item()`, `nodeList.entries()`, `nodeList.forEach()`, `nodeList.keys()`, `nodeList.values()` | [NodeList](https://developer.mozilla.org/en-US/docs/Web/API/NodeList) |


## Asynchronous Programming

TO-DO

### Web APIs

TO-DO - `XMLHttpRequest`, `Fetch`

| Async HTTP Request Object | Description | Representative Properties | Representative Methods | MDN Reference |
| :---: | :---: | :---: | :---: | :---: |
| `XMLHttpRequest` | Object to interact with Web servers asynchronously, used extensively in AJAX programming  | `xhr.onreadystatechange`, `xhr.readyState`, `xhr.response`, `xhr.responseText`, `xhr.status`, `xhr.statusText`, `xhr.timeout` | `xhr.abort()`, `xhr.getAllResponseHeaders()`, `xhr.getResponseHeader()`, `xhr.open()`, `xhr.send()`, `xhr.setRequestHeader()` | [XMLHttpRequest](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) |

!TO-DO: Fetch API - e.g., 
```js
fetch(request)
 .then(response => { ... return ...; })
 // (optional) chained .then(...)'s
 .catch(error => { ... return ...; };
```

| Fetch API Object | Description | Representative Properties | Representative Methods | MDN Reference |
| :---: | :---: | :---: | :---: | :---: |
| `Body` | Represents the body of the `Request` and `Response` object | `response.body`, `response.bodyUsed` | `response.blob()`, `response.formData()`, `response.json()`, `response.text()` | [Body](https://developer.mozilla.org/en-US/docs/Web/API/Body) |
| `Headers` | Performs various action on HTTP request and response headers | (*no properties*) | `headers.append()`, `headers.delete()`, `headers.entries()`, `headers.forEach()`, `headers.forEach()`, `headers.get()`, `headers.has()`, `headers.keys()`, `headers.set()`, `headers.values()` | [Headers](https://developer.mozilla.org/en-US/docs/Web/API/Headers) |
| `Request` | Represents an HTTP resource request | `request.body`, `request.bodyUsed`, `request.cache`, `request.destination`, `request.headers`, `request.method`, `request.mode`, `request.url` | `request.clone()`, `request.blob()`, `request.formData()`, `request.json()`, `request.text()` | [Request](https://developer.mozilla.org/en-US/docs/Web/API/Request) |
| `Response` | Represents the response to an HTTP request | `response.body`, `response.bodyUsed`, `response.headers`, `response.ok`, `response.status`, `response.statusText`, `response.type`, `response.url` | `response.blob()`, `response.clone()`, `response.error()`, `response.formData()`, `response.json()`, `response.redirect()`, `response.text()` | [Response](https://developer.mozilla.org/en-US/docs/Web/API/Response) |

!TO-DO: global (async) functions `setTimeout`, `clearTimeout`, `setInterval`, `clearInterval`

### Built-In Global Objects

TO-DO - `Promise`, `async`/`await`

| Async Promise Object | Description | Representative Properties | Representative Methods | MDN Reference |
| :---: | :---: | :---: | :---: | :---: |
| `Promise` | An object representing the evantual completion/failure of an asynchronous operation, and its resulting value (i.e., *pending*, *fulfilled*, or *rejected*) | (*no properties*) | `Promise.all()`, `Promise.allSettled()`, `Promise.any()`, `p.catch()`, `p.finally()`, `Promise.race()`, `Promise.reject()`, `Promise.resolve()`, `p.then()` | [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) |

!TO-DO: `async`/`await` functions (ES8+)

## Exception Handling

TO-DO - `Error` (and related `...Error` objects)

# Third-Party Libraries: Full-Stack Web Applications

TO-DO

## Frontend: React

TO-DO

## Backend: Node.js & Express

TO-DO

## Utilities

TO-DO

### Axios

TO-DO

### Massive

TO-DO

### bcrypt

TO-DO
