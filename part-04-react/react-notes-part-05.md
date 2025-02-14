# IMPORTANT TOPICS IN REACT

## 1️⃣ steps to follow to create new component in new file

1. Lets decide to create a component name `Sample`.
2. First create a file named `Sample.jsx`
3. Open `Sample.jsx`.

```javascript
// Sample.jsx
export default function Sample() {
  // default comp...
  return <p> Sample Component </p>;
}
```

## 2️⃣ Importing and exporting components

```javascript
// Cartoon.jsx
function Cartoon() {
  // default component
  return <p>Cartoon component</p>;
}

function Ben10() {
  return <p>Ben10 component</p>;
}

function Ben10AlienForce() {
  return <p>Ben10 component</p>;
}

export default Cartoon; // this is how you have to export default component.
export { Ben10, Ben10AlienForce }; // this is how you have to export non default components.
```

```javascript
// App.jsx
import Cartoon from "./Cartoon.jsx";
import { Ben10, Ben10AlienForce } from "./Cartoon.jsx";

function App() {
  return (
    <div>
      <Cartoon />
      <Ben10 />
      <Ben10AlienForce />
    </div>
  );
}

export default App;
```

### export

1. export default | eg: `export default Cartoon;`
2. export multiple items | eg: `export { Ben10, Ben10AlienForce };`
3. `export`, `export default` in function declaration are 2 different things. But doing export operation only.

- The export default keywords specify the main component in the file.
- 🔔`only one export default can be written in a file.` 🔔

### `import`

1. import default | eg: `import Cartoon from './Cartoon.jsx';`
2. import multiple items | eg: `import { Ben10, Ben10AlienForce } from './Cartoon.jsx';`
3. import both in single line | eg: `import Cartoon, { Ben10, Ben10AlienForce } from './Cartoon.jsx';`
4. 🔔 MOSTLY IMPORTS will be taken care by `AUTO_IMPORT` feature in VS-code. ⚠️But sometimes, AUTO_IMPORT will not work.

---

## 3️⃣ Displaying data

- using `{ }` we can display data inside markups

eg:

```javascript
// App.jsx

export function LeaveLetter() {
  // We can have more than one component in single file.
  // Like here LeaveLetter is another component inside App.jsx file.
  // where App is the default component.
  let name = "roshan";
  let problem = "cold and Cough";
  let value1 = undefined;
  let value2 = null;
  let value3 = true;
  let arr = ["apple", "orange"]; // by default in output, it will concat without any spaces.
  return (
    <div>
      <div>name : {name}</div>
      <div>problem : {problem}</div>
      <div>value1 : {value1}</div>
      <div>value2 : {value2}</div>
      <div>value3 : {value3}</div>
      <div>value4 : {value4}</div>
      <div>arr : {arr}</div>
    </div>
  );
}

function App() {
  return (
    <>
      <LeaveLetter />
    </>
  );
}
export default App;
```

- `undefined` and `null` will show nothing in webpage.
- `Boolean` will only show after using toString method.
- `array` with strings will be joined without any space.

![image](https://github.com/user-attachments/assets/a75c5910-538b-428a-91b1-91b8293361d3)

## 4️⃣ Adding styles

- `1. Write all your CSS in 'index.css' (or) App.css, simple approach.`
- `2. Write CSS using libraries (or) CDN, e.g., Bootstrap, Tailwind CSS.`
- `3. Component-based styling, e.g., Material UI, Semantic UI.`
- `4. Write CSS alongside the component, e.g., CSS Modules.`
- `5. Use styled-components library for CSS-in-JS.`
- `6. Use other CSS-in-JS libraries like Emotion.`
- `7. CSS Modules`

```bash
📂 Components
|____💄HomePage.css
|____📄HomePage.jsx
```

## 5️⃣ OTHER POINTS IN REACT

- we can use both close tag or self close tag in react components.
- eg: `<SampleComp/>`
- eg: `<SampleComp></SampleComp>`
- You can store Markup in a variable also.

## 6️⃣ Conditional rendering

Ways to write conditional rendering:

- using `if`
- using `switch`
- using ternary operator `?:`
- Short-circuit evaluation

```javascript
// using if
import React from "react";

const IfElseExample = () => {
  const isLoggedIn = false;

  if (isLoggedIn) {
    return <h1>Welcome back!</h1>;
  } else {
    return <h1>Please log in.</h1>;
  }
};

export default IfElseExample;
```

```javascript
// using switch
import React from "react";

const SwitchExample = () => {
  const userRole = "admin"; // Can be 'admin', 'user', or 'guest'

  switch (userRole) {
    case "admin":
      return <h1>Welcome, Admin!</h1>;
    case "user":
      return <h1>Welcome, User!</h1>;
    case "guest":
      return <h1>Welcome, guest</h1>;
  }
};

export default SwitchExample;
```

```javascript
// Ternary operator
import React from "react";

const TernaryExample = () => {
  const isLoggedIn = true;

  return (
    <div>{isLoggedIn ? <h1>Welcome back!</h1> : <h1>Please log in.</h1>}</div>
  );
};

export default TernaryExample;
```

```javascript
// Short-circuit evaluation
import React from "react";

const App = () => {
  const isError = true; // Change this to false to see the difference

  return (
    <div>
      <h1>Welcome to the App</h1>
      {isError && <p>You are wrong!</p>}
      <p>My email is sample@gmail </p>
    </div>
  );
};

export default App;
```

## 7️⃣ Rendering lists

- It is about displaying items within the array.
- To display, we use map concept.

### steps

1.  you need a array to render list.
2.  use below syntax.

        {
              arr.map( ( value, index ) => {
                 return <li key={index} > { value } </li>;
              })
        }

3.  You can replace above markup with **component** also.

Here's a very simple example of rendering a list using an unordered list (`<ul>`) in React.

### **Rendering a List (ListExample.jsx)**

```jsx
import React from "react";

const ListExample = () => {
  const fruits = ["Apple", "Banana", "Cherry", "Grapes"];

  return (
    <div>
      <h1>Fruit List</h1>
      <ul>
        {fruits.map((value, index) => {
          return <li key={index}>{fruit}</li>;
        })}
      </ul>
    </div>
  );
};

export default ListExample;
```

### Explanation

- **Array**: `fruits` is a simple array of fruit names.
- **Rendering**: The `.map()` function is used to loop through the `fruits` array and render each fruit as a list item (`<li>`).
- **Key**: A `key` is added to each `<li>` for uniqueness, which is important when rendering lists in React. Or Else you will get a ⚠️ warning in your console.

This will output a list of fruits in an unordered list on the page.

---

## 1️⃣2️⃣ Remove React.StrictMode

- to avoid loading ☠️ twice ☠️
- If you don't want to render your component twice
- then remove it.
- this `<React.StrictMode>` will be available in `index.js`

`<React.StrictMode>` lets you find common bugs in your components early during development.

### `index.js`

```javascript
import React from "react";
import ReactDOM from "react-dom/client";
import "./index.css";
import App from "./App";
import reportWebVitals from "./reportWebVitals";

const root = ReactDOM.createRoot(document.getElementById("root"));
// here in below case. we have used.
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();
```

### 1️⃣3️⃣ Strict Mode enables the following development-only behaviors

- Your components will re-render an extra time to find bugs caused by impure rendering.
- Your components will re-run Effects an extra time to find bugs caused by missing Effect cleanup.
- Your components will be checked for usage of deprecated APIs.

## 1️⃣4️⃣ rendering

- First time React display the content in webpage by reading components.
- First time displaying content is called rendering.

## 1️⃣5️⃣ re-rendering

- On any change in `props`, `state` or `useEffect` will reload the component.
- This is called re-rendering

## 1️⃣6️⃣ re-conciliation

- The process of displaying page using virtual DOM and diff algorithm.
