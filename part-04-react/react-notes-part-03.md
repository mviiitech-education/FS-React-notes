# FAQ while running your vite+REACT project

If you face any issue while running your project. check below points.

1. Make sure, your changes have been saved properly.
1. Check your spellings. - eg: `✅ className  | ❌ classname` `✅ onClick    | ❌ onclick`
1. Stop your running project by using `ctrl + C` within in terminal. Again start react project using `npm run dev`.
1. But still not working properly. Then close your VS-Code project and open it again. It will work.
1. If you do any thing wrong, The page will be full white blank. Then where to see the error. Open developer tools by doing inspect. In console tab, you will see the errors.

## Node JS

- To use React in production, you need npm which is included with Node.js.
- npx ( **N**ode **P**ackage e**X**ecute ):
  - Execute package without any prior installing of packages.
- npm ( **N**ode **P**ackage **M**anager ):
  - Use to manage, install and remove packages for Node JS.

## To check if node js is installed

1. open command prompt
2. check below commands are working

`node --version`
`npm --version`
`npx --version`

## React

- React is a `JavaScript` library for building user interfaces.
- Created by Facebook / Meta.
- React is used to build `single-page` applications.
- React is a tool for building UI components.
- **NOTE:** React follows a component based architecture.

### `.js` vs `.jsx`

- Usually in react a file which save as `.js` or `.jsx` both will be valid by react.
- But it is preferred to write `.jsx`.
- In react when javascript files are saved as below extension.
  Following properties are enabled.

1. `.js` => not preferred.
2. `.jsx` => preferred.

**version 16** has major changes
Current React latest version **18**

## React History

**version 16** has major changes
Current React latest version **18**

## React Docs

legacy : <https://legacy.reactjs.org/>  
modern : <https://react.dev/>

## How React works ?

- Here All our component jsx files are converted to pure js files.
  This file is named as bundle.js file. and included in `<head>` tag.
- Mainly all our Components are loaded inside `<div id="root">`

### **Virtual DOM in React**

[React Virtual DOM Reference](https://legacy.reactjs.org/docs/faq-internals.html)

_React uses a VIRTUAL DOM (VDOM) to improve performance._

- **Create:** React creates a VDOM in memory.
- **Update:** When there's a change, React updates the VDOM first.
- **Compare:** React compares the VDOM with the real DOM.
- **Apply Changes:** React updates only the parts of the real DOM that need changes.

**Why use VDOM?**

- **Speed:** Updating the real DOM is slow.
- **Efficiency:** Manipulating the VDOM is fast because nothing gets drawn on the screen until necessary.

This approach ensures efficient updates and better performance in your applications.

## very very important

### **NOTE:**

- JSX follows new rules to write HTML and CSS codes.
- **Example:**

**HTML example:**

```html
<div class="container"></div>
```

**JSX example:**

```jsx
// App.jsx
export default function App() {
  return (
    <>
      <div className="container"></div>
    </>
  );
}
```
