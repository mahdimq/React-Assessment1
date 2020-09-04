### Conceptual Exercise

Answer the following questions below:

- What is React? When and why would you use it?
  React is a powerful Front End library developed by Facebook. It makes small encapsulated components that contain HTML, CSS and JS that can be resuable and manage their own state.

- What is Babel?
  Babel is a toolchain mainly used to convert the new ECMAScript 2015 or later into older JavaScript, making the code backward compatible for older browsers and environments.

- What is JSX?
  JSX is an HTML-like syntax used by React that extends ECMAScript and processed by Babel to be backward compatible. This allows users to write concise HTML/XML like code inside React/JavaScript.

- How is a Component created in React?
  Components are created like JavaScript functions or classes. Components accept inputs or properties called "props" and return React elements describing what should render on the DOM.

- What are some difference between state and props?
  Props are variables passed to its parent by components. Props are immutable and should never be changed in a child component. State is also a variable but directly initialized and managed by the components itself. State is mutable.

* What does "downward data flow" refer to in React?
  Downward data flow means that the direction of the flow of data is from PARENT to CHILD, and not the other way around. This is so that an object can be changed without effect to its parent data by simple state modifications.

* What is a controlled component?
  A controlled component or a "dumb component" is one that takes its current value through props, and notifies changes through callbacks (onChange for a form). A parent component controls the component by handling the callback and managing it's own state and so passes down the new values to the controlled component as props. A form input is a controlled component.

* What is an uncontrolled component?
  An uncontrolled component is one that stores and manages it's own state internally. Uncontrolled components are like traditional HTML where a DOM query is made using a "ref" (useRef) in React.

* What is the purpose of the `key` prop when rendering a list of components?
  Key prop allows React to keep track or identify which items in the array have changed, added or have been removed. This prop has to be unique.

* Why is using an array index a poor choice for a `key` prop when rendering a list of components?
  Using an array index as a "key" is a poor choice because the order of the items may change. This can impact the performance and may cause issues with the components state. If a unique key is not passed in as a key, React cannot differentiate if the items were changed or removed/added.

* Describe useEffect. What use cases is it used for in React components?
  useEffect in React adds the ability to perform side effects from a function conponent. It allows the component to do something "after" it has rendered for the first time. React remembers the function passed in (the "effect") and calls it later after the DOM has updated.

* What does useRef do? Does a change to a ref value cause a rerender of a component?
  useRef is a function that returns a mutable "ref" object. This object has a .current property that does not change throughout the component's lifetime. A change is ref value does not cause a rerender of a component.

* When would you use a ref? When wouldn't you use one?
  UseRefs are used to access DOM nodes or React elements or storing a mutable variable. Refs cannot be used to change state, since they do not cause a re-render cycle.

* What is a custom hook in React? When would you want to write one?
  Custom Hooks lets the user extract component logic into a resuable function. Hooks generally have names that start with "use.." and can call other Hooks like useState or useEffect. We would write a custom Hook if we notice we're repeating a common Hook between multiple components.
