<details>
<summary>
    <h3>1. How does React work?</h3>
</summary>

React creates a virtual DOM. When the state changes in a component it first runs a "diffing" algorithm, which identifies what has changed in the virtual DOM. The second step is reconciliation, where it updates the DOM with the results of diff.

</details>


# 1. How does `React` work?
### React creates a virtual DOM. When the state changes in a component it first runs a "diffing" algorithm, which identifies what has changed in the virtual DOM

>Let’s say one of your friends posted a photograph on Facebook. Now you go and like the image and then you started checking out the comments too. Now while you are browsing over comments you see that the likes count has increased by 100, since you liked the picture, even without reloading the page. This magical count change is because of ReactJS.
 
 - React is not a framework. It is just a library developed by Facebook to solve some problems that we were facing earlier.

### While building client-side apps, a team of Facebook developers realized that the DOM is slow So, to make it faster, React implements a virtual DOM that is basically a DOM tree representation in JavaScript. So when it needs to read or write to the DOM, it will use the virtual representation of it. Then the virtual DOM will try to find the most efficient way to update the browser’s DOM.


# 2. What are the advantages of using `React`?

> React.js is one of the most popular front-end JavaScript libraries for building Web applications.

  `advantages`:
- Write once, and learn anywhere.
- It is simple: The component-based approach, automatic rendering, and use of just plain JavaScript make React very simple to learn, build a web (and mobile applications), and support it. We can mix Javascript and HTML together to create a special syntax called JSX which makes it easier to grasp and work with it.

- SEO friendly: SEO is about making it easier for developers to find the right content for the user. When a user makes a search, search engines platforms like Google, Yahoo, Bing or Baidu try to find which page is the most relevant to that specific search. React affects the SEO by giving you a SPA (Single Page Application) which requires Javascript to show the content on the page which can then be rendered and indexed.
- Fast, efficient, and easy to learn.

## 3. What is the difference between a `Presentational` component and a `Container` component?
 > In react the components are divided into two categories: presentational components and container components.

### Presentational components
 - Mainly concerned with how things look.
- Have no major dependencies on the rest of the app.
- No connection with the specification of the data that is outside the component.
- Mainly receives data and callbacks exclusively via props.

### Container components

- Mainly concerned with how things work.
- Provide the data and behaviour to presentational or other container components.


## 4. What are the differences between a `class` component and `functional` component?
### functional component :-
- A functional component is just a plain JavaScript pure function that accepts props as an argument and returns a React element(JSX).
- There is no render method used in functional components.
- Functional component run from top to bottom and once the function is returned it cant be kept alive.
- Also known as Stateless components as they simply accept data and display them in some form,
- React lifecycle methods cannot be used in functional components.
- Hooks can be easily used in functional components to make them Stateful.
- Constructors are not used.

### class component : -
- A class component requires you to extend from React.
- It must have the render() method returning JSX
- Also known as Stateful components because they implement logic and state.
- React lifecycle methods can be used inside class components
- Constructor are used as it needs to store state. 

## 5. What is the difference between `state` and `props`?
### PROPS :-
- The Data is passed from one component to another.
- It is Immutable (cannot be modified).
- Props can be used with state and functional components.	
- Props are read-only.

### STATES :-
- The state represents parts of an Application that can change.
 - Each component can have its State.
- It is Mutable ( can be modified).
- State can be used only with the state components/class component.
- State is both read and write.


## 6. What are the different `lifecycle methods`?

> `componentWillMount` (deprecated) - this is most commonly used for App configuration in your root component.



> `componentDidMount` - here you want to do all the setup you couldn’t do without a DOM, and start getting all the data you need. Also if you want to set up eventListeners etc. this lifecycle hook is a good place to do that.


> `componentWillReceiveProps` (deprecated) - this lifecyclye acts on particular prop changes to trigger state transitions.


> `shouldComponentUpdate` - if you’re worried about wasted renders shouldComponentUpdate is a great place to improve performance as it allows you to prevent a rerender if component receives new prop. shouldComponentUpdate should always return a boolean and based on what this is will determine if the component is rerendered or not.


> `componentWillUpdate` (deprecated) - rarely used. It can be used instead of componentWillReceiveProps on a component that also has shouldComponentUpdate (but no access to previous props).


> `componentDidUpdate` - also commonly used to update the DOM in response to prop or state changes.


> `componentWillUnmount` - enables you can cancel any outgoing network requests, or remove all event listeners associated with the component.




## 7. Explain `React Hooks`.
 ### React Hooks are simple JavaScript functions that we can use to isolate the reusable part from a functional component. Hooks can be stateful and can manage side-effects.

> `useState`: To manage states. Returns a stateful value and an updater function to update it.

> `useEffect`: To manage side-effects like API calls, subscriptions, timers, mutations, and more.

> `useContext`: To return the current value for a context.

> `useReducer`: A useState alternative to help with complex state management.

> `useCallback`: It returns a memorized version of a callback to help a child component not re-render unnecessarily.

> `useMemo`: It returns a memoized value that helps in performance optimizations.

> `useRef`: It returns a ref object with a .current property. The ref object is mutable. It is mainly used to access a child component imperatively.

> `useLayoutEffect`: It fires at the end of all DOM mutations. It's best to use useEffect as much as possible over this one as the useLayoutEffect fires synchronously.

> `useDebugValue`: Helps to display a label in React DevTools for custom hooks.`


## 8. Where in a React class component should you make an AJAX/API request?
### componentDidMount is where an AJAX request should be made in a React component. This method will be executed when the component mounts (is added to the DOM) for the first time. This method is only executed once during the component’s life.

#### AJAX requests should be made after the component has been rendered to the browser, and usually, they need to be made only once. Thus, the best place to make the requests is inside an useEffect hook.

## 9. What are `controlled` components?
- In a controlled component, form data is handled by a React component. 
- In React, Controlled Components are those in which form’s data is handled by the component’s state. 
- It takes its current value through props and makes changes through callbacks like onClick,onChange, etc
> The alternative is uncontrolled components, where form data is handled by the DOM itself. 


10. What are refs used for in React?
- Refs are a function provided by React to access the DOM element and the React element that you might have created on your own.
-  They are used in cases where we want to change the value of a child component, without making use of props and all. 
- They also provide us with good functionality as we can use callbacks with them.  

### We can create a Ref by the following three methods:

- Using React.createRef()
- Using useRef() hook
- Using callback ref


## 11. What is a `higher order component`?
- Higher-order components or HOC is the advanced method of reusing the component functionality logic. 
- It simply takes the original component and returns the enhanced component.
- Easy to handle
- Makes code more readable

## 12. What advantages are there in using `arrow functions`?
- This arrow function reduces lots of code and makes the code more readable.
- Writing the arrow => is more flexible as compared with the writing function keyword.
- Arrow functions have shorter syntax than regular function expressions.
- Arrow functions have implicit return statements.
- Arrow functions increase readability.
