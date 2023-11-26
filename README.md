
# 🥳 React Interview Ques :

there react question based on topic :
## 😁 BEGINNER ======>



## Q1. What is React?

React is an `open-source front-end JavaScript library` that is used for building `composable user interfaces`, especially for `single-page applications`. It is used for handling view layer for web and mobile apps based on components in a declarative approach.


```
like a toolbox that helps developers create the visual parts of websites or web applications 
```

## Q2. What are the major features of React?

The major features of React are:

- Uses `JSX syntax`, a syntax extension of JS that allows developers to write HTML in their JS code.
- It uses `Virtual DOM` instead of Real DOM considering that Real DOM manipulations are expensive.
- Supports `server-side rendering` which is useful for Search Engine Optimizations(SEO).
- Follows `Unidirectional` or one-way data flow or data binding.
- Uses `reusable/composable UI` components to develop the view.

```
JSX is quite similar to HTML, but it's a special syntax used in React 
ike a bilingual person who can speak both JavaScript and HTML at the same time.
```

```
 Virtual DOM:
 It keeps a lightweight copy of the web page called the "virtual DOM," which helps it figure out what parts of the page need to change. This makes updates faster and more efficient.
```

```
Component-Based Architecture:
Think of components as building blocks,Each piece does a specific job and can be used over and over again in different combinations to build something larger.
```

```
Unidirectional Data Flow:
This means changes in the data affect how the user interface looks, and when users interact with the interface, it doesn’t directly change the data. 
```
## Q3. What is JSX? How is it different from HTML?

HTML: 
- HTML as a set of building blocks or instructions you use to create the structure of a web page.
- It's like putting together a Lego set by following a specific manual. For example, you use HTML tags like `<div>`, `<p>`, `<h1>`, and `<img>` to define different parts of a web page, such as paragraphs, headers, images, etc.

JSX:
- JSX is quite similar to HTML, but it's a special syntax used in React to describe what the user interface should look like.
- Instead of writing separate instructions in JavaScript to create elements (like document.createElement('div')), in JSX, you write HTML-like code directly inside your JavaScript files. For example:

```
const myElement = <h1>Hello, JSX!</h1>;
```

Differences between JSX and HTML:
- **Syntax:** JSX allows you to write HTML-like code directly in JavaScript files, making it more convenient for developers working with React

- **Dynamic Content:**
JSX also allows you to embed JavaScript expressions within curly braces {}. This means you can dynamically insert values or execute JavaScript code within your HTML-like syntax.

- **ClassName vs. Class:**
In HTML, we use class to define CSS classes for elements. In JSX, to avoid conflicts with JavaScript's class keyword, you use className instead.

## Q4. What is the virtual DOM in React? Explain its working principle.

- The virtual DOM in React is essentially a `lightweight copy` of the `actual browser DOM`.

- It works by `comparing changes made`, `identifies what's different`, and `updates only those parts` in the real web page.


- It acts as a `middleman` between the developer-written code and the real DOM. When changes occur in a React application, React `first updates this virtual representation` rather than directly manipulating the browser's DOM.


- This process speeds up rendering and improves performance by `minimizing unnecessary updates` to the `entire page`.
## Q5. What are the differences between class components and functional components?

**Class Components:**

- **Syntax:** Defined with ES6 classes, extend **`React.Component`**.
- **State Handling:** Manage state using **`this.state`** and **`setState()`**.
- **Lifecycle Methods:** Utilize methods like **`componentDidMount`**, **`componentDidUpdate`**, etc.
- **Complexity:** Can be more verbose due to the use of **`this`** and lifecycle methods.
```
- Class components are like the older, traditional schools where things were more structured
- principal in a school, class components have more features and can manage their own state (data) using this.state. 
- More Boilerplate, Kinda Like Lengthy Forms
```

 **Functional Components:**

- **Syntax:** Defined as simple JavaScript functions.
- **State Handling:** Use hooks (**`useState`**, **`useEffect`**) to manage state and lifecycle.
- **No this Keyword:** Avoid reliance on **`this`**, making them simpler and more predictable.
- **Easier Testing:** Easier to test due to their functional nature.

```
- Functional components are more modern, like flexible workspaces where you can adapt and rearrange things easily.
- Focused on Doing One Thing Well 
- Concise and Straightforward, Like Quick Text Messages
```


## Q6. What are stateful and stateless components?

- Stateful components, known as **class components**, manage their own state using **`this.state`** and handle complex logic and data changes.

- Stateless components, **functional components**, do not manage state and focus on rendering UI based on received props. They are simpler and purely presentational.
## Q7. How to create components in React?

Components are the building blocks of creating User Interfaces(UI) in React. There are two possible ways to create a component.

**Function Components:** This is the simplest way to create a component. Those are pure JavaScript functions that accept props object as the first parameter and return React elements to render the output:
```
function Greeting({ message }) {
  return <h1>{`Hello, ${message}`}</h1>;
}
```
**Class Components:** You can also use ES6 class to define a component. The above function component can be written as a class component:

```
class Greeting extends React.Component {
  render() {
    return <h1>{`Hello, ${this.props.message}`}</h1>;
  }
}
```
## Q8.When to use a Class Component over a Function Component?

**Use Class Components when:**
- You need complex state management with intricate logic.
- Working on legacy codebases or projects where class components are already in use.


**Use Function Components when:**
- Simplicity and readability are a priority.
- Performance optimization is crucial.
- Utilizing hooks for state management and side effects.
- Emphasizing component reusability and composition.
## Q9. What is pure component ?

pure component in React is a way to build components that know when they actually need to update and re-render. Think of it as a smart way for components to avoid unnecessary work.

When you create a pure component, it checks if the data it receives (like props or state) has changed since the last time it was rendered. If the new data is the same as the old data, the pure component says, "Hey, nothing has changed here, so no need to repaint or re-render." This helps in saving processing power and making your app more efficient.


## Q10. What is state in React?

- State of a component is an object that holds some information that may change over the lifetime of the component. 
- The important point is whenever the state object changes, the component re-renders. 
- It is always recommended to make our state as simple as possible and minimize the number of stateful components.
## Q11. What are props in React?
Props in React are essentially a means of transferring data from a parent component to a child component. They're read-only and help create more dynamic and reusable components.

```
Props in React are like items in a lunchbox that a parent gives to a child. They're pieces of information passed from a parent component to a child component to use for displaying content or performing actions.

```
**Passing Data from Parent to Child Component:**

1. **Parent Component:** Passes data by specifying attributes in the child component similar to HTML attributes.
    
    ```jsx
    <ChildComponent propName={propValue} />
    
    ```
    
2. **Child Component:** Receives data through props and accesses it within the component.

```
const ChildComponent = (props) => {
  return (
    <div>
      <p>{props.propName}</p>
    </div>
  );
};


```
## Q12. Can we pass data from child to parent ? if yes then How ?

In React, data can be passed from a child component to a parent component by passing a function from the parent to the child as a prop as callback. The child component can invoke this function, passing any necessary data, enabling communication between the components and allowing the child to update the parent's state or trigger actions.

1. **Parent Component:** Define a function in the parent component that handles the data received from the child.
    
    ```jsx
    
    const ParentComponent = () => {
      const handleDataFromChild = (data) => {
        // Handle the received data from the child component
        console.log("Data received from child:", data);
        // Perform actions or update state based on the received data
      };
    
      return (
        <div>
          {/* Pass the function as a prop to the child component */}
          <ChildComponent sendDataToParent={handleDataFromChild} />
        </div>
      );
    };
    
    ```
    
2. **Child Component:** Accept the function passed from the parent as a prop and call it to send data back to the parent.
    
    ```jsx
 
    const ChildComponent = ({ sendDataToParent }) => {
      const sendData = () => {
        const data = "Data from child component";
        // Call the function received from the parent, passing the data
        sendDataToParent(data);
      };
    
      return (
        <div>
          <button onClick={sendData}>Send Data to Parent</button>
        </div>
      );
    };
    
    ```
    


## Q13. What is the difference between state and props?

- **Mutability:** Props are immutable and cannot be changed from within the component, while state can be changed using setState().
- **Source:** Props are passed to a component from its parent, while state is managed internally within the component.
- **Scope:** Props are available throughout the component's lifecycle, whereas state is limited to the component where it's defined.
## Q14. Why should we not update the state directly?

- Updating state directly bypasses React’s internal mechanisms, leading to potential inconsistencies, bugs, and unpredictable behavior due to which React not detecting the change properly. 
- Always use the setState() method provided by React to update state, ensuring proper rendering, predictable behavior, and compatibility with React's optimization strategies.
## Q15. What is the difference between HTML and React event handling?

Below are some of the main differences between HTML and React event handling,

**1.** In HTML, the event name usually represents in lowercase as a convention:
```
<button onclick="activateLasers()"></button>
```
Whereas in React it follows camelCase convention:
```
<button onClick={activateLasers}>
```
**2.** In HTML, you can return false to prevent default behavior:
```
<a
  href="#"
  onclick='console.log("The link was clicked."); return false;'
/>
```
Whereas in React you must call preventDefault() explicitly:

```
function handleClick(event) {
  event.preventDefault();
  console.log("The link was clicked.");
}
```
**3.** In HTML, you need to invoke the function by appending `()` Whereas in react you should not append `()`with the function name. (refer "activateLasers" function in the first point for example)


## Q16. What is the significance of keys in React?

Keys in React are unique identifiers assigned to components in a list. They help React efficiently identify and manage changes when working with lists of items, aiding in faster updates and ensuring that components maintain their state correctly. Just like labels on books, keys help React keep track of individual components, making things more organized and easier to manage.

**Imagine Organizing Books on Shelves:**

Think of a shelf where you organize books. Each book has a unique identifier, like a label or tag. When you rearrange the books, you can quickly identify and move a specific book by looking at its tag.

```
javascriptCopy code
const ItemList = () => {
  const data = [
    { id: 1, name: 'Apple' },
    { id: 2, name: 'Banana' },
    { id: 3, name: 'Orange' }
  ];

  return (
    <ul>
      {data.map((item) => (
        <li key={item.id}>{item.name}</li>
      ))}
    </ul>
  );
};

ReactDOM.render(<ItemList />, document.getElementById('root'));
```
## Q17. What are synthetic events in React?

- Synthetic events in React are a unified way of handling browser events. They abstract native browser events, ensuring consistent behavior across browsers, optimizing performance, and providing an interface similar to native events for event handling in React components.

- SyntheticEvent is a cross-browser wrapper around the browser's native event. Its API is same as the browser's native event, including stopPropagation() and preventDefault(), except the events work identically across all browsers. The native events can be accessed directly from synthetic events using nativeEvent attribute.

```
function BookStore() {
  handleTitleChange(e) {
    console.log('The new title is:', e.target.value);
    // 'e' represents synthetic event
    const nativeEvent = e.nativeEvent;
    console.log(nativeEvent);
    e.stopPropogation();
    e.preventDefault();
  }

  return <input name="title" onChange={handleTitleChange} />
}
```


## Q18. What is Lifting State Up in React?

When several components need to share the same changing data then it is recommended to lift the shared state up to their closest common ancestor. That means if two child components share the same data from its parent, then move the state to parent instead of maintaining local state in both of the child components.
## Q19. What is prop drilling?

Prop Drilling is the process by which you pass data from one component of the React Component tree to another by going through other components that do not need the data but only help in passing it around.
## (optional) Explain the differences between controlled and uncontrolled components in React.

**Controlled:** A component that controls the input elements within the forms on subsequent user input is called Controlled Component, i.e, every state mutation will have an associated handler function.

For example, to write all the names in uppercase letters, we use handleChange as below,
```
handleChange(event) {
  this.setState({value: event.target.value.toUpperCase()})
}
```

**UnControlled:** The Uncontrolled Components are the ones that store their own state internally, and you query the DOM using a ref to find its current value when you need it. This is a bit more like traditional HTML.

In the below UserProfile component, the name input is accessed using ref.

```
class UserProfile extends React.Component {
  constructor(props) {
    super(props);
    this.handleSubmit = this.handleSubmit.bind(this);
    this.input = React.createRef();
  }

  handleSubmit(event) {
    alert("A name was submitted: " + this.input.current.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          {"Name:"}
          <input type="text" ref={this.input} />
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```
In most cases, it's recommend to use controlled components to implement forms. In a controlled component, form data is handled by a React component. The alternative is uncontrolled components, where form data is handled by the DOM itself.
## Q20. Describe the component lifecycle in React.

- The component lifecycle in React encompasses three key phases: Mounting, Updating, and Unmounting.

- During Mounting, a component is created and added to the DOM. It goes through **`constructor()`** for initial setup, **`render()`** to display its UI, and **`componentDidMount()`** where we can perform actions after the component is mounted.

- In the Updating phase, when the component's state or props change, React checks whether to re-render via **`shouldComponentUpdate()`**, then invokes **`render()`** to update the UI. Finally, **`componentDidUpdate()`** is called after the component updates.

- The Unmounting phase involves **`componentWillUnmount()`**, executed just before a component is removed from the DOM, allowing for cleanup tasks.

----Undersatnding-----
> Think of the component lifecycle in React as the journey of a plant, from the moment it's planted until it grows, blossoms, and eventually withers away. In simpler terms, here's how the component lifecycle works in React:
> 

> Planting the Seed (Mounting Phase):
> 

> **Birth - `constructor()`:** It's like preparing the soil for the seed. The `constructor()` is the first method called when a component is created. Here, you set up initial values and prepare things before the component is "planted."
> 

> **Growing - `render()`:** Just as the seed starts growing roots and stems, the `render()` method "grows" the component by returning what should be displayed on the screen. It's where the component starts taking shape.
> 

> **Sprouting Leaves - `componentDidMount()`:** Once the plant has grown a bit, it starts to show leaves. Similarly, `componentDidMount()` is called after the component is displayed on the screen for the first time. It's like the moment the plant starts to flourish. Here, you might do things like fetch data or set up subscriptions.
> 

> Blooming and Adapting (Updating Phase):
> 

> **Changes - `componentDidUpdate()`:** As the plant grows, it might change its appearance or size. Similarly, when a component's state or props change, `componentDidUpdate()` is called. This is a good place to perform actions after the component updates, like fetching new data based on changes.
> 

> Aging and Withering (Unmounting Phase):
> 

> **Fading Away - `componentWillUnmount()`:** Eventually, the plant withers away. Similarly, when a component is removed from the screen or unmounted, `componentWillUnmount()` is called. Here, you can clean up any resources or subscriptions used by the component.
>
## Q21. Why React uses className over class attribute?

React uses className instead of class in JSX to apply CSS classes to HTML elements within components to avoid conflicts with JavaScript's class keyword. This helps maintain compatibility and prevents naming collisions with JavaScript syntax in React components.

```
function MyComponent() {
  return <div className="my-class">Hello, world!</div>;
}

```

## Q22.What are the limitations of React?

Learning Curve: Initial complexity for newcomers due to JSX and component-based architecture.
Boilerplate Code: Complex apps might require additional libraries, leading to more code.
JSX Dependency: Might pose challenges for developers accustomed to HTML syntax.
Performance Impact: Large or deeply nested component trees can impact performance.
Tooling Complexity: Vast library choices might create confusion in tool selection.
Community Fragmentation: Diverse libraries could lead to conflicting approaches.
SEO Challenges: Initial hurdles for SEO in SPA implementations.
Lack of Built-in Solutions: No built-in routing or state management in React core.
Constant Evolution: Continuous updates might cause issues during upgrades.
Steep Learning Curve for Advanced Patterns.
## Q23.What are Higher-Order Components?

- Higher-Order Components (HOCs) in React are functions that take a component and return a new enhanced component. They enable reusability and shareable logic by abstracting common functionalities and behaviors from components.

- In short, HOCs are functions that enhance components by adding extra capabilities or behaviors without changing their original logic, promoting code reuse and composability in React applications.

```
import React, { useEffect } from 'react';

// Higher-Order Component: withLogging
const withLogging = (WrappedComponent) => {
  const WithLogging = (props) => {
    useEffect(() => {
      console.log(`Component ${WrappedComponent.name || 'Anonymous'} mounted`);
      return () => {
        console.log(`Component ${WrappedComponent.name || 'Anonymous'} will unmount`);
      };
    }, []);

    return <WrappedComponent {...props} />;
  };

  return WithLogging;
};

// Component to enhance with the HOC
const MyComponent = () => {
  return <div>Hello, I am the wrapped component!</div>;
};

// Enhance MyComponent using withLogging HOC
const MyEnhancedComponent = withLogging(MyComponent);

export default MyEnhancedComponent;

```
## Q24. What is context?

Context provides a way to pass data through the component tree without having to pass props down manually at every level.
## Q25. How to use styles in React?

The style attribute accepts a JavaScript object with camelCased properties rather than a CSS string. This is consistent with the DOM style JavaScript property, is more efficient, and prevents XSS security holes.

```
const divStyle = {
  color: "blue",
  backgroundImage: "url(" + imgUrl + ")",
};

function HelloWorldComponent() {
  return <div style={divStyle}>Hello World!</div>;
}
```
## Q26. What is the use of react-dom package?

`react-dom` is a package in React primarily used for rendering React components into the DOM, managing the interactions between React's virtual DOM and the actual browser DOM, supporting React Portals, enabling DOM manipulation, event handling, error boundaries, and server-side rendering hydration.
## Q27.What is the purpose of render method of react-dom?

The `render()` method in `react-dom` is used to render React components into the DOM, taking a React element or component and mounting it into a specified container element in the HTML document.

```
import React from 'react';
import ReactDOM from 'react-dom';

// Example React component
const App = () => {
  return <h1>Hello, React!</h1>;
};

// Mounting the React component into the DOM
ReactDOM.render(
  <App />,
  document.getElementById('root') // The target container element in the HTML
);

```

- App is a simple React component.
- ReactDOM.render() takes the <App /> element (or component) and mounts it into the HTML document at the element with the ID 'root'. This is where the React component will be rendered within the HTML DOM structure.

The ReactDOM.render() method is the entry point for rendering React components into the DOM and is typically called once to initialize the main component of a React application.
## Q28. Why does strict mode render twice in React?

- In React's Strict Mode (`<React.StrictMode>`), components may render twice in development mode. 
- This intentional behavior helps catch and highlight potential issues, such as `unsafe lifecycle` methods or `unintended side-effects`, aiding developers in identifying and fixing problems early in the development process. 
- This double render doesn't occur in production builds and is a tool for enhancing code quality during development.
## Q29. What is code Splittting in react

Code splitting in React is a technique used to improve performance by splitting your JavaScript bundle into smaller chunks, allowing parts of your application to be loaded asynchronously when needed. This technique helps reduce the initial load time of your web application, as only the necessary code for the current view or route is loaded, rather than loading the entire application at once.

There are different ways to perform code splitting in React:

1. **Dynamic Import (with `import()`):** The dynamic `import()` function allows you to asynchronously import modules, splitting code at specific points. It returns a Promise that resolves to the module's namespace object, allowing you to use dynamic imports within your components.

    Example:
    ```javascript
    const MyComponent = React.lazy(() => import('./MyComponent'));
    ```

    `React.lazy` and `Suspense` are used for code splitting with dynamic imports in React. This method is commonly used with React.lazy for lazy loading components.

2. **React.lazy and Suspense:** `React.lazy` is a built-in React feature that enables lazy loading of components. `Suspense` is used to handle loading states while the lazily loaded components are being fetched.

    Example:
    ```javascript
    const LazyComponent = React.lazy(() => import('./LazyComponent'));

    function MyComponent() {
      return (
        <React.Suspense fallback={<div>Loading...</div>}>
          <LazyComponent />
        </React.Suspense>
      );
    }
    ```

3. **Webpack or Other Bundlers:** Tools like Webpack provide code-splitting capabilities. With Webpack, you can use dynamic imports or `import()` statements along with its configuration to split chunks based on routes or components.

    Example (Webpack):
    ```javascript
    // webpack.config.js
    module.exports = {
      //...
      optimization: {
        splitChunks: {
          chunks: 'all',
        },
      },
    };
    ```

    Webpack's `splitChunks` optimization allows you to split chunks based on shared dependencies, reducing duplication and optimizing load times.

Code splitting is beneficial for larger applications to improve performance, reduce initial load times, and enhance the overall user experience by loading only the required code when navigating through different parts of the application.

## Q30. What is Lazy Loading ?
Lazy loading is a technique used in web development to defer the loading of non-critical resources (such as images, scripts, or components) until they are needed. In the context of web applications, lazy loading typically refers to loading parts of an application only when they are required, rather than loading everything upfront.

In the context of React or other JavaScript frameworks, lazy loading usually involves deferring the loading of components or modules until they are needed, particularly in situations where the entire application bundle might be large or contains components that are not immediately required when the app loads.

In React, lazy loading is often achieved using the `React.lazy()` function combined with dynamic imports (`import()`). `React.lazy()` allows you to lazily load components, splitting the bundle and loading the component's code only when it's required.

Example in React using `React.lazy()` and `Suspense`:

```javascript
const MyLazyComponent = React.lazy(() => import('./MyLazyComponent'));

function App() {
  return (
    <React.Suspense fallback={<div>Loading...</div>}>
      <MyLazyComponent />
    </React.Suspense>
  );
}
```

In this example, `MyLazyComponent` will be loaded asynchronously when it's first rendered, and the `React.Suspense` component displays a fallback content (in this case, a "Loading..." message) until the lazy component finishes loading.

Lazy loading is beneficial for optimizing web application performance by reducing the initial load time. It allows for a better user experience by loading only the essential parts of the application upfront and deferring the loading of less critical or less immediately required resources until they're actually needed, leading to faster initial page loads and improved perceived performance.
## Full form

**CRA:** create-reacte-app
**RWD:** Responsive web developnment
**PWA:** 
Progressive Web Apps
