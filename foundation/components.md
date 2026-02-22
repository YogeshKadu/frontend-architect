---
title: Components
nav_order: 2
layout: home
parent: Foundation
---

# Component

In general a Component or a function is a smallest unit of code designed to perform a singular task. it act as a self-contained module that can be called multiple times.

Function/Component usually takes data as input, process it and returns a result.

# React Components

React Components are independent reusable block of code representing part of *User Interface* in DOM.
The primary goal of react component is to Render User Interface and update it whenever its internal state is changed or any event triggered.

React component works in isolation, it accepts **props** as an input and returns a **JSX code** as output. 
Which then converted into react createElement code.

A react component can only return single JSX element. Its a technical limitation of react as Virtual DOM follows tree like structure.

We can return multiple element by adding them inside a invisible element called `React.Fragment`.

for e.g.

```js
return (
    <>
        <h1>Hello</h1>
        <p>welcome to learning blog!</p>
    </>
)
// OR
return (
    <React.Fragment>
        <h1>Hello</h1>
        <p>welcome to learning blog!</p>
    </React.Fragment>
)
```

---

### Types of Components

1. Class Component
2. Functional Component

### 1. Class Component

Class components are React components written using ES6 class syntax that provide built-in support for state management, lifecycle methods, and controlled rendering of UI based on data changes.

The class component extends **React.Component** to inherit React’s core functionality, including access to props, state, lifecycle methods, and the render() mechanism that enables controlled and dynamic UI updates.
Also known as **stateful component**.

**Example :-**

```js
class class_name extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

### 2. Functional Component

Functional components are React components written as JavaScript functions that define the UI by returning JSX.
Functional components can accept props as input and return JSX that describes what the component should render.
Also known as stateless component.

**Example**

```js
function function_name(props) {
   return  <h1>Hello, {props.name}</h1>;
}
```
