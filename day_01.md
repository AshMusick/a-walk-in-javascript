# [A walk in JavaScript](/README.md)

## DAY 1

- [A walk in JavaScript](#a-walk-in-javascript)
  - [DAY 1](#day-1)
  - [Introduction to JavaScript](#introduction-to-javascript)
    - [But what is ECMA?](#but-what-is-ecma)
    - [Languages features quick overview](#languages-features-quick-overview)
    - [Myths busted](#myths-busted)
  - [ES5 vs ES6](#es5-vs-es6)
    - [Why are we using ES6 in this course?](#why-are-we-using-es6-in-this-course)
    - [After ES6?](#after-es6)
  - [Initial workspace setup](#initial-workspace-setup)

## Introduction to JavaScript

A great overview regarding ECMAScript and JavaScript.
[Article by Michael Aranda](https://www.freecodecamp.org/news/whats-the-difference-between-javascript-and-ecmascript-cba48c73a2b5/)

> JavaScript began as - and primarily still is - a language for scripting inside web browsers; however, the standardization of the language as ECMAScript has made it popular as a general-purpose language. In particular, the Mozilla implementation SpiderMonkey is embedded in several environments such as the Yahoo! Widget Engine. Other applications embedding ECMAScript implementations include the Adobe products Adobe Flash (ActionScript) and Adobe Acrobat (for scripting PDF files). [Scripting Language - Wikipedia](https://en.wikipedia.org/wiki/Scripting_language)

### But what is ECMA?

Let's start with some facts

- In 1995 [Brendan Eich](https://en.wikipedia.org/wiki/Brendan_Eich) was recruited by [Netscape](https://en.wikipedia.org/wiki/Netscape_Navigator) to embed [Scheme](https://en.wikipedia.org/wiki/Scheme_(programming_language)) programming language into netscape Navigator. Due to different company level decisions the original idea mutated, and it ends up with Brendan writing a new language prototype written in 10 days,
- In 1996 Netscape submitted JavaScript to [ECMA Internacional](https://www.ecma-international.org/memento/index.html), an industry association dedicated to standardization of Information and Communication Technology (ICT) and Consumer Electronics (CE), the task of defining a Standard specification so that other vendors could implement the language as well.
- In 1997 the first release of the ECMA-262 standard was published and JavaScript gradually became the most popular implementation. Other ECMAScript languages derived from that standard too, e.g [ActionScript](https://en.wikipedia.org/wiki/ActionScript) and [JSscript](https://en.wikipedia.org/wiki/JScript).

> Source [Standardization](https://en.wikipedia.org/wiki/JavaScript#Standardization) on wikipedia

### Languages features quick overview

- [Dynamic typed](https://en.wikipedia.org/wiki/Dynamic_typing)
- Functions as [first-class citizens](https://en.wikipedia.org/wiki/First-class_citizen)

- **Multi-paradigm language**
  - [Structured](https://en.wikipedia.org/wiki/Structured_programming)
    - [Imperative](https://en.wikipedia.org/wiki/Imperative_programming) in which the programmer instructs the machine how to change its state,
      - [Procedural](https://en.wikipedia.org/wiki/Procedural_programming) which groups instructions into procedures,
      - [Object-oriented](https://en.wikipedia.org/wiki/Object-oriented_programming) which groups instructions together with the part of the state they operate on,
      - [Prototype-based](https://en.wikipedia.org/wiki/Prototype-based_programming)
    - [Declarative](https://en.wikipedia.org/wiki/Declarative_programming) in which the programmer merely declares properties of the desired result, but not how to compute it ( e.g regex )
      - [Functional](https://en.wikipedia.org/wiki/Functional_programming) in which the desired result is declared as the value of a series of function applications,

  - [Event-driven](https://en.wikipedia.org/wiki/Event-driven_programming)
- [Client-side](https://en.wikipedia.org/wiki/Client-side)
  - Web Browsers
- [Server-side](https://en.wikipedia.org/wiki/Server-side)
  - Node.js

[See more](https://en.wikipedia.org/wiki/JavaScript#Features)

### Myths busted

> **[MYTH]** JavaScript === Client-Side

Well that's easy to prove ... lets say ... starting with Node.js

> **[MYTH]** JavaScript === Front-End

Humm, see above? and ... what's FE anyway? is it the visual aspect? the user interaction handling? the data process occurring when an API is consumed to store a denormalized version of the schema in a local database?

> **[MYTH]** JavaScript === "interpreted" language.

JavaScript is not an "interpreted" language anymore!!! or at least is not ONLY interpreted. Since V8 introduced [JIT compilation](https://en.wikipedia.org/wiki/Just-in-time_compilation) in 2008, all modern browsers started overhauling their engines to be able to compete.
Several improvements were based on pre-compiling optimizations, including (but not only) the generation of an intermediate Bytecode and a post optimization to produce machine code. Also several optimization initiatives were disregarded along the way like V8's Full-codegen and [Crankshaft](https://blog.chromium.org/2010/12/new-crankshaft-for-v8.html).

Here some interesting articles

- [V8 Background compilation](https://v8.dev/blog/background-compilation)
- [V8 Ignition + TurboFan](https://v8.dev/blog/launching-ignition-and-turbofan)
- [Understanding V8's ByteCode](https://medium.com/dailyjs/understanding-v8s-bytecode-317d46c94775)
- [SpiderMonkey ByteCodes](https://developer.mozilla.org.cach3.com/en-US/docs/Mozilla/Projects/SpiderMonkey/Internals/Bytecode#Bytecode_Listing) (the original url is no longer available so I replaced it with a cache version)
- [The Baseline Interpreter: a faster JS interpreter in Firefox 70](https://hacks.mozilla.org/2019/08/the-baseline-interpreter-a-faster-js-interpreter-in-firefox-70/)

## ES5 vs ES6

To be fair we should go back to the evolution of ES.

> The JavaScript standard is referred to officially as "ECMAScript" (abbreviated "ES"), and up until just recently has been versioned entirely by ordinal number (i.e., "5" for "5th edition").
>
> The earliest versions, ES1 and ES2, were not widely known or implemented. ES3 was the first widespread baseline for JavaScript, and constitutes the JavaScript standard for browsers like IE6-8 and older Android 2.x mobile browsers. For political reasons beyond what we'll cover here, the ill-fated ES4 never came about.
>
> In 2009, ES5 was officially finalized (later ES5.1 in 2011), and settled as the widespread standard for JS for the modern revolution and explosion of browsers, such as Firefox, Chrome, Opera, Safari, and many others.
>
> Leading up to the expected next version of JS (slipped from 2013 to 2014 and then 2015), the obvious and common label in discourse has been ES6.
>
> Extract from [YDKJS - ES6 & Beyond](https://github.com/getify/You-Dont-Know-JS/blob/1st-ed/es6%20%26%20beyond/ch1.md#versioning) by Kyle Simpson

What is important to understand is that **until ES6** all versions were **ordinal versioned** and the release pace was **freaking slow** mostly because the browsers weren't decoupled from the OS and therefore any change should be integrated at OS releasing scale.

Since ES6 - AKA ES2015, a year-based schema was introduced to reflect and support the fast development pace of JavaScript particularly impulsed by the decoupling of the Web Browsers from OS first but also due to the expansive adoption of the language and the growth of its use beyond "just swapping a button img on rollover" (A very interesting article about that was written by **Matthew MacDonald**, [read it here](https://medium.com/young-coder/how-javascript-grew-up-and-became-a-real-language-17a0b948b77f)).

From ES2015 the standardization process started behaving as a **living standard** hence not tied to structured cuts but by an release based on continuous consensus and progressive adoption.
In order to keep the pace, several improvements were required under the hood to keep it stable and scalable. Browsers will then adopt the new features based at their own pace, which left on the engineering side the responsibility for maintaining the backward compatibility, what led to an extensive growth of techniques such as [polyfilling](https://github.com/getify/You-Dont-Know-JS/blob/1st-ed/es6%20%26%20beyond/ch1.md#shimspolyfills) and [transpiling](https://github.com/getify/You-Dont-Know-JS/blob/1st-ed/es6%20%26%20beyond/ch1.md#transpiling)

Tons of publications can be found online comparing both standards; you can read them online. I'd suggest to start with clean unbiased documents such as the [ecma-262 5.1](https://262.ecma-international.org/5.1/index.html) and [ecma-262 6.0](https://262.ecma-international.org/6.0/) ... but some find that too tedious :D ... you can check also this [ECMAScript 6 — New Features: Overview & Comparison](http://es6-features.org/) by Ralf S. Engelschall which I find very interesting, or jump into the excellent [You Don't Know JS book series](https://github.com/getify/You-Dont-Know-JS/) by Kyle Simpson, especially on the dedicated book [ES6 & Beyond](https://github.com/getify/You-Dont-Know-JS/blob/1st-ed/es6%20%26%20beyond/) by Kyle Simpson

My summary is:

- Several improvements made under the hood to support scalability
- Several "syntactic sugar" added to improve the coding experience, some of the to avoid repetitive patterns and reducing human error vectors, some other to emulate coding styles from other languages, some of them really misleading ( like the use of "class" emulation when there's no "class" at all in JS World)
- Several ( and continuously increasing ) new features to support the wide spread of the language usage.
- Several new restrictions adopted as default when previously they were optional ( e.g. strict mode )

### Why are we using ES6 in this course?

Essentially because even though you will still work with legacy pre-ES6 code, hopefully you will grow as engineers on a post-ES6 world. Secondly because it's easier to understand and work with JavaScript as a general purpose language using ES6 rather than ES5 and most of the examples you'll find online will be presented that way.

### After ES6?

Well, by the time being we're on the [ES2019 version](https://262.ecma-international.org/10.0/) ... though funny they still use a their URI with the ordinal version ( see the link ) instead of the year-based ... ¯\\_(ツ)_/¯ ... and the features included are following a 4-stages revision flow described on the [Technical Committee 39 (aka TC39) web site](https://tc39.es/process-document/)

## Initial workspace setup

1. [Install Node.js](https://nodejs.org/en/)
   1. Alternatively you can Install Volta (https://volta.sh/) which is a great Node.js version manager
2. [Install VS Code](https://code.visualstudio.com/)
3. Add the following extensions to VS Code
   1. [CodeRunner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)
   2. [EsLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
4. [Introduction to NPM](https://docs.npmjs.com/about-npm/)

***
[Go next to DAY 2](/day_02.md)
***
[Back to main page](https://github.com/thinkb4/a-walk-in-javascript/tree/master#day-1)
