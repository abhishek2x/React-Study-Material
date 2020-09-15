
# Fundamentals of React

>## Snippets
**Extension Name** : ES7 React/Redux/GraphQL/React-Native snippets

<ul>
<li>rce -> Creates a Class based component</li>
<li>rfce -> Creates a Functional component</li>
<li>rconst -> Creates the constructor for the class.</li>
</ul>

***

>## Lifecycle Methods
 
 ### Mounting
 When an instance of component is created or inserted into the DOM
 + constructor
 + static getDerivedStateFromProps 
 + render
 + componentDidMount
 ### Upgrading
 When a component is being re-rendered as a result of change to either it's props or state. 
 + static shouldComponentUpdate
 + shouldComponentMount
 + render
 + getSnapBeforeUpdate
 + componentDidUpdate
 ### Unmounting
 When the component is being removed from the DOM
 + componentWillUnmount
 ### Error handling
 When there is an error during rendering, in a lifecycle method, or in a constructor of a child component
 + static getDerivedStateFromError
 + componentDidCatch


***
>## Fragments
A common pattern in React is for a component to return multiple elements. Fragments let you group a list of children without adding extra nodes to the DO

>## Pure Component

Pure component only re-renders the class component when there is a shallow comparisn of props and state. This results in a performance improvement. It works only with class based components.

>## Memo
It is a higher order component. What pure component is to class based component ,memo is to functional components

***

>## Refs
Refs makes it possible to access DOM nodes in React. There are two valid approaches are:- 

<li>React.createRef() method</li>  
<li>Callback method.</li>

Refs can be used with both functional and class component. Refs can also be passed from a parent component to the child component.<br>

**Forwarding Ref**: Refs can also be forwarded from the parent compoonent to native input component using **forwardRef(*native component*, *ref*)** method. Basically the child component recieves the ref from the parent component and attaches it to the native input element.

>## Portals
*React portals provide a way to render children into a Dom node that exists outside the DOM hierarchy of the parent component*. It provides the ability the break out of the DOM Tree. It uses a function **ReactDOM.createPortal(*JSX*, *id*)**.Portal behave like a React child.
We need of Portals to deal with child-parent CSS

>## Error Boundary
*Error Boundary are React Component that catch JavaScript errors in the child component tree, log these errors, and display the fallback UI*
A Class Component that implements either one or both of the lifecycle methods *getDerivedStateFromError* and *componentDidCatch* becomes an error boundary. 

**getDerivedStateFromError**: This is a static method that is used to render the fallback UI after an error is thrown.<br>
**componentDidCatch**: This is a method which is used to log the error message.

Error Boundary catch error during rendering in lifecycle methods and in the constructor of the whole tree below them, however, they do not catch errors inside event handelers

***

>## Higher Order Component - HOC
*A pattern where a function takes a component as an argument and returns a new enhanced component*. It shares common properties within the components without having to repeat the code.

>const newComponent = higherOrderComponent( originalComponent )<br>
>Non-technical example: const  Ironman = withSuit( TonyStark )

It is a nice little pattern that can be used to share common funtionality between React Components.

>## Render Props 
The term "render prop" refers to a technique for **sharing code** between React Component using a **prop whose value is a function**.

>## React Context
Context provide a way to pass data through the component tree without having to pass props down manually at each level.<br>
It mainly includes three steps: 
* Create a context - Using createContext() method and export provider and consumer component as well.
* Provide a context value - At top level, include provider component and pass the value using value attribute.
* Consume the context value - Use comsumer component and pass a function as a child 

***
***
