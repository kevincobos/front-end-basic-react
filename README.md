# Front End - Basic React
## Table of Contents
- [Introduction](#introduction)  
- [React](#react)
- [Starting to use React on my projects](#starting-to-use-react-on-my-projects)   
- [Create a new react-app using](#create-a-new-react-app-using)
- [Additional packages to consider installing](#additional-packages-to-consider-installing)
- [Principles of React Components](#principles-of-react-components)
- [React Components](#react-components)
- [Importing components](#importing-components)
- [React Props](#react-props)
- [JavaScript Expressions in JSX](#javascript-expressions-in-jsx)
- [Fragments](#fragments)
- [CSS Styling](#css-styling)
- [Arrow Functions on React](#arrow-functions-on-react)
- [Expressions as Props](#expressions-as-props)
- [Enbeded Atributes](#enbeded-atributes)
- [If Statements and For Loops inside JSX](#if-statements-and-for-loops-inside-jsx)
- [React evets and event handlers](#react-evets-and-event-handlers)
- [React Hooks](#react-hooks)
- [Destructure Name Convention](#destructure-name-convention)
- [useState Hook](#usestate-hook)
- [useEffect Hook](#useeffect-hook)
- [useContext Hook](#usecontext-hook)
- [useReducer Hook](#usereducer-hook)
- [useRef Hook](#useref-hook)
- [Data Fetching with React Hooks](#data-fetching-with-react-hooks)
- [Parent Child Data Flow](#parent-child-data-flow)
- [React State Management](#react-state-management)
- [Context API](#context-api)
- [useReducer Hook](#usereducer-hook)
- [useRef Hook](#useref-hook)
- [Data Fetching with React Hooks](#data-fetching-with-react-hooks)
- [Adding Images](#adding-images)
- [Adding Videos](#adding-videos)
- [Navigation](#navigation)
- [React Router](#react-router)
- [Markdown Language](#markdown-language)


- [Miscellaneous](#miscellaneous)
- [Disclaimer](#disclaimer)
- [References](#references)

## Introduction
### Why I'm writing this document?
I'm writing this document to help me remember somne basic concepts of React. The main idea is to keep adding more examples and code snippets for later reference as I learn more about the tools related to this technology.


## React
React is a JavaScript library for building user interfaces. It is maintained by Facebook and a community of individual developers and companies.    
-  React can be used with a combination of other JavaScript libraries or frameworks, such as Angular JS in MVC.   
- React is not a framework, nor is it a complete solution. It is a library for building composable user interfaces. It encourages the creation of reusable UI components, which present data that changes over time. Lots of people use React as the V in MVC.   
- React abstracts away the DOM from you, giving a simpler programming model and better performance. React can also render on the server using Node, and it can power native apps using React Native.   
- React implements one-way reactive data flow, which reduces the boilerplate and is easier to reason about than traditional data binding.   
- React uses JSX - an XML-like syntax that allows you to write React components in a familiar way.     
- React is scalable - large applications with data that changes over time without reloading the page is where React performs best. 

### React Main Features
- JavaScript library for building user interfaces.
- Tool for building SPAs (Single Page Applications).
- Tool for handling the view layer for web and mobile apps.
- Tool for building fast and scalable front-end applications.
- Tool for building UI components that can be used on their own or combined with other components to build complex UIs.

SPA's are web applications that load a single HTML page and dynamically update that page as the user interacts with the app. SPAs use AJAX and HTML5 to create fluid and responsive web apps, without constant page reloads. However, this means much of the work happens on the client side, in JavaScript.  
React allows developers to build SPAs.

React JSX, JSX stands for JavaScript XML. JSX allows us to write HTML in React. JSX makes it easier to write and add HTML in React. JSX converts HTML tags into react elements. JSX is an extension to the JavaScript language based on ES6, but it is not required to use it. JSX is not a necessity to write React applications. JSX is a syntax extension to JavaScript. You can definitely use React without JSX but JSX makes React a lot more elegant. Just like XML, JSX tags have a tag name, attributes, and children. If an attribute value is enclosed in quotes, the value is a string. Otherwise, wrap the value in braces and the value is the enclosed JavaScript expression.

## Starting to use React on my projects   
   
### First install React using:   
```CLI 
npx create-react-app "name of the app"
``` 
  
Updating your build tooling is typically a daunting and time-consuming task. When new versions of Create React App are released, you can upgrade using a single command:   
```CLI 
npm install react-scripts@latest
```  

## Create a new react-app using:
```npm init react-app "App name"``` <samp> or </samp> ```npx create-react-app .``` <samp> where "." means the current directory. </samp> 
### Run the new app using:
If diferent directory then use ```cd  "app name"```   
Then ```npm start```   

### Additional packages to consider installing
<b>React-Botstrap</b> is a library with a complete re-implementation of Bootstrap components using React. It has no dependency on either bootstrap.js or jQuery. If you have React setup and React-Bootstrap installed you have everything you need. 
```CLI 
npm install react-bootstrap bootstrap
```   
<b>React Icons</b> include popular icons in your React projects easily with react-icons, which utilizes ES6 imports that allows you to include only the icons that your project is using.  
```CLI 
npm install react-icons --save
```    
# Principles of React Components 
## React Components
Components are independent and reusable bits of code. They serve the same purpose as JavaScript functions, but work in isolation and returns HTML via a render function.   
Components come in two types, Class components and Function components.   
Functional components are reusable blocks of code that act like a JavaScript function and you can pass data from one component to another using props.   
Data flow is one-directional which means that a parent component can send the same data to one or more child components, but it's not possible to communicate from the child components back to the parent component using props.    

React Components can be stateful or stateless.   
Example of a stateless component:
```javascript   
function App() {
  return (
    <div>
      <h1>This component is rendering text and also uses a variable {variable}</h1>
      <h1>this becomes a stateless component</h1>
    </div>
  )
}
```
Example of a stateful component: Bellow we can see a example 
```javascript
  function App() {
    return (
      <h1>
        This text is not going to change, so this is a exaple of a stateless component.
      </h1>
    )
  }
```
Thanks to ES6 Array Destructuring, we can use props as a parameter and then use the individual props as variables.   
Example of array destructuring:   
```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];   

const fruits = ["Banana", "Orange", "Apple", "Mango"];
const [first, second, third, fourth] = fruits;
```

## Create a React Component
A React component is a function or a class which optionally accepts input and returns a React element (typically via JSX which gets compiled to a createElement invocation).

![React Function](https://github.com/kevincobos/front-end-basic-react/blob/main/img/functionComponent.png?raw=true);   

## Importing components
- Build a new file by right-clicking on the src folder, then in the right-click contextual menu that appears, clicking on the New File command. Name the file "HelloWorld.js".   

- Once you've typed HelloWorld.js, press the ENTER key to finish the process of naming the file. Upon pressing the ENTER key, your new, empty HelloWorld.js file will be shown, ready to be edited and updated with some code.

- Import the HelloWorld component into the App component.   
Add this at the end of the file that you are exporting   
  <samp> export default HelloWorld; </samp>   
Add this to inporting file    
<samp> import HelloWorld from "./HelloWorld"; </samp>    

![React Function](https://github.com/kevincobos/front-end-basic-react/blob/main/img/newComponent.png?raw=true);

For a component to render something on the page, it needs to return it as one or more JSX elements.

## React Props
Props are arguments passed into React components. Props are passed to components via HTML attributes.  
Props can be used to pass data, or functions, from one component to another.  
   
This is how you pass data from one component to another as an attribute:
![React Props Code](https://github.com/kevincobos/front-end-basic-react/blob/main/img/propsComponentsCode.png?raw=true)    

The Browser Render:
![React Props Browser Render](https://github.com/kevincobos/front-end-basic-react/blob/main/img/propsComponents.png?raw=true?width=auto&height=auto)   

### JavaScript Expressions in JSX
You can write any JavaScript expression inside the curly braces in JSX. Each React element is a JavaScript object that you can store in a variable or pass around in your program. You can use an if statement in the curly braces to show or hide an element. You can also use the **ternary operator** condition ? true : false to show something. You can also use JavaScript expressions to embed a map() call in JSX. You can also use JavaScript expressions to embed a function call in JSX.   

The following JavaScript code ```{'abc'+'def'}``` will render this <samp> abcdef </samp>   
The following JavaScript code ```{2+3}``` will render this <samp> 5 </samp>   
The following JavaScript code ```{2===3}``` will render this <samp> false </samp>   

### Ternary Operators 
The ternary operator is the only JavaScript operator that takes three operands. This operator is frequently used as a shortcut for the if statement.

### Ternary Operator on React:   
The ternary operator is a simplified conditional operator like if / else.   
**Syntax:** condition ? \<expression if true\> : \<expression if false\>    
  
  ```javascript
  //condition ? exprIfTrue : exprIfFalse
  // Example
  function getFee(isMember) {
    return (isMember ? '$2.00' : '$10.00');
  }

  console.log(getFee(true));
  // expected output: "$2.00"
  ```
### Fragments
A common pattern in React is for a component to return multiple elements. Fragments <code> <></> </code> let you group a list of children without adding extra nodes to the DOM.

Example of a fragment:
```javascript
return(<> content here </>);
```   
   
### note:   
don't forget we can't use class in react, we have to use className.   
```className``` is used to specify the class name of an element, and it is used by the browsers to apply CSS rules to elements.   
Html <code> class=" " </code>   
JSX <code> className=" " </code> 

![Example of use of className](https://github.com/kevincobos/front-end-basic-react/blob/main/img/using-className.png?raw=true)

### CSS Styling
React does not have a built-in way to style components, but there are several libraries that allow us to use CSS in React.   

Using React, you can easily convert a CSS rule to a JavaScript object, where each key-value pair describes a CSS declaration.   

### Arrow Functions on React

Arrow functions are a new way to write anonymous function expressions in JavaScript. They have a shorter syntax than function expressions. Arrow functions do not have their own this. They are not well suited for defining object methods. Arrow functions are not hoisted. They must be defined before they are used.   
Using const is safer than using var, because a function expression is always constant value. You can only omit the return keyword and the curly brackets if the function is a single statement. Because of this, it might be a good habit to always keep them:   

Regular function declaration:   
```javascript
function XFunction(props) {
    return (
        <ul>
            <li>{props.first}</li>
        </ul>
    )
};
```
Regular function expression:   
```javascript
const XFunction = function(props) {
    return (
        <ul>
            <li>{props.first}</li>
        </ul>
    )
};
```
Arrow function expressions:   

```javascript
const XFunction = (props) => { return (
    <ul>
        <li>{props.first}</li>
    </ul>
  )
};
```    
or   
```javascript
const XFunction = props => { return (
    <ul>
        <li>{props.first}</li>
    </ul>
  )
};
```

### Expressions as Props
You can pass any JavaScript expression as a prop, by surrounding it with curly braces.   
Example:   
```javascript
function App() {
  return (
    <div>
      <Header username="Kevin" />
      <Greeting />
    </div>
  )
}
```

### Enbeded Atributes
You can embed JavaScript expressions in your JSX by wrapping them in curly braces.    
Example:   
```javascript
function App() {
  const date = new Date()
  const hours = date.getHours()
  let timeOfDay
  
  if (hours < 12) {
    timeOfDay = "morning"
  } else if (hours >= 12 && hours < 17) {
    timeOfDay = "afternoon"
  } else {
    timeOfDay = "night"
  }
  
  return (
    <h1>Good {timeOfDay}!</h1>
  )
}
```   

### If Statements and For Loops inside JSX
You can use an if statement in the curly braces to show or hide an element. You can also use the ternary operator condition ? true : false to show something. You can also use JavaScript expressions to embed a map() call in JSX. You can also use JavaScript expressions to embed a function call in JSX.   

Example of a ternary operator:     
```javascript
//regular if statement: 
{
  if (name === "Kevin"){
    return "Yes, it is Kevin"
  } else {
    return "I don't know this person"
  }
}
```   
Ternary operator:
```javascript
//Using ternary operator
{
  name === "Kevin" ? "Yes, it is Kevin" : "I don't know this person"
}
```
Applying conditional rendering using the ternary operator
```javascript
function App() {
  const date = new Date()
  const hours = date.getHours() 
  
  return (
    {hours >= 12 && hours < 17
      ? <Daytime />  
      : <Nighttime /> 
    }
  )
}
```
Code bellow show something that is posible too using (logical && operator)
```javascript
let renderLine = true;

false && console.log('This will never show');
true && console.log('This will always show');
renderLine && console.log('This will always show');
```
Conditional Component Rendering
```javascript
//Depending on what the value of isLoggedIn is, either the LoginButton or the LogoutButton component will be rendered.
function LogInOutButton(props) {
  const isLoggedIn = props.isLoggedIn;
    if (isLoggedIn) {
      return <LogoutButton />;
    } else {
    return <LoginButton />;
  }
}
```

### React evets and event handlers
React events are written in camelCase syntax: onClick instead of onclick. React event handlers are written inside curly braces: onClick={shoot} instead of onClick="shoot()". React event handlers are passed with an event object argument: onClick={(event) => this.shoot(event)}. Arrow functions allow you to pass arguments to event handlers: onClick={() => this.shoot("Goal")}.   

In React, the rule is to avoid manipulating the DOM directly as much as possible. Instead, setup everything declaratively, meaning that you describe updates to React and let it figure out the rest. React uses a virtual DOM to manage the state of the actual DOM. React only updates the necessary parts of the DOM when a component's state changes. This makes React fast.
Remember not to invoke a function when passing it as a prop.  
For example, this will not work: <code>onClick={shoot()}</code>   
It should be: <code>onClick={shoot}</code> The problem with this is that it will call the shoot function immediately when the component renders, and shoot the football every time the component re-renders. Instead, we want to pass the function itself, without running it.

Example of a event handler:   
``` javascript
<button onClick={shoot}>Take the shot!</button> 
```    

Example of a event handler with arguments:   
``` javascript
<button onClick={() => this.shoot("Goal")}>Take the shot!</button> 
```   

Handling events using inline anonymous ES5 functions:    
```javascript
<button onClick={function() { console.log('example') }}>
  Click me
</button>
```
Handling events using inline anonymous ES6 arrow functions:   
``` javascript
<button onClick={() => console.log('example')}>
  Click me
</button>
```
Handling events using class methods:   
```javascript
class LoggingButton extends React.Component {
  handleClick() { console.log('this is:', this);}

  render() {
    // This syntax ensures `this` is bound within handleClick
    return (
      <button onClick={() => console.log('example')}>
        Click me
      </button>
    );
  }
}
```
Handling events using class fields:   
```javascript 
class LoggingButton extends React.Component { 
  // This syntax ensures `this` is bound within handleClick.
  // Warning: this is *experimental* syntax.
  handleClick = () => {
    console.log('this is:', this);
  }

  render() {
    return (
      <button onClick={this.handleClick}>
        Click me
      </button>
    );
  }
}
```

Handaling events using separate functions:   
```javascript
function App() {
  function shoot() {
    alert("Great Shot!");
  }
  return (
    <button onClick={shoot}>Take the shot!</button>
  );
}
```

Handaling events using separate functions with arguments:   
```javascript
function App() {
  function shoot(player, distance) {
    alert(player + " kicked the ball " + distance + " meters")
  }
  return (
    <button onClick={shoot.bind(this, "Kevin", 45)}>Take the shot!</button>
  );
}
```

Handaling events using separate functions expressions:   
```javascript
function App() {
  const shoot = () => {
    alert("Great Shot!");
  }
  return (
    <button onClick={shoot}>Take the shot!</button>
  );
}
```

Handaling events using separate functions expressions with arguments:   
```javascript
function App() {
  const shoot = (player, distance) => {
    alert(player + " kicked the ball " + distance + " meters")
}
  return (<button onClick={() => shoot("Kevin", 45)}>Take the shot!</button>);
}
```

### React Hooks
Hooks are a new addition in React 16.8. Hooks are functions that let you “hook into” React state and lifecycle features from function components.   
Hooks don’t work inside classes — they let you use React without classes.   
Hooks provide access to imperative escape hatches and don’t require you to learn complex functional or reactive programming techniques.   
Hooks let you always use functions instead of having to constantly switch between functions, classes, higher-order components, and render props.   
Hooks let you reuse stateful logic without changing your component hierarchy.   
React Hooks can be call only from the top level of a function component and only from React functions.   
React Hooks can not be call from a regular function or a class component.

#### Things to know about React Hooks:
Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions.  
We can call Hooks from React function components and not just any regular JavaScript function.
We can make multiple calls to state or effect hooks.



### Destructure Name Convention
If the count is the name of the variable the convention is to use the same name for the function that updates the variable, the only difference is that the function name starts with the word set.
```javascript
// Count is the name of the variable
// setCount is the name of the function that updates the variable
import React, { useState } from "react" 
const [count, setCount] = useState(0);
```  

### useState Hook   
The useState hook is use on less complex data.
The useState hook is a special function that takes the initial state as an argument and returns an array of two entries. The first entry is the current state and the second entry is a function that allows us to update the state.   
Example of correct use of useState Hook, that is using the stateUpdate function:
``` javascript
import React, { useState } from "react" 

funtion App() {
  // count is the current state, we use this to access the current state   
  //setCount is the function that allows us to update the state   
  const [count, setCount] = useState(0);
  return (
    <div>
      <h1>{count}</h1>
      <button onClick={() => setCount(count + 1)}>Change!</button>
    </div>
  )
}
```   
#### Updating a stete Object the correct way
The sujested way to update a state object is to use the spread operator.  
**( ... )** is the spread operator. It takes all the properties of the object and copies them into the new object.

```javascript
import { useState } from "react"; 
 
export default function App() { 
  const [mainObject, setMainObject] = useState({ 
    message: "Original object" 
    place: "World"
    activated: true,
  }); 
  console.log(mainObject, setMainObject); 
 
  function updateMainObject() { 
    const tempMainObject = {...mainObject};            // <-- Spread operator
    tempMainObject.message = "Original object and updated"; 
    setMainObject(tempMainObject); 
  } 

  function updateMainObjectArroFunc() { 
    setGreeting(tempState => { 
      return {...tempState, 
        place: "Under world"
        activated: false,
      } 
    }); 
  } 
 
  return ( 
    <div> 
      <h1>{mainObject.message}</h1> 
      <h1>{mainObject.place}</h1>
      <button onClick={updateMainObject}>Update object</button> 
      {
        mainObject.activated && <button onClick={updateMainObjectArroFunc}>
          Hidding button
        </button> 
      }
    </div> 
  ); 
} 
```
### Pure and Impure Functions in React
A pure function is a function that **does not cause side effects**. A pure function is a function that does not modify the values passed to it.   
Impure functions are functions that **have side effects**. A side effect is any change in the state of the program that can be observed outside the function itself.   
For example, invoking console.log, fetch, geolocation or a function that modifies a global variable would be considered impure because it changes the state of the program outside of its own scope.  
Example of pure and impure functions:

```JavaScript
// This is a pure function
function sum(a, b) {
  return a + b;
}

// This is a impure function
function sum(a, b) {
  return a + b + Math.random();
}

```

### useEffect Hook   
The useEffect hook is a special function that takes a function as an argument. The function that we pass to the useEffect hook will run after every render of the component.   
The useEffect hook is similar to the componentDidMount and componentDidUpdate lifecycle methods in React class components.  
The useEffect hook can be used to perform side effects in function components, fetch data from a server, set up event listeners, perform cleanup, update the document title, perform **side effects** in function components, fetch data from a server, set up event listeners, perform cleanup, update the document title, etc.   
Example of useEffect Hook:   
```javascript
import React, { useState, useEffect } from "react" 
function ShoppingCart(){
  const total prop.count * prop.price;

  // useEffect hook takes a function as an argument and a array, we can leave the
  // array empty if we want the function to run after every render of the component.
  useEffect(() => {
    document.title = `Total: ${total}`,[];
  });

  // Not using this empty array may cause performance issues, especially if your 
  // side effects are computationally intensive. 
  useEffect(() => {
    console.log(`Total: ${total}`),[];
  });
}
```
React does not limit us to use the useEffect hook only once. We can use the useEffect hook as many times as we want.


### useContext Hook   
The useContext hook is a special function that takes a context object as an argument and returns the current context value for that context.
Example of useContext Hook:   
```javascript
import React, { useContext } from "react" 
```
### useReducer Hook   
The useReducer hook is best used on more complex data, specifically, arrays or objects.
The useReducer hook is a special function that takes a reducer function and an initial state as arguments and returns an array of two entries. The first entry is the current state and the second entry is a dispatch function that allows us to update the state.   

Example of useReducer Hook:   
```javascript
import React, { useReducer } from "react" 

function App() {
  const [count, dispatch] = useReducer((state, action) => {
    switch (action.type) {
      case "add":
        return state + 1;
      case "minus":
        return state - 1;
      case "reset":
        return 0;
      default:
        return state;
    }
  }, 0);
  return (
    <div>
      <h1>{count}</h1>
      <button onClick={() => dispatch({ type: "add" })}>Add!</button>
      <button onClick={() => dispatch({ type: "minus" })}>Minus!</button>
      <button onClick={() => dispatch({ type: "reset" })}>Reset!</button>
    </div>
  );
}
```

```javascript


```

### useRef Hook   
The useRef hook can be used to access the DOM nodes or React elements, focus an input field, measure the size or position of a DOM node, etc.  

Example of useRef Hook:   

```javascript
import React, { useRef } from "react" 

function App() {
  const inputRef = useRef();
  return (
    <div>
      <input ref={inputRef} type="text" />
      <button onClick={() => inputRef.current.focus()}>Focus!</button>
    </div>
  );
}
```
### Data Fetching with React Hooks
The useEffect hook can be used to fetch data from a server, set up event listeners, perform cleanup, update the document title, etc.   

Keep in mind when working with React, fetching data from a third-party API is considered a side-effect, we need to use the useEffect hook to deal with using the Fetch API calls in React.   

```javascript
import { useState, useEffect } from "react"; 
 
export default function App() { 
  const [comingData, setComingData] = useState({}); 
  useEffect(() => { 
    fetch(`https://api.website.com/datasheet.json`) 
      .then((response) => response.json()) 
      .then((jsonData) => setComingData(jsonData.value)) 
      .catch((error) => console.log(error)); 
  }, []); 
 
  return Object.keys(comingData).length > 0 ?( 
    <> 
      <h1>Coming Data</h1> 
      <p>Code: {comingData.code}</p> 
      <p>Symbol: {comingData.symbol}</p> 
      <p>Rate: {comingData.rate}</p> 
      <p>Description: {comingData.description}</p> 
      <p>Rate Float: {comingData.rate_float}</p> 
    </> 
  ):(
    <h1>Downloading...</h1>
  );
} 
```
### Custom Hooks
A custom hook is simply a way to extract a piece of functionality that we can use again and again, whith custom hooks we can create a reusable, reliable and streamlined piece of functionality in our React apps.

```JavaScript

// Creating a custom hook
function useFetch(url) {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);

  useEffect(() => {
    fetch(url)
      .then((response) => response.json())
      .then((data) => {
        setData(data);
        setLoading(false);
      })
      .catch((error) => {
        setError(error);
        setLoading(false);
      });
  }, [url]);

  return { data, loading, error };
  export default useFetch;
}

// Using the custom hook
function App() {
  const { data, loading, error } = useFetch(
    "https://api.website.com/datasheet.json"
  );

  if (loading) return <h1>Loading...</h1>;
  if (error) return <h1>Error!</h1>;

  return (
    <>
      <h1>Coming Data</h1>
      <p>Code: {data.code}</p>
      <p>Symbol: {data.symbol}</p>
      <p>Rate: {data.rate}</p>
      <p>Description: {data.description}</p>
      <p>Rate Float: {data.rate_float}</p>
    </>
  );
}
```

### JSX to an Element
React converts the JSX tree to an element tree where each node is a plane object describing a component instance and then to a DOM tree, which is then rendered to the page. 

Element tree  
![Element tree](./img/element-tree.png)

## Parent Child Data Flow   
### State Data
State is the place where the data comes from. We should always try to make our state as simple as possible and minimize the number of stateful components. If we have, for example, ten components that need data from the state, we should create one container component that will keep the state for all of them.

### Props Data
Props are how components talk to each other. They are passed down from a parent component to a child component. Props data is read-only, which means that data coming from the parent should not be changed by child components. Props are used to pass data, or functions, from one component to another. Data with props are being passed in a uni-directional flow. (one way from parent to child)

Example of parent child data flow:   
```javascript
funtion AppInformation(props) {
  return (
    <div>
      <Header username={props.username} />
      <Greeting age={props.age} />
    </div>
  )
}
const data = {
  name: "Kevin",
  age: 30
}
function App() {
  return (
    <div>
      <AppInformation 
        userName={data.name}
        age={data.age} 
      />
    </div>
  )
}
```
![Parent Child Data Flow](https://github.com/kevincobos/front-end-basic-react/blob/main/img/parentChildDataFlow.png?raw=true)

## React State Management
State management is the process of maintaining the state of a React app. Using APIs like setState(), useState(), useReducer(), useContext(), etc. we can manage the state of a React app, so an API provides a predefined way to manage the state of a React app.

### Context API
The Context API is a React API that allows us to manage the state of a React app. The Context API is a way to pass data through the component tree without having to pass props down manually at every level. 
Example of Context API:  

```javascript
import React from "react";
const MealContext = React.createContext();
const todayMeals = ["Beans", "Rice", "Meat"];

const MealProvider = ({children}) => {

  const [meals, setMealsList] = React.useState(todayMeals);

  return (
    <MealsContext.Provider value={{meals}}>
      {children}
    </MealsContext.Provider>
  );
};

export const useMealsListContex = () => React.useContext(MealsContext);
export default MealProvider;
```

```javascript
inport { useMealsListContex } from "../providers/MealContext";

const MealsList = () => {
  const { meals } = useMealsContext();
  return (
    <div>
      <h1>Meals List using Context API</h1>
        {meals.map((meal, index) => (
          <h2 key={index}>{meal}</h2>
        ))}
    </div>
  );
};
```

```javascript
import { useMealsListContex } from "./providers/MealContext";

const Counter = () => {
  const { meals } = useMealsListContex();

  return (
    <div>
      <h3> Number of meals today: {meals.length} </h3>
    </div>
  );
}
```
## Adding Images
```JavaScript
import example1 from "./assests/images/react.png";
function App() {
  return (
    <div>
      <img src={example1} alt="example1" />
    </div>
  );
}
```
```javascript
function App() {
  const example2 = "https://coboskevin.com/assests/images/react.png";
  return (
    <div>
      <img src={example2} alt="example2" />
    </div>
  );
}
```
```javascript
  return (
    <div>
      <img src={require("./assests/images/react.png")} alt="example3" />
    </div>
  );
```  

## Adding Videos
```javascript
import example1 from "./assests/videos/example1.mp4";
function App() {
  return (
    <div>
      <video width="320" height="240" controls>
        <source src={example1} type="video/mp4" />
      </video>
    </div>
  );
}
```
### Adding Video with React-Player "Third Party Library"
First install react-player using:   
```CLI
npm install react-player
```
Then import react-player using this code on the App.js file:   

```javascript
//React component for playing a variety of URLs, including file paths, YouTube, Facebook, Twitch, etc.
// Check the documentation for more info: https://www.npmjs.com/package/react-player
import ReactPlayer from "react-player";

// Line bellow is the same as the one above, the difference is that the code bellow reduce your bundle size
import ReactPlayer from 'react-player/youtube'

function App() {
  return (
    <div>
      <ReactPlayer url="https://www.youtube.com/watch?v=rNWaLeZ5TV0" />
    </div>
  );
}
```

## Navigation   
### React Router
What is react router?   
React router is a routing library built on top of the react which is used to create the routing in react apps.   
Main venefits of react router:
- It is used to create routes in the react app. 
- It maintains the mapping between the url and the components. 
- It keeps your UI in sync with the URL. 
- It is used to create the single page application. 
- It is used to create the navigation between the components. 
- It is used to create the multiple pages in the react app. 
- It is used to create the dynamic routing in the react app.  
- It has a simple API with powerful features like lazy code loading, dynamic route matching, and location transition handling built right in. 

### Installing React Router
```linux
npm install react-router-dom
```
![React Router](https://github.com/kevincobos/front-end-basic-react/blob/main/img/installing-react-router.png?raw=true)
### Usage
To use we need to add this to the index.js file
```javascript
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';
import reportWebVitals from './reportWebVitals';
// this line bellow is new
import { BrowserRouter } from 'react-router-dom'; 

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <BrowserRouter>  // this is the new line
      <App />
    </BrowserRouter> // this is the new line
  </React.StrictMode>
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();
```
On the App.js file we need to add this:
```javascript
/*Code*/
import {Routes, Route} from 'react-router-dom';

funtion App() {

  /*Code*/

  return (
    <div className="App">
      <nav className="nav">
        <Link to="/" className="nav-item">Home</Link>
        <Link to="/about" className="nav-item">About</Link>
      </nav>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
      </Routes>
    </div>
  );
}
```
## Layouts
Layouts are important because they provide a framework that site designers can use to structure a site's content. They also help designers and programmers work together more efficiently by providing a common language and a means of separating concerns. 
### Grid Layout
A grid layout is a way of structuring content on a website. It uses a grid of rows and columns to give order and structure to a website's content. Grid layouts can be used to arrange blog posts, products, testimonials, and any other content that needs to be organized in a clean and easy-to-read way. Grid layouts are a popular choice for websites because they are easy to use and can be customized to fit any design. Grid layouts are also responsive, meaning they will adapt to different screen sizes and devices. 

### React Bootstrap
React Bootstrap is a library with a complete re-implementation of Bootstrap components using React. It has no dependency on either bootstrap.js or jQuery. If you have React setup and React-Bootstrap installed you have everything you need.

Adding bootstrap to react app using npm:   
```linux
npm install react-bootstrap bootstrap
```
Using react bootstrap:   
```javascript
import React from 'react';
import { Container, Row, Col } from 'react-bootstrap';

function App() {
  return (
    <Container>
      <Row>
        <Col>1 of 1</Col>
      </Row>
      <Row>
        <Col>1 of 2</Col>
        <Col>2 of 2</Col>
      </Row>
      <Row>
        <Col>1 of 3</Col>
        <Col>2 of 3</Col>
        <Col>3 of 3</Col>
      </Row>
    </Container>
  );
}
```

### Transforming Lists  
When we need to transform a list of data, we can use the map() method to transform each item in the list into a new item, also when using the map() method, you will need to define a new variable, as it always returns a new array. This will allow us to fetched data from a third party or external provider.

Example of transforming lists:
```javascript
// In javascript we can use map to transform a list
const data = [
    {
        id:"1",
        title:"Milk",
        price:50
    }, 
    {
        id:"2",
        title:"Orange",
        price:1.50
    },
    {
        id:"3",
        title:"Apple",
        price:2.50
    }
];
function ListUse() {
    const listItem = data.map(values => {
        const itemText = '${values.title} - ${values.price}';
        return <li>itemText </li>
    });
    return (
        <div>
            <h1> {listItem} </h1>
        </div>
    );
}

export default ListUse;
```

Bellow is the same example but using React:
```javascript
function checkCalories(calToCheck) {
  const maxCalories = 100;
  return calToCheck.calories <= maxCalories;
}
function DessertsList(props) {
  // This code gets some data array from a react component
  const tempData = props.dataFromParentComponent;
  const tempSortedData = tempData.sort(
    (a, b) => a.calories - b.calories);
  const tempLowValue = tempSortedData.filter(checkCalories);
  const returningData = tempLowValue.map(newEditData => {
    const newItemsToShow = `${newEditData.name} - ${newEditData.calories}  calories`;
    return <li>{newItemsToShow}</li>;
  });
  return(
    <div>
      <ul>{returningData}</ul>
    </div>
  );
}

export default DessertsList;
```

### Keys on React
Keys help React identify which items have changed, are added, or are removed, also keys instructs the treatment of elements when an update occurs, avoiding unnecessary recreations. Keys should be given to the elements inside the array to give the elements a stable identity. Keys used within arrays should be unique among their siblings. However, they don’t need to be globally unique. We can use the key prop on the element itself instead of putting it inside a separate attribute. When we use the key attribute on an element, React uses the key attribute to track the elements in the list.
Using keys attribute on React we can avoid the following error:   
```javascript
Warning: Each child in a list should have a unique "key" prop.
```
Example of using keys on React:
```javascript
function ListUse() {
    const listItem = data.map(values => {
        const itemText = '${values.title} - ${values.price}';
        return <li key={values.id}>itemText </li>
    });
    return (
        <div>
            <h1> {listItem} </h1>
        </div>
    );
}
```
This example is a little bit less complex, but it shows how to use keys work:
```javascript
// Using Keys when we update the list of items
// React will know which items have changed, added, or removed
// without the key attribute, React will treat the list as a single unit and every 
// item will be updated when a change occurs
<ul>
  <li key='book'>book</li>
  <li key='page'>page</li>
</ul>

// In this case, React will know that the first item has been added and the second 
// and third items has stayed the same
<ul>
  <li key='title'>title</li>
  <li key='book'>book</li>
  <li key='page'>page</li>
</ul>
```
### Controlled Components
In a controlled component, form data is handled by a React component. The alternative is uncontrolled components, where form data is handled by the DOM itself. To write an uncontrolled component, instead of writing an event handler for every state update, you can use a ref to get form values from the DOM.   
In order to create a controlled component, we need to use a combination of local state and the value prop.
Example of a controlled component:
```javascript
import React, { useState } from "react";
onChange(event){
  setValue(event.target.value);
}


<form onSubmit={handleSubmit}>

</form>
  handleSubmite(event){
    validate(value);
    event.preventDefault();
  }
```
Example of a uncontrolled component:
```javascript
const Form = () => { 
 return ( 
   <div> 
     <input type="input text" /> 
   </div> 
 ); 
}; 
```
Getting the value of an uncontrolled component:
```javascript
//In the code below, you can see how a ref is used to 
//access the value of the input whenever the form is submitted.
const Form = () => { 
 const inputRef = useRef(null); 

 const handleSubmit = () => { 
   const inputValue = inputRef.current.value; 
   // Do something with the value 
 } 
 return ( 
   <form onSubmit={handleSubmit}> 
     <input ref={inputRef} type="text" /> 
   </form> 
 ); 
}; 
```
Now lets see how to use a controlled component, with the same example as above:
```javascript
// In the code example bellow we can see every time you type a new character, the 
// handleChange function is executed. It receives the new value of the input, and
// then it sets it in the state. 
const Form = () => { 
 const [value, setValue] = useState(""); 

 const handleChange = (e) => { 
   setValue(e.target.value) 
 } 

 return ( 
   <form> 
     <input 
       value={value} 
       onChange={handleChange} 
       type="text" 
     /> 
   </form> 
 ); 
}; 
```
#### Avoid default form behavior
To avoid the default behavoior of a form, we need to use the preventDefault() method.
```javascript
function App() {
  const {name, setName} = useState('');
  const handleSubmit = (event) => {
    event.preventDefault();  // <====== this line is important
    console.log('You clicked submit.');
  }
  return (
    <div className="App">
      <form onSubmit={handleSubmit}>
        <fieldset>
          <div className="Field">
            <label htmlFor="name">Name:</label>
            <input 
              type="text"
              placeholder="name" 
              name="name" 
              value={name}
              onChange={(event) => setName(event.target.value)} />
          </div>          
          <button type="submit">Submit</button>        
        </fieldset>
      </form>
    </div>
  );
}
```

### Something to remember when working with Forms on React
```JavaScript 
... 

// this is use to show an error message when the password is less than 8 characters
const PasswordErrorMessage = () => {
  return (
    <p className="FieldError">Password should have at least 8 characters</p>
  );
};

... 

function App() {

  // To be able to modify this value, we need to use: 
  // setPasswrod({ ...password, value: e.target.value }); 
  // setPassword({ ...password, isTouched: true }); 
  const [password, setPassword] = useState({
    value: "",
    isTouched: false,
  });

 
  // The important part is that we need to don't use the 
  // the if statement inside the return statement instead we need to use it
  // to write the condition of the return statement 
  const getIsFormValid = () => {
    // Implement this function
    return ( 
      (firstName != "") &&
      (role.value != 0) &&
      password.value.length >= 5
    );
  };

  const handleSubmit = (event) => {
    event.preventDefault();

    ...

    return;
  };

  return (
      <div className="App">
        <form onSubmit={handleSubmit}>
          <fieldset>
            <input
              placeholder="Password"
              type="password"
              placeholder="password"
              name="password" 
              value={password.value}
              onChange={(event) => { 
                setPassword({ ...password, value: event.target.value }); 
              }} 
              onBlur={() => { 
                setPassword({ ...password, isTouched: true }); 
              }} 
            />

            // if the password is less than 8 characters and is 
            // touched, then show the error message.
            // The important part is that we need to don't use the 
            // the if statement inside the return statement
            <div>
              {                
                password.isTouched && password.value.length < 8 ? (
                <PasswordErrorMessage /> 
                ) : null
              }
            </div>
          <button type="submit" disabled={!getIsFormValid()}>
            Create account
          </button>
        </form>
    </div>
  );
}

```
This is an example of the code above, checking if the password is valid
![React Router](/img/form_example.png)

### React Props and State
Props and state are related. The state of one component will often become the props of a child component. Props are passed to the child within the render method of the parent as the second argument to React.createElement() or, if you're using JSX, the more familiar tag attributes. State are managed within the component

Props is a short term for properties and they are used to pass data between React components. Props are immutable, which means that their data cannot be changed. Props are used to pass data, or functions, from one component to another. Data with props are being passed in a uni-directional flow. (one way from parent to child)

State is a special React object that stores a component's dynamic data and determines the component's behavior. State is mutable, which means that its data can be changed. State is used to store data that changes over time, or that comes from a user input. State is used to manage the data that changes in a React app.

#### Pasing data using Context
Props drilling problem, when we have a lot of nested components, we need to pass props from the top level component to the bottom level component, this is called props drilling. To avoid this problem we can use the Context API. The Context API is a React API that allows us to manage the state of a React app. The Context API is a way to pass data through the component tree without having to pass props down manually at every level.

Example of Context API: This is the UserContext.js file
```javascript
import { createContext } from "react";

const UserContext = createContext(undefined);
export const UserProvider = ({children}) => {
  const [user] = useState({
    name: "Kevin",
    age: 30,
  });
  return <UserContext.Provider value={{user}}></UserContext.Provider>
};
export const useUser = () => useContext(UserContext);
```

Example of Context API: I'm using the context on this App.js file
```javascript
import { UserProvider } from "./context/UserContext";

...

const LoggedUser = () => {
  const {user} = useUser();
  return {
    // This is the way to access the data from the context
    // The important part is within the curly braces
    <p>
      Hello <span className="UserName"> {user.name}, you are {user.age} years old.
    </p>
  }
}

...

function Root() {
  return (
    <UserProvider>
      <App />
    </UserProvider>
  );
}
Export default Root;
```



### React Rendering Process
React uses a declarative paradigm that makes it easier to reason about your application and aims to be both efficient and flexible. It designs simple views for each state in your application, and React will efficiently update and render just the right components when your data changes. Declarative views make your code more predictable and easier to debug. React can also render on the server using Node and power mobile apps using React Native.

#### React.memo
React.memo is a higher order component. It’s similar to React.PureComponent but for function components instead of classes. If your function component renders the same result given the same props, you can wrap it in a call to React.memo for a performance boost in some cases by memoizing the result. This means that React will skip rendering the component, and reuse the last rendered result.

#### React.PureComponent
React.PureComponent is similar to React.Component. The difference between them is that React.Component doesn’t implement shouldComponentUpdate(), but React.PureComponent implements it with a shallow prop and state comparison.

### Component composition with children
In React, component composition is a natural pattern of the component model. It's how we build components from other components, of varying complexity and specialization through props. Component composition is one of React's powerful compositional patterns. It's a way to combine simple functions together to create complex functions.

Example of component composition with children:
```javascript
const AlertMessage = ({ children }) => {
  return (
    <div className="alert alert-primary" role="alert">
      {children}
    </div>
  );
};

const ContinueButton = (
  <button className="btn btn-primary">Continue</button>
);

function App() {
  return (
    <div>
      <h1>My Header</h1>      
      <AlertMessage>
        <h4>Showing message</h4>
        <p>This is an alert message</p>
        <ContinueButton />
      </AlertMessage>
    </div>
  );
}
```
### Manipulating children dynamically in JSX
#### React.cloneElement()
Using React.cloneElement() we can manipulate children dynamically in JSX. React.cloneElement() is used to clone and return a new React element using a given element as the starting point. The resulting element will have the original element’s props with the new props merged in shallowly. New children will replace existing children. key and ref from the original element will be preserved.   
```JavaScript
// the first argument is the element to clone, the second argument 
// is an optional object of props to merge into the cloned element.
React.cloneElement(element, [props]) 
```
Example of manipulating children dynamically in JSX using React.cloneElement():
```javascript
const AlertMessage = ({ children }) => {
  const newChildren = React.cloneElement(children, {
    style: { color: "red" },
  });
  return (
    <div className="alert alert-primary" role="alert">
      {newChildren}
    </div>
  );
};
```
#### React.Children()
Using React.Children() we can manipulate children dynamically in JSX. React.Children provides utilities for dealing with the this.props.children opaque data structure.   

Example of manipulating children dynamically in JSX using React.Children():
```javascript

```
#### React.Children.Map()

Example of manipulating children dynamically in JSX using React.Children.Map():
```javascript
const AlertMessage = ({ children }) => {
  const newChildren = React.Children.map(children, (child) => {
    return React.cloneElement(child, {
      style: { color: "red" },
    });
  });
  return (
    <div className="alert alert-primary" role="alert">
      {newChildren}
    </div>
  );
};
```

### Webpack
Webpack is a static module bundler for modern JavaScript applications. When webpack processes your application, it internally builds a dependency graph which maps every module your project needs and generates one or more bundles, which are static assets to serve your content from.

More benefits of webpack:
- Smart way to bundle assets
- Better performance
- Better developer experience
- It converts modern JS code into older versions of JavaScript, this process is known as <b> transpiling </b>. 
- It can process your SCSS code into the regular CSS.
- It can produce various kinds of files based on rules and templates.

## Markdown Language 
Markdown is a lightweight markup language for creating formatted text using a plain-text editor. Markdown is widely used in blogging, instant messaging, online forums, collaborative software, documentation pages, and readme files.
### react-markdown
React component for rendering Markdown with react-markdown.
```linux
npm install react-markdown
```   
```javascript 
import React from 'react';
import ReactMarkdown from 'react-markdown';
```

### react-showdown
React component for rendering Markdown with showdown.   
```linux
npm install react-showdown
```
```javascript
import React from 'react';
import ReactShowdown from 'react-showdown';

```

## Miscellaneous
### Important to remember
- **\`** is used to interpolate a variable inside a string, also remember **\`** is not the same as **'** or **"**

### Important Terms
- **Isomorphic App's** can run both on the client and the server. This approach is also referred to as universal rendering.  

- **Lazy loading** is a technique for loading JavaScript code and other assets on demand, that is only when they are needed for rendering a portion of a page. Lazy loading is a great way to optimize your site or application, because it helps you reduce the amount of initial JavaScript sent to the browser by splitting your code into multiple bundles, and then loading them on demand.   

- **SSR (Server-side rendering)** is the process of rendering web pages on a server and passing them to the browser (client-side), instead of rendering them in the browser.   

- **Production mode** is an optimized version of the development mode. It is used to create a production build of the app.   

- **Development mode** is used to run the app locally. It is used to create a development build of the app.    

- **DRY (Don't Repeat Yourself)**
Is a principle of software development aimed at reducing repetition of software patterns, replacing it with abstractions or using data normalization to avoid redundancy.   
When the DRY principle is applied successfully, a modification of any single element of a system does not require a change in other logically unrelated elements. Additionally, elements that are logically related all change predictably and uniformly, and are thus kept in sync. 
Besides using methods and functions, we can also use loops to avoid repeating ourselves.   

- **Dependency graph** is a directed graph representing dependencies of several objects towards each other. It is used to model and solve scheduling problems.   

- **JSX** is a syntax extension to JavaScript. It is used with React to describe what the user interface should look like.

- **Deterministic** is an algorithm that, given a particular input, will always produce the same output, with the underlying machine always passing through the same sequence of states. Deterministic algorithms are by far the most studied and familiar kind of algorithm, as well as one of the most practical, since they can be run on real machines efficiently.


### Git CLI   
Basic commands to use git in the command line interface. Adding a new repository to GitHub using CLI.  
First navigate to the folder you want to add to GitHub using CLI and then use the following commands:

```CLI 
git init
```   
```CLI 
git add .
```   
```CLI 
git commit -m "type a message"
```   
```CLI 
git remote add "origin"
```  
```CLI 
git remote add kevincobos https://github.com/kevincobos/front-end-basic-react
   ```  
```CLI 
git push -u kevincobos main
```   

```CLI 
git push
``` 

### Create new branch using CLI
```CLI 
git branch A
```   
```CLI 
git checkout A
```
create new branch B and commit on it   
```CLI 
git checkout -b B
```    
```CLI 
git commit -am "commit on branch B"
```    
   
go back to branch A   
```CLI 
git checkout A
```       
```CLI 
git commit -am "commit on branch A"
```
   

### Disclaimer  
``` I have used GitHub Copilot to help me writing this readme file. ```

### References
- [React](https://reactjs.org/)
- [React Router](https://reactrouter.com/)
- [React Bootstrap](https://react-bootstrap.github.io/)
- [React Icons](https://react-icons.github.io/react-icons/)
- [React Hooks](https://reactjs.org/docs/hooks-intro.html)
- [React Context API](https://reactjs.org/docs/context.html)
- [GitHub Markup Language](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks)
- [React Player](https://www.npmjs.com/package/react-player)
- [React Markdown](https://www.npmjs.com/package/react-markdown)
- [React Showdown](https://www.npmjs.com/package/react-showdown)

### [Go back to Table of Contents](#table-of-contents)
  