[![MasterHead](https://github.com/Sakib963/bistro-boss-server/assets/66853064/51508d0e-6e5d-47bb-892c-433205f28283)](https://github.com/Sakib963)

<h1 align="center">REACT INTERVIEW QUESTIONS AND ANSWERS</h1>

## 1. What is React?

React JS is a JavaScript Library for building user interfaces. It is declarative, efficient and flexible. Also, React is fast and component Based Library.

## 2. What are the major features of React?

The major features of React are:

- Uses JSX syntax, a syntax extension of JS that allows developers to write HTML in their JS code.
- It uses Virtual DOM instead of Real DOM considering that Real DOM manipulations are expensive.
- Supports server-side rendering which is useful for Search Engine Optimizations(SEO).
- Follows Unidirectional or one-way data flow or data binding.
- Uses reusable/composable UI components to develop the view.

<div id='what-is-jsx'>
<h2>3. What is JSX?</h2>
<p>JSX is a syntax extension for JavaScript that let's you write HTML-like markup inside a JavaScript file. Rules of JSX:</p>
<ul>
<li>To return multiple elements from a component, wrap them with a single parent tag like or empty fragment <></>.</li>
<li>'class' attribute becomes 'className'</li>
<li>Properties are written in camelCase.</li>
<li>Tags must be closed.</li>
</ul>
</div>

## 4. What is the difference between Element and Component?

An Element is a plain object describing what you want to appear on the screen in terms of the DOM nodes or other components. Elements can contain other Elements in their props. Creating a React element is cheap. Once an element is created, it cannot be mutated.

```
<div id="login-btn">Login</div>
```

Whereas a component can be declared in several different ways. It can be a class with a render() method or it can be defined as a function. In either case, it takes props as an input, and returns a JSX tree as the output:

```
const Button = ({ handleLogin }) => (
  <div id={"login-btn"} onClick={handleLogin}>
    Login
  </div>
);
```

## 5. What is state in React?

State of a component is an object that holds some information that may change over the lifetime of the component. The important point is whenever the state object changes, the component re-renders.

A built in react object, used to contain data about the component. It is changeable over time and changes in state causes re-render.

## 6. What are props in React?

Props are inputs to components. They are single values or objects containing a set of values that are passed to components on creation similar to HTML-tag attributes. Here, the data is passed down from a parent component to a child component.

## 7. What is the difference between state and props?

In React, both state and props are plain JavaScript objects and used to manage the data of a component, but they are used in different ways and have different characteristics. state is managed by the component itself and can be updated using the setState() function. Unlike props, state can be modified by the component and is used to manage the internal state of the component. Changes in the state trigger a re-render of the component and its children. props (short for "properties") are passed to a component by its parent component and are read-only, meaning that they cannot be modified by the component itself. props can be used to configure the behavior of a component and to pass data between components.

## 8. What is useState()?

&rarr; Allows us to have state variables in functional component.
<br/>
&rarr; Takes the initial state to the function.
<br/>
&rarr; Returns a variable with the current state value and a function to update it.

## 9. What is useEffect()?

&rarr; To provide a way to handle performing side effects.<br/>
&rarr; Doesn't affect the rendering or performances of the component that it's in.<br/>
&rarr; Performs asynchronous tasks.

## 10. What is useEffect cleanup function? OR Why is the cleanup function useful?

&rarr; The useEffect cleanup allows ys to tidy up our code before our component unmounts.<br/>
&rarr; When our code runs and reruns for every render, useEffect also cleanup after itself using the cleanup function.<br/>
&rarr; The cleanup function prevents memory leaks and remove some unnecessary and unwanted behaviors.

## 11. What are synthetic events in React?
SyntheticEvent is a cross-browser wrapper around the browser's native event. Its API is same as the browser's native event, including stopPropagation() and preventDefault(), except the events work identically across all browsers. The native events can be accessed directly from synthetic events using nativeEvent attribute.

Let's take an example of BookStore title search component with the ability to get all native event properties
```javascript
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

## 12. What are inline conditional expressions?
You can use either if statements or ternary expressions which are available from JS to conditionally render expressions. Apart from these approaches, you can also embed any expressions in JSX by wrapping them in curly braces and then followed by JS logical operator &&.
```jsx
<h1>Hello!</h1>;
{
  messages.length > 0 && !isLogin ? (
    <h2>You have {messages.length} unread messages.</h2>
  ) : (
    <h2>You don't have unread messages.</h2>
  );
}
```

## 13. What is "key" prop and what is the benefit of using it in arrays of elements?
A key is a special attribute you should include when creating arrays of elements. Key prop helps React identify which items have changed, are added, or are removed.

Keys should be unique among its siblings. Most often we use ID from our data as key:
```javascript
const todoItems = todos.map((todo) => <li key={todo.id}>{todo.text}</li>);
```
When you don't have stable IDs for rendered items, you may use the item index as a key as a last resort:
```javascript
const todoItems = todos.map((todo, index) => (
  <li key={index}>{todo.text}</li>
));
```
Note:

* Using indexes for keys is not recommended if the order of items may change. This can negatively impact performance and may cause issues with component state.
* If you extract list item as separate component then apply keys on list component instead of li tag.
* There will be a warning message in the console if the key prop is not present on list items.
* The key attribute accepts either string or number and internally convert it as string type.

## 14. What is the use of refs?
The ref is used to return a reference to the element. They should be avoided in most cases, however, they can be useful when you need a direct access to the DOM element or an instance of a component.

## 15. What is Virtual DOM?
The Virtual DOM (VDOM) is an in-memory representation of Real DOM. The representation of a UI is kept in memory and synced with the "real" DOM. It's a step that happens between the render function being called and the displaying of elements on the screen. This entire process is called reconciliation.

## 16. What is Reconciliation?
Reconciliation is the process by which React updates the UI to reflect changes in the component state. The algorithm uses two main techniques to optimize updates:

Diffing: React compares the current virtual DOM tree with the updated virtual DOM tree, and identifies the minimum number of changes necessary to bring the virtual DOM in line with the updated state. This work is done by diffing algorithm.

Batching: React batches multiple changes into a single update, reducing the number of updates to the virtual DOM and, in turn, the real DOM.

The reconciliation algorithm is a critical part of React’s performance and helps make React one of the fastest and most efficient JavaScript libraries for building user interfaces.

## 17. How Virtual DOM works?
The Virtual DOM works in three simple steps.

* Whenever any underlying data changes, the entire UI is re-rendered in Virtual DOM representation.
![plot](./images/vdom1.png)
* Then the difference between the previous DOM representation and the new one is calculated.
![plot](./images/vdom2.png)
* Once the calculations are done, the real DOM will be updated with only the things that have actually changed. <br/>
![plot](./images/vdom3.png)

## 18. What is the difference between Shadow DOM and Virtual DOM?
The Shadow DOM is a browser technology designed primarily for scoping variables and CSS in web components. The Virtual DOM is a concept implemented by libraries in JavaScript on top of browser APIs.

## 19. What is the difference between createElement and cloneElement?
JSX elements will be transpiled to React.createElement() functions to create React elements which are going to be used for the object representation of UI. Whereas cloneElement is used to clone an element and pass it new props.

## 20. What are the different phases of component lifecycle?
The component lifecycle has three distinct lifecycle phases:

* Mounting: The component is ready to mount in the browser DOM. This phase covers initialization from constructor(), getDerivedStateFromProps(), render(), and componentDidMount() lifecycle methods.

* Updating: In this phase, the component gets updated in two ways, sending the new props and updating the state either from setState() or forceUpdate(). This phase covers getDerivedStateFromProps(), shouldComponentUpdate(), render(), getSnapshotBeforeUpdate() and componentDidUpdate() lifecycle methods.

* Unmounting: In this last phase, the component is not needed and gets unmounted from the browser DOM. This phase includes componentWillUnmount() lifecycle method.

## 21. What is context?
Context provides a way to pass data through the component tree without having to pass props down manually at every level.

For example, authenticated users, locale preferences, UI themes need to be accessed in the application by many components.
```javascript
const { Provider, Consumer } = React.createContext(defaultValue);
```

## 22. What is children prop?
Children is a prop that allows you to pass components as data to other components, just like any other prop you use. Component tree put between component's opening and closing tag will be passed to that component as children prop.
```jsx
const MenuCategory = ({ children }) => {
  const {items, img, title, subTitle, btnText} = children;
  return (
    <div className="my-10">
      {title && <Cover img={img} title={title} subTitle={subTitle}></Cover>}
      <div className="grid md:grid-cols-2 gap-8 my-10">
        {items.map((item) => (
          <MenuItem key={item._id} item={item}></MenuItem>
        ))}
      </div>
      <Link to={`/order/${title}`}><MenuButton text={btnText}></MenuButton></Link>
    </div>
  );
};
```

## 23. How to write comments in React?
The comments in React/JSX are similar to JavaScript Multiline comments but are wrapped in curly braces.

Single-line comments:
```jsx
<div>
  {/* Single-line comments(In vanilla JavaScript, the single-line comments are represented by double slash(//)) */}
  {`Welcome ${user}, let's play React`}
</div>
```
Multi-line comments:
```jsx
<div>
  {/* Multi-line comments for more than
   one line */}
  {`Welcome ${user}, let's play React`}
</div>
```

## 24. What is reconciliation?
Reconciliation is the process through which React updates the Browser DOM and makes React work faster. React use a diffing algorithm so that component updates are predictable and faster. React would first calculate the difference between the real DOM and the copy of DOM (Virtual DOM) when there's an update of components. React stores a copy of Browser DOM which is called Virtual DOM. When we make changes or add data, React creates a new Virtual DOM and compares it with the previous one. This comparison is done by Diffing Algorithm. Now React compares the Virtual DOM with Real DOM. It finds out the changed nodes and updates only the changed nodes in Real DOM leaving the rest nodes as it is. This process is called Reconciliation.

## 25. Why React uses className over class attribute?
The attribute class is a keyword in JavaScript, and JSX is an extension of JavaScript. That's the principal reason why React uses className instead of class. Pass a string as the className prop.

## 26. What are fragments?
It's a common pattern or practice in React for a component to return multiple elements. Fragments let you group a list of children without adding extra nodes to the DOM. You need to use either or a shorter syntax having empty tag (<></>).

## 27. Why fragments are better than container divs?
Below are the list of reasons to prefer fragments over container DOM elements,

* Fragments are a bit faster and use less memory by not creating an extra DOM node. This only has a real benefit on very large and deep trees.
* Some CSS mechanisms like Flexbox and CSS Grid have a special parent-child relationships, and adding divs in the middle makes it hard to keep the desired layout.
* The DOM Inspector is less cluttered.

## 28. What are stateless components?
If the behaviour of a component is independent of its state then it can be a stateless component. You can use either a function or a class for creating stateless components. But unless you need to use a lifecycle hook in your components, you should go for function components. There are a lot of benefits if you decide to use function components here; they are easy to write, understand, and test, a little faster, and you can avoid the this keyword altogether.

## 29. What are stateful components?
If the behavior of a component is dependent on the state of the component then it can be termed as stateful component. These stateful components are either function components with hooks or class components.

## 30. What are the advantages of React?
Below are the list of main advantages of React,

* Increases the application's performance with Virtual DOM.
* JSX makes code easy to read and write.
* It renders both on client and server side (SSR).
* Easy to integrate with frameworks (Angular, Backbone) since it is only a view library.
* Easy to write unit and integration tests with tools such as Jest.
