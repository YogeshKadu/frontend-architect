---
title: Components
nav_order: 2
layout: default
parent: React Foundation
---

# Components
{: .no_toc}

## Definition
{: .no_toc}
In general a Component or a function is a smallest unit of code designed to perform a singular task. it act as a self-contained module that can be called multiple times.

Function/Component usually takes data as input, process it and returns a result.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

# React Components

React Components are independent reusable block of code representing part of _User Interface_ in DOM.
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
);
// OR
return (
  <React.Fragment>
    <h1>Hello</h1>
    <p>welcome to learning blog!</p>
  </React.Fragment>
);
```

---

### Types of Components

1. [Class Component](#1-class-component)
2. [Functional Component](#2-functional-component)

### 1. Class Component

Class components are React components written using ES6 class syntax that provide built-in support for state management, lifecycle methods, and controlled rendering of UI based on data changes.

The class component extends **React.Component** to inherit React’s core functionality, including access to props, state, lifecycle methods, and the render() mechanism that enables controlled and dynamic UI updates.
It is also known as **stateful component**.

**Example :-**

```js
class class_name extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
class Class_Name extends React.Component {
  constructor(props) {
    super(props);
    console.log(this.props);
    /**
     * Never use setState in constructor
     * instead initialize the states directly.
     * */
    this.state = {};
  }
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

**Class Functions**{: .fs-5}

#### **Constructor**{: .fs-3}

Constructor is function which get invoked when a new class object is created. the purpose of the constructor is to initialize the component which includes initial prop validation, state initialization.

It is same as a js function, which can only be invoked indirectly by code.

Theres a difference between default and parameterized constructor. the props are passed as a parameter to constructor. 

{: .warning}
> If we are initializing Component in constructor we must also initialize Base Constructor with **super()** and it should be the first statement of constructor block.

**Example :-**

```js
class class_name extends React.Component {
  constructor(props) {
    super(props);
    console.log(this.props);
    /**
     * without `super(props)` this.props will hold undefined value as this is not initialized for constructor block.
     * */
    const valid = isNumber(this.props.age);
    this.state = {
        validAge: valid
    }
  }
  render() {
    if(this.state.validAge)
        return <h1>Hello, {this.props.name} - {this.props.age}</h1>;
    else
        return <h1>Not a Valid {this.props.age} is not a number</h1>;
  }
}
```

{: .highlight}
> Get to know about react lifecycle and functions in [CH-2](#) page.

### 2. Functional Component

Functional components are React components written as JavaScript functions that define the UI by returning JSX.
Functional components can accept props as input and return JSX that describes what the component should render.
Also known as stateless component.

**Example**

```js
function function_name(props) {
  return <h1>Hello, {props.name}</h1>;
}
```
