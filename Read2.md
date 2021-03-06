# State and Props


## What are props?
**Props is short for properties and they are used to pass data between React components. React’s data flow between components is uni-directional (from parent to child only).**

>How do you pass data with props?

*Here is an example of how data can be passed by using props:*

    class ParentComponent extends Component {    
    render() {    
        return (        
            <ChildComponent name="First Child" />    
        );  
    }
    }

    const ChildComponent = (props) => {    
        return <p>{props.name}</p>; 
    };

>**Firstly, we need to define/get some data from the parent component and assign it to a child component’s “prop” attribute.**

`<ChildComponent name="First Child" />`
**“Name” is a defined prop here and contains text data. Then we can pass data with props like we’re giving an argument to a function:**

    const ChildComponent = (props) => {  
    // statements
    };

>And finally, we use dot notation to access the prop data and render it:

>`return <p>{props.name}</p>;`


## **What is state?**

**React has another special built-in object called state, which allows components to create and manage their own data. So unlike props, components cannot pass data with state, but they can create and manage it internally.**

>Here is an example showing how to use state:

    class Test extends React.Component {    
    constructor() {    
        this.state = {      
            id: 1,      
            name: "test"    
        };  
    }    
    
    render() {    
        return (      
            <div>        
              <p>{this.state.id}</p>        
              <p>{this.state.name}</p>      
            </div>    
        );  
    }
    }

>*How do you update a component’s state?
State should not be modified directly, but it can be modified with a special method called `setState( ).`*


    this.state.id = “2020”; // wrong

    this.setState({         // correct  
        id: "2020"
    });


## What happens when state changes?
**OK, why must we use setState( )? Why do we even need the state object itself? If you’re asking these questions, don't worry – you’ll understand state soon :) Let me answer.**

A change in the state happens based on user-input, triggering an event, and so on. Also, React components (with state) are rendered based on the data in the state. State holds the initial information.

So when state changes, React gets informed and immediately re-renders the DOM – not the whole DOM, but only the component with the updated state. This is one of the reasons why React is fast.

And how does React get notified? You guessed it: with `setState( )`. The `setState( )` method triggers the re-rendering process for the updated parts. React gets informed, knows which part(s) to change, and does it quickly without re-rendering the whole *DOM*.


>In summary, there are 2 important points we need to pay attention to when using state:

* State shouldn’t be modified directly – the setState( ) should be used
* State affects the performance of your app, and therefore it shouldn’t be used unnecessarily

## Can I use state in every component?

>Another important question you might ask about state is where exactly we can use it. In the early days, state could only be used in class components, not in functional components.


## What are the differences between props and state?

* Components receive data from outside with props, whereas they can create and manage their own data with state
* Props are used to pass data, whereas state is for managing data
* Data from props is read-only, and cannot be modified by a component that is receiving it from outside
* State data can be modified by its own component, but is private (cannot be accessed from outside)
* Props can only be passed from parent component to child (unidirectional flow)
* Modifying state should happen with the `setState ( )` method