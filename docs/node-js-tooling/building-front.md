---
sidebar_position: 3
---

# Building Frontend

Conceptual blocks of building a web application as of 2024:

+ User interface - how users will consume and interact with your application.
+ Routing - how users will navigate among the parts of your application.
+ Data Fetching - where data lives and how to get it.
+ Rendering - when and where the rendering of static and dynamic content happens.
+ Integrations - what third parties used in the application and how to connect to them
+ Infrastructure - where you deploy, store, and run you application code (serverless,CDN,edge,etc.)
+ Developer Experience - your team's experience building and maintaining your application.

In the React + NextJS stack, React is a library that gives APIs functions and tools to create interactive user interfaces. NextJS is a React **framework** that gives the building blocks to create web applications.

By framework we mean Next.js handles the tooling and configuration needed for React, and provides additional structure, features, and optimizations for your applications.

A user goes to website, then the server sends to the client (the browser) an html file. The rendering happens in the browser when the browsers constructs the DOM with the html file. 

## What is the DOM?
 It is a tree-like representation of the html code. Using DOM methods, you can act on user input and manipulate the DOM in response by selecting, adding, updating and deleting elements in the UI.

I can use js for manipulatin the DOM and is very powerful but verbose. It is an **imperative** way of programming to build UIs. React is a **declarative** library for buidling UIs.

You as developer tell **what** you want, instead of **how**. 

## React and JSX

+ **react** is the core library
+ **react-dom** provides DOM-specific methods that enable to use React with the DOM.

Instead of using verbose code to describe how to manipulate the DOM in js. React allows to describe what you want to manipulate using an extension of Javascript called **JSX** that allows to describe UI manipulations (adding, updating) in traditional HTML syntax.

Nevertheless, browsers don't understand JSX directly, so transforming/compiler tools like **babel** are used to transform the JSX code into regular Javascript.

Apart from the following three rules, JSX is almost like html.

## The three rules of JSX

### 1. Return a single root element
To return multiple elements from a component, wrap them with a single parent tag.

For example, using a div
```html
<div>
  <h1>Hedy Lamarr's Todos</h1>
  <img 
    src="https://i.imgur.com/yXOvdOSs.jpg" 
    alt="Hedy Lamarr" 
    class="photo"
  />
  <ul>
    <li>Invent new traffic lights</li>
    <li>Rehearse a movie scene</li>
    <li>Improve the spectrum technology</li>
  </ul>
</div>
```
### 2. Close all the tags
JSX requires all tags to be closed explicitely: ```<img>``` must become ```<img />``` and wraping tags must be ```<li></li>```

### 3. camelCase ~~all~~ most of the things
