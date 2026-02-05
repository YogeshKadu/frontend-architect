---
title: Introduction
nav_order: 1
layout: home
parent: Foundation
---

# Introduction

## Definition

React is an open source JavaScript library for building User interfaces, developed by the Facebook software engineer `Jordan Walke`.

React follows component based architecture. where each component represent a single, unique block of JSX code which can be reused in application.

## Roadmap
[React Roadmap]

## How does react work ?

React operates by creating an in-memory [virtual DOM] rather than directly manipulating the browser’s DOM.
It performs necessary manipulations within this virtual representation before applying changes to the actual browser DOM.

{: .note}
> ReactJS [Virtual DOM] is an in-memory representation of the actual DOM (Document Object Model). React uses this lightweight JavaScript object to track changes in the application state and efficiently update the actual DOM only where necessary.
>

## Features of React

* Component-Based Architecture
* Virtual DOM
* JavaScript Syntax Extension(JSX)
* One-way Data Binding
* Unidirectional Data Flow

### Component-Based Architecture: 

React allows developers to break down the UI into independent, reusable components. Each component manages its own state and logic, promoting code reusability, maintainability, and scalability.

### Virtual DOM (VDOM):
React uses a lightweight in-memory representation of the real DOM. When a component's state changes, React first updates the Virtual DOM, then efficiently compares it with the previous version (diffing) and updates only the changed parts in the actual DOM, significantly improving performance.

### JavaScript Syntax Extension(JSX):
JSX is a syntax extension that allows writing HTML-like code within JavaScript. It enhances code readability and makes it easier to visualize the UI structure while integrating logic. Although optional, JSX is widely used in React development

### One-way Data Binding:
One-way data binding means that the data stored in React state is automatically reflected in the UI.
However, when the user interacts with the UI (like typing in an input), the state does not change automatically.
To update the state, we must use event handlers (like onChange) that explicitly modify the state.
So, data flows from state to UI automatically, but UI to state only through events.

### Unidirectional Data Flow:
Unidirectional data flow means that data in React always flows in one direction — from parent components to child components through props.
A child component cannot directly modify the data it receives.
If a child needs to change something, it must call a function provided by the parent, and the parent updates its own state.
This keeps data ownership clear and predictable.

## Components

React Components are independent reusable block of code representing part of *User Interface* in DOM.
The primary goal of react component is to Render User Interface and update it whenever its internal state is changed or any event triggered.

React component must return a single root JSX element so that component can be converted into DOM tree.

### Types of Components

1. Class Component
2. Functional Component

### 1. Class Component

Class components are React components written using ES6 class syntax that provide built-in support for state management, lifecycle methods, and controlled rendering of UI based on data changes.
The class component extends React.Component to inherit React’s core functionality, including access to props, state, lifecycle methods, and the render() mechanism that enables controlled and dynamic UI updates.

### 2. Functional Component

Functional components are React components written as JavaScript functions that define the UI by returning JSX.
Functional components can accept props as input and return JSX that describes what the component should render.




[Virtual DOM]: https://www.geeksforgeeks.org/reactjs/reactjs-virtual-dom
[React Roadmap]: https://www.tutorialspoint.com/reactjs/reactjs_roadmap.htm