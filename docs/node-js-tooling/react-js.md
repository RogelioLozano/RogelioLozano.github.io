---
sidebar_position: 3
---

# Building UI with React

React core concepts. There are three core concepts of React that you'll need to be familiar to start building React applications. These are:

+ Components
+ Props
+ State

**Components** are an application of the modularization principle that allows to define less coupled parts of code that when assembled can represent more complex User Interfaces! So then we can update, add, or delete inside components elements and not altering the other parts! (of course this is only loose modularization).

In a more general context than react, Loose modularization is the effort to provide modularization among modules/components but inside the same machine/program. (The modules still could share memory access and the asssembly instruction code is the same for both, so possible register execution errors inside Module A can modify parts of the code in module B even when the source code define those separately! Even on different packages or libraries if they are finally linked to be used in the final production binary!).

Components in React are js functions that return **UI elements**.


https://react.dev/learn/your-first-component

In a React app, every piece of UI is a component and components are regular Js functions except that their names always begin with a capital letter and they return JSX markup.

**Props**

They are used to pass data to components from parent to child.

https://nextjs.org/learn/react-foundations/displaying-data-with-props

**State**
We use state and event handlers to add interactivity with React. React has a set of functions called **hooks** that allow you to add state to components. State is information in the UI that changes over time, usually triggered by user interaction.


