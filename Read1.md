# Introduction to React and Components

## What is a component?

> **A Component** : is a software object, intended to interact with other components, encapsulating certain functionality or a set of functionalities. It has an obviously defined interface and conforms to a recommended behavior common to all components within an architecture.

## What are the charactistics of a component?

* **Reusability** − Components are usually designed to be reused in different situations in different applications. However, some components may be designed for a specific task.

* **Replaceable** − Components may be freely substituted with other similar components.

* **Not context specific** − Components are designed to operate in different environments and contexts.

* **Extensible** − A component can be extended from existing components to provide new behavior.

* **Encapsulated** − A A component depicts the interfaces, which allow the caller to use its functionality, and do not expose details of the internal processes or any internal variables or state.

* **Independent** − Components are designed to have minimal dependencies on other components.

## What are the advantages of using component based architecture?

* **Ease of deployment**

* **Reduced cost**

* **Ease of development**

* **Reusable**

* **Modification of technical complexity**

* **Reliability**

* **Independent**

* **System maintenance and evolution**

# Props

## What is props short for?

`Props is a special keyword in React, which stands for properties and is being used for passing data from one component to another.*`

## How are props used in React?
* Firstly, define an attribute and its value(data)
* Then pass it to child component(s) by using Props
* Finally, render the Props Data

## What is the flow of props?

**Adding Flow types to your React components is incredibly powerful. After typing your component, Flow will statically ensure that you are using the component in the way it was designed to be used.**

**Early in React’s history the library provided `PropTypes` which performed basic runtime checks. Flow is much more powerful as it can tell you when you are misusing a component without running your code.**

**There are some Babel plugins which will generate `PropTypes` from Flow types such as `babel-plugin-react-flow-props-to-prop-types` if you want both static and runtime checks.**

> Finally: We can talk about `flow of props` is more powerful way ^_^