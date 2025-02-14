# 🏷️ Beginner

## 1️⃣ Components in React

- A function is a React component if its name starts with a capital letter.
- React components are JavaScript functions that **return markup**.
- React apps are built from components.
- A component is a piece of the user interface (UI) with its own **logic and appearance**.
- Components can range from small elements, like buttons, to large sections, like entire pages.

![component example](./s_thinking-in-react_ui_outline.png)

## 2️⃣ diff between components and other tags

- `<SampleComp>` Components has names start with Capital letters
- `<p></p>` Always in small letters

```jsx
// App.jsx

export default function App() {
  return (
    <>
      <h1>My heading</h1>
      <button>Click me</button>
      <Button>Click me</Button>
    </>
  );
}
```

### 3️⃣ Rules to create JSX Files

- File name must be started with Capital letter
- Must have one function with same name as File name
- apply `export default` on above function.
- That component is default component

```javascript
// Counter.jsx 👈 file name.

export default function Counter() {
  return (
    <div>
      <button>click me</button>
    </div>
  );
}
```

## 4️⃣ Expressions in JSX

use curly braces {}
eg: `<p> Addition of 2 numbers : { a + b } </p>`

```jsx
// Add.jsx

export default function Add() {
  const a = 100;
  const b = 200;
  return (
    <>
      <p>The addition of 2 number : {a + b}</p>
    </>
  );
}
```

## 5️⃣ Inserting a single Line of code

if single line, there is not need of brackets ()

```javascript
// App.jsx
export default function App() {
  return <button>click me</button>;
  // in above you we are not using (), as it has only one tag.
}
```

## 6️⃣ Inserting a Large Line of HTML

You need enclose with `( )`

```javascript
// App.jsx
export default function App() {
  return (
    <div>
      <p>line 01</p>
      <p>line 02</p>
      <p>line 03</p>
    </div>
  );
  // in above you we are using (), as it has many tags.
}
```

## 7️⃣ One Top Level Element

- Must have one parent element.
- **NOTE:** JSX will throw an error if the HTML is not correct, or if the HTML misses a parent element.
- The HTML code must be wrapped in ONE top level element or we can use `<></>`
- you can use a "fragment" to wrap multiple lines.
- [NOTE]: JSX will throw an error 👎❌ if the HTML is not properly closed.

```javascript
export default function App() {
    return (
        <button> add </button>
        <button> delete </button>
    );
}
// The above code will through error, becz no parent tag there to enclose its children tags.

// in this case we can use Fragments as shown below.
export default function App() {
    return (
        <>
            <button> add </button>
            <button> delete </button>
        </>
    );
}
```

## 8️⃣ 2 types of components in REACT

### class components ( old )

- uses javascript class to create components
- is a state-full component
- it is state-full because by default all class components has state.

### function components ( new )

- uses javascript function to create components.
- is a stateless component.
- because by default function component don't have state. we will include using `useState()` hooks.
- we will achieve all class component features in functional component using hooks 🪝.

#### Example 🍳

Sure! Here are two versions of a simple counter app, one using a functional component with hooks and the other using a class component.

### **Functional Component with Hooks:**

```jsx
import React, { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <h1>Counter: {count}</h1>
      <button onClick={() => setCount(count + 1)}>Increment</button>
      <button onClick={() => setCount(count - 1)}>Decrement</button>
      <button onClick={() => setCount(0)}>Reset</button>
    </div>
  );
}

export default Counter;
```

### **Class Component:**

```jsx
import React, { Component } from "react";

class Counter extends Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0,
    };
  }

  increment = () => {
    this.setState({ count: this.state.count + 1 });
  };

  decrement = () => {
    this.setState({ count: this.state.count - 1 });
  };

  reset = () => {
    this.setState({ count: 0 });
  };

  render() {
    return (
      <div>
        <h1>Counter: {this.state.count}</h1>
        <button onClick={this.increment}>Increment</button>
        <button onClick={this.decrement}>Decrement</button>
        <button onClick={this.reset}>Reset</button>
      </div>
    );
  }
}

export default Counter;
```

In both examples, you have a `Counter` component that displays the current count and has three buttons to increment, decrement, and reset the count.

- **Functional Component:** Uses the `useState` hook to manage the state and arrow functions to handle the button clicks.
- **Class Component:** Uses a constructor to set the initial state and class methods to handle the button clicks.

Feel free to use the one that best suits your needs! If you have any questions or need further assistance, let me know!
