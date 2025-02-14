## 1️⃣0️⃣ Sharing data between components ( props )

- Props is used to share data between components

### PARENT to CHILD

- passing values down to children component using props

```jsx
function Card({ name, id }) {
  return (
    <div>
      {id} : {name}
    </div>
  );
}

export default function Parent() {
  return (
    <ul>
      <Card id={112} name={"doremon"} />
      <Card id={123} name={"doremi"} />
    </ul>
  );
}
```

### CHILD TO PARENT

        you can pass values from a child component to a parent component in React, but since data flow in
         React is unidirectional (from parent to child), you'll need to pass a callback function from the
         parent to the child as a prop.
        The child component can then use this callback function to send data back to the parent.

- passing values up to parent component using function ( call back function ) as props
- But mostly people will not use this. instead they will go to useContext concept.

- `<ComponentName  setCount={setCount}  handleClick={handleClick}/>`

- `function ComponentName({ setCount, handleClick })`

```javascript
import { useState } from "react";

function ChildComp({ count, setCount }) {
  // but using this function 👆
  // we are able to state value which in PARENT component
  function handleIncrBtn() {
    setCount(count + 1);
  }
  function handleDecrBtn() {
    setCount(count - 1);
  }
  return (
    <>
      <button onClick={handleIncrBtn}> incr </button>
      <button onClick={handleDecrBtn}> decr </button>
    </>
  );
}
function ParentComp() {
  const [count, setCount] = useState(0);
  return (
    <>
      <p> my count : {count} </p>
      {/*          👇 here count state is being passed PARENT to CHILD component from  */}
      <ChildComp count={count} setCount={setCount} />
      {/* We are passing our setCount function 👆 here. 
                so that I can update my count state which is in PARENT component, 
                inside CHILD component.
                
                This is literally like passing value from CHILD to PARENT component.
            */}
    </>
  );
}

function Sample() {
  return <ParentComp />;
}

export default Sample;
```

## 1️⃣1️⃣ React Dev Tools

A browser extension used to debug react application.

- we can view structure of React components and its hierarchy.
- we can watch over states and props.
