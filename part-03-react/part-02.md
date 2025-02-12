# Beginner

- Creating your first React app using Vite.
- Vite is a build tool that aims to provide a faster and leaner development experience for modern web projects.
- Lets see step-by-step guide:

## **1. Install Node.js and npm**

Make sure you have Node.js and npm installed on your computer. You can download and install them from the [official Node.js website](https://nodejs.org/).

## **2. Create a New Project Using Vite**

- Open your terminal or command prompt where you want to create the project.
- And run the following command to create a new project:

```bash
npm create vite@latest
```

This command will prompt you to enter a project name and select a framework and variant. For a React project, follow these steps:

- Enter the project name (e.g., `my-react-app`).
- Choose `React` as the framework.
- Choose `JavaScript` or `TypeScript` as the variant, depending on your preference.

## **3. Navigate to the Project Directory**

After the project is created, navigate to the project directory using the following command:

```bash
cd my-react-app
```

- Open you VSCODE, go to `file > open folder`, Then open your project folder.
- To check you have opened you project correctly. On `top middle`, you will see the project folder topic.

## **4. Install Dependencies**

- Install the necessary dependencies by running:
- Open `command prompt`/`terminal` in VS-CODE. go to `view > terminal`.

```bash
npm install
```

- Above command will create a folder called `node_modules` which has all necessary packages.

## **5. Start the Development Server**

Start the development server using the following command:

```bash
npm run dev
```

This will start the development server, and you can view your React app in the browser by navigating to the URL provided (usually `http://localhost:5713`).

## **6. Project Structure**

Here is an overview of the project's structure:

```plaintext
my-react-app/
├── node_modules/
├── public/
│   ├── vite.svg
├── src/
│   ├── assets/
│   ├── components/
│   ├── App.jsx
│   ├── main.jsx
├── .gitignore
├── index.html
├── package.json
├── vite.config.js
```

- **index.html**: The main HTML file.
- **src/App.jsx**: The main React component.
- **src/main.jsx**: The entry point of the React application.

## **7. Editing the App**

- Don't remove the following files, 💀 Just remove the content 📄
- files are `index.css` and `App.css`

Keep following in content in following files.

### `📄 App.jsx`

```jsx
import React from "react";

export default function App() {
  return (
    <div>
      <h1>Hello, Vite and React!</h1>
    </div>
  );
}
```
