---
title: Introduction
nav_order: 1
layout: home
parent: Foundation
---

# Introduction

## Definition

React is an open source JavaScript library for building User interfaces, developed by the Facebook software engineer `Jordan Walke`.


## Roadmap
[React Roadmap]

## How does react work ?

React operates by creating an in-memory [virtual DOM] rather than directly manipulating the browser’s DOM.
It performs necessary manipulations within this virtual representation before applying changes to the actual browser DOM.

{: .note}
> ReactJS [Virtual DOM] is an in-memory representation of the actual DOM (Document Object Model). React uses this lightweight JavaScript object to track changes in the application state and efficiently update the actual DOM only where necessary.
> 

### Components

React Components are independent reusable block of code representing part of *User Interface* in DOM.
The primary goal of react component is to Render User Interface and update it whenever its internal state is changed or any event triggered.

### Types of Components

1. Function Components





[Virtual DOM]: https://www.geeksforgeeks.org/reactjs/reactjs-virtual-dom
[React Roadmap]: https://www.tutorialspoint.com/reactjs/reactjs_roadmap.htm