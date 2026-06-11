---
title: States
nav_order: 4
layout: default
parent: React Foundation
---

# React States
{: .no_toc}

## Definition
{: .no_toc}


State in react is a built-in Component level object that is use to store and manage data change over time.

When state changes, React automatically re-renders the component to reflect the updated data.

## Key Characteristics
- Local and Private: State is specific to a component instance and cannot be directly modified by parent components.
- Mutability: Unlike props, which are read-only, state is mutable and updated via specific methods.
- Automatic Updates: Changes to state trigger the reconciliation algorithm, ensuring only necessary parts of the DOM are updated.

**Example :-**

```js
import React, { useState } from 'react';
function ExampleComponent () {
    const [count, setCount] = useState(0);
    return(
        <>
            <p>Count is {count}</p>
            <button onClick={()=>setCount(pre => pre + 1)}>Increase</button>
        </>
    )
}
```