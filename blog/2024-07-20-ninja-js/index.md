---
slug: ninja-js
title: Mastering ninja javascript concepts and models
authors: [rogelio]
tags:  [developing]
---

## Why javascript?

Javascript has become the lingua franca of the browser. As such, learning it can uncover powerful skills to understand new frameworks, tools or systems written for the browser and also to be able to write down one myself one day!

To that end, is of priority to understand how the browser works.

## Web browser models of execution.

The browser is quite ample of a theme => Main principle to begin:

## Client-side web application Life Cycle

Consists of two phases:
1. **Page building**: The DOM (document object model) is built from the markup language html. The elements of the DOM tree are created and rendered in the browser and displayed in the webpage. The css styling and js code is also loaded and if there are js blocks of code, they influence the state of the client-side application and can create or alter or modify or almost anything related to DOM elements. Like creating new nodes, registering event handlers to certain actions like user interactions or server side events. During this phase, the browser execution can shift between rendering the DOM and executing javascript code. This is why JS is a hell of a lot useful for web development!
2. **Event handling**: Once step one is finished, the event handling phase starts. It consists of listening to events stored in an Event Queue dispatched in a FIFO order by their corresponding event listeners registered in the previous phase. This loop keeps going, listening to new events added to the Queue and handling them by event handlers, it only ends when the page is closed or new browser I suspect the suspension mode that some tabs fall in when inactive for a period of time is the same as stopping the execution of the Event Loop. Okay, according to chatgpt:

"Even in an inactive tab, the event loop continues to run, but with limited or deferred activity to conserve resources."

Browsers (such as chrome, safari, mozilla) have **single threaded execution model** this means that only one flow of execution can be active at a time.

Now that we now more about the execution context of js programs, let's move on to know about js and its importance.

## Javascript functional programming paradigm

The functional paradigm of js is key to exploit is most powerful capabilities to develop programs. Js functions are first-class citizens of the langauge, which means that they can be used whenever an object is used. They can be defined as expressions literals or single-statements. This function expressions can be passed as parameters, assigned to bindings, returned from other functions or methods and so on. 

**-------> The key to have in mind is**: *the flexibility of using js functions allow to perform sneaky changes throught the whole codebase, declaring, instantiating, and in sum using encapsulated blocks of code that define verbs (higher level of abstractions actions) whenever we need them; fostering modularization, reusability and maintainability.*


References:
- Secrets Of The Javascript Ninja. John Resig and Bear Bibeault. Manning Publications. December 2012. 


