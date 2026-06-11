---
title: Props
nav_order: 3
layout: default
parent: React Foundation
---

# React Props
{: .no_toc}

## Definition
{: .no_toc}

Props in react are properties passed from parent to child a component to customize its behavior and appearance.
They are read-only meaning the receiving component cannot modify them, ensuring unidirectional data flow from parent to children.
We can consider props as an argument passed to the function. they look similar to setting HTML tag attribute.

---
<!-- 
## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

--- -->

In JSX props resembles HTML attributes.

Props are immutable, they are the readonly variable. this insures unidirectional data flow.

Change in props causes Child component to be rerender.

**Example :-**

```js
function ParentComponent() {
    // Passing props to child component
    return <ChildComponent name="Yogesh" age="26" />
}
// Accept props form parent
function ChildComponent(props) {
    const { age } = props;
    return <>
        Hi {props.name},
        Age - {age}
    </>
}
```

## props.children

this is the special type of props which is used when component do not know about the children's ahead of time.

```jsx

const ExampleChild = (props) => {
  return <header>{props.children}</header>
}
const ExampleParent = () => {
  return <ExampleChild>Hello Child</ExampleChild>
}
```

---

## Prop drilling

refers to the process of passing data from a parent component down to nested child components through props.
This situation occurs when a prop needs to be passed through several layers of nested components to reach a deeply nested child component that actually needs the prop.

**Example :-** 

```mermaid
graph TD;
  start([root]) --> nodeA[Node A];
  start -- data --> nodeB[Node B];
  nodeB -- data --> nodeD[Node D];
```