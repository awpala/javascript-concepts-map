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
    * DOM Manipulation
  * Asynchronous Programming
    * Web APIs
    * Built-In Global Objects
  * Exception Handling

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

### DOM Manipulation

TO-DO - `Window`, `Document`, `Node`, `Element`, `HTMLElement`, `HTMLCollection`, `NodeList`, `Event`

## Asynchronous Programming

TO-DO

### Web APIs

TO-DO - `XMLHttpRequest`, `Fetch`

### Built-In Global Objects

TO-DO - `Promise`, `async`/`await`

## Exception Handling

TO-DO - `Error` (and related `...Error` objects)

