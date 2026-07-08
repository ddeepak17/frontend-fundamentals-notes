# React.js Basics

## 1. What is React and Why Use It?

React is a JavaScript library used to build user interfaces. It is mainly used for building frontend applications where the UI changes based on user actions or data.

Instead of writing one large page, React lets developers break the UI into smaller reusable parts called components.

Example:

```jsx
function Welcome() {
  return <h1>Hello, Darren</h1>;
}
```

React is useful because:

- It helps build reusable UI components.
- It makes large interfaces easier to organize.
- It updates the UI when data changes.
- It works well for single-page applications.
- It is commonly used in modern frontend development.

My understanding: React helps organize the frontend by breaking the page into components. This makes the code easier to manage and reuse.

---

## 2. React Project Setup Using Vite

Vite is a build tool used to quickly create and run frontend projects. It is commonly used with React because it is fast and simple to set up.

To create a React project with Vite:

```bash
npm create vite@latest my-app
```

Then choose:

- React
- JavaScript or TypeScript

After creating the project:

```bash
cd my-app
npm install
npm run dev
```

Common commands:

```bash
npm run dev
```

Starts the development server.

```bash
npm run build
```

Creates a production build.

```bash
npm run preview
```

Previews the production build locally.

My understanding: Vite is used to quickly set up a React project and run it locally during development.

---

## 3. JSX Syntax

JSX is a syntax used in React that looks similar to HTML, but it works inside JavaScript.

Example:

```jsx
const element = <h1>Hello World</h1>;
```

JSX allows JavaScript expressions inside curly braces.

Example:

```jsx
const name = "Darren";

function App() {
  return <h1>Hello, {name}</h1>;
}
```

Important JSX rules:

- Components should return one parent element.
- Use `className` instead of `class`.
- JavaScript expressions go inside `{}`.
- Tags should be closed properly.
- Component names should start with a capital letter.

Example:

```jsx
function App() {
  return (
    <div className="card">
      <h1>React App</h1>
      <p>This is JSX.</p>
    </div>
  );
}
```

Incorrect:

```jsx
<img>
```

Correct:

```jsx
<img />
```

My understanding: JSX lets me write UI in a way that looks like HTML, but I can also use JavaScript inside it.

---

## 4. Components and Reusable UI

Components are reusable pieces of UI in React. A component can be something small like a button or something bigger like a navbar, card, or page section.

Example component:

```jsx
function Button() {
  return <button>Click Me</button>;
}
```

Using a component:

```jsx
function App() {
  return (
    <div>
      <Button />
      <Button />
    </div>
  );
}
```

Components are useful because:

- They reduce repeated code.
- They make the UI easier to organize.
- They make code easier to maintain.
- They allow the same UI pattern to be reused in different places.

My understanding: components are one of the main reasons React is useful. Instead of repeating the same code, I can create a component once and reuse it.

---

## 5. Props

Props are used to pass data from one component to another. They make components more flexible.

Example:

```jsx
function UserCard({ name, role }) {
  return (
    <div>
      <h2>{name}</h2>
      <p>{role}</p>
    </div>
  );
}
```

Using the component:

```jsx
<UserCard name="Darren" role="Software Engineer Intern" />
```

In this example, `name` and `role` are props.

My understanding: props are like inputs for components. They let one component receive data and display different content.

---

## 6. State

State is used to store data that can change while the app is running.

Example:

```jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <button onClick={() => setCount(count + 1)}>
      Count: {count}
    </button>
  );
}
```

In this example:

- `count` is the current state value.
- `setCount` updates the value.
- `useState(0)` sets the starting value to 0.

When state changes, React updates the UI.

My understanding: state is useful when something on the screen needs to change, like a counter, form input, menu open/close, or selected item.

---

## 7. Event Handling

React can respond to user actions like clicking a button, typing in an input, or submitting a form.

Example:

```jsx
function App() {
  function handleClick() {
    alert("Button clicked");
  }

  return <button onClick={handleClick}>Click Me</button>;
}
```

Common events:

- `onClick`
- `onChange`
- `onSubmit`
- `onMouseEnter`
- `onKeyDown`

My understanding: event handling lets the app respond when the user interacts with the UI.

---

## Quick Summary

React is used to build user interfaces using reusable components. Vite helps set up and run React projects quickly. JSX lets developers write UI inside JavaScript. Components help organize the UI, props pass data into components, and state manages values that change over time. React is useful because it makes frontend code more organized and easier to maintain.
