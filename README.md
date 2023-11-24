# A walk in JavaScript

## Preface

A lot of information has been written about JavaScript and EcmaScript since both the language creation time and the standard definition time.
The intention of this road map is to share with you one of many paths you can take to grok the language and specially to draw you to the highest quality information  (which I won't be ever able to write in a better way) in the attempt to prevent you from coming across misleading (when not completely wrong) documents out in the wild.

Hopefully your walk will be much easier than mine!

## Table Of Contents


### [DAY 1](/day_01.md)
- [Introduction to JavaScript](/day_01.md#introduction-to-javascript)
  - What is JS anyway?
  - [What's ECMAScript?](/day_01.md#but-what-is-ecma)
  - [Language features quick overview](/day_01.md#languages-features-quick-overview)
  - [Myths busted](/day_01.md#myths-busted)
- [ES5 vs ES6](/day_01.md#es5-vs-es6)
  - Relevant differences
  - Relevant improvements
  - [Why are we using ES6 in this course?](/day_01.md#why-are-we-using-es6-in-this-course)
  - [After ES6?](/day_01.md#after-es6)
- [Initial workspace Setup](/day_01.md#initial-workspace-setup)
  - Basic Runtime ( Node )
  - IDE ( Visual Studio Code )
  - [Run Code extension](/day_01.md#initial-workspace-setup)
  - Introduction to NPM
***
### [DAY 2](/day_02.md)
  - [Syntax, Grammar & Semantics](/day_02.md#syntax-grammar--semantics)
    - [Statements](/day_02.md#statements)
    - [Expressions](/day_02.md#expressions)
    - [Contextual Rules](/day_02.md#semantics)
  - [ECMAScript Types](/day_02.md#ecmascript-types)
    - [Value type groups](/day_02.md#value-type-groups)
      - Primitives
        - Boolean
        - Null
        - Undefined
        - Number
        - BigInt ( it's still a Stage 3 proposal but Chrome already support it and Firefox and Safari are underway.
        - String
        - Symbol( new in ES6! )
      - [Composite/Compound](/day_02.md#compositecompound)
        - Object
    - [Type conversion](/day_02.md#type-conversion)
      - Explicit ( "type casting" )
      - Implicit ( Coercion )
  - [Operators](/day_02.md#operators)
    - Assignment operators
    - Comparison operators
    - Arithmetic operators
    - Bitwise operators
    - Logical operators
    - String operators
    - Conditional (ternary) operator
    - Comma operator
    - Unary operators
    - Relational operators
    - Destructuring
    - [Operators Precedence](/day_02.md#operators-precedence)
    - [Spread/Rest](/day_02.md#the-case-of-the---spreadrest-operator-)
***
### [DAY 3](/day_03.md)
  - Objects explained
    - Objects, the big picture
    - Syntax
    - Object properties attributes (accessors, descriptors)
    - Prototype
    - Behavior Delegation
    - Exotic Objects
    - Object built-in methods
    - Standard built-in objects
***
### [DAY 4](/day_04.md)
  - Indexed and Keyed Collections
    - Collections family
    - The Array Object
    - Syntax
    - Array Built-in methods
    - Preliminary practice
    - Exercises
***
### [DAY 5](/day_05.md)
  - Control Structures
    - General definition
    - Branching
    - Grouping
    - Exception handling
    - Iteration
    - Arbitrary Jumps
    - The Iterable and the Iterator Protocol
    - Preliminary Practice
    - Exercises
***
### [DAY 6](/day_06.md)
  - Functions
    - General Definition
    - Function declaration (function statement)
    - Function expression
    - Function constructor
    - Constructor vs declaration vs expression
    - Properties of the Function object in the prototype chain
    - Arity & formal parameters
    - Formal parameters and the `arguments` thing
    - Functions as properties of an object
    - IIFE
    - Pure functions
    - Side Effects
  - Execution context
    - Types of Execution Context (executable code)
    - Execution Stack
    - How Execution Context is defined?
    - Articles and books used for this section
  - Scope
    - Part of a program
    - ECMAScript definition
    - General definitions
    - Examples
  - Hoisting
  - Closure
    - General definition
    - Examples
  - Can we Cheat Scope?
    - ev[a|i]l
    - with
  - Relative Concepts Readings
  - Preliminary practice
  - Exercises
***  
### [DAY 7](/day_07.md)
  - `this` Keyword
    - Introduction
    - Resolving `this`
    - Explicitly binding `this` through prototype methods
      - `Function.prototype.bind()`
      - `Function.prototype.apply()`
      - `Function.prototype.call()`
  - Strict mode
    - What happens on strict mode?
    - Semantic Differences
  - Arrow Functions
  - Generators
  - Exercises
***
### [DAY 8](/day_08.md)
  - Classes
    - General definition
    - Syntax
      - `class` declaration statement
      - `class` expression
      - Class body and method definitions
    - ES6 Classes in depth
  - OOP vs Functional
    - General definitions
    - Some essential differences
    - Examples
  - Exercises
***
### [DAY 9](/day_09.md)
  - Asynchronous programming
    - Event Loop
    - Callback
    - Promises
    - Async/Await
    - Exercises
***
### [DAY 10](/day_10.md)
  - JavaScript, where does it live?
    - The ECMAScript Engine
    - What does the engine actually do?
      - Visual guide based on V8
    - How many of them are there?
    - Engines Differences
  - The ECMAScript runtime
    - Runtimes Differences
    - Similarities
  - Javascript and the web
    - HTML
    - CSS
  - TL;DR
  - Complementary readings
***
### [DAY 11](/day_11.md)
  - Quality and reliability
    - An introduction to the "reliability" and "quality" concepts
  - Unit / Integration / Functional testing
    - Definitions
    - Comparison
    - TDD
    - Testing frameworks for JavaScript
  - Debugging
    - Debugging tools available for JavaScript
      - Global console object
      - Node.js console
      - debugger statement
      - node.js debugger
      - Browser's developer tools
      - IDE interaction with a browser to debug
  - Transpilers
    - Babel
  - Task runners, bundlers, build systems
    - Webpack
    - Grunt
    - Gulp
    - Brunch
    - Yeoman
    - RollUp
***
### [DAY 12](/day_12.md)
  - Destructuring
    - Syntax
    - Examples
    - Readings
  - Advanced Function/code factorization
    - Currying
    - Partial application
    - First-class composition
    - Readings
