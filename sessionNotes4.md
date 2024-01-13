/** Let's get classy **/

E8 P4 - TOPICS

Life Cycle methods

## How the class based component is mounted/loaded

> Whenever the parent(about) component is rendered on to the web page, it basically starts rendering the JSX
> When mounting it comes across the UserClass component, it starts loading the class component(instance of this class is created)
> First thing that is loaded when a class is called(instance of the class is created) is the constructor
> Next render() is called
> Class (instance of class) -> Constructor is called -> render() is called

We can write it like this too:
// import { Component } from "react";

class About extends Component {
render(){
returm(
//
)
}
}

## How are parent and child components loaded on to the DOM (class based)

Instance of the parent class is created
Constructor of Parent is called
Parent render is called
child constructor
child render

## Class based components have one more method called componentDidMount()

> Given to us by react class based component
> When its loaded first the CONSTRUCTOR is called, then the RENDER() is called, once this class based component is mounted on to the DOM then this method(componentDidMount) is called
> It is called when the component is mounted

## what if we had one componentDidMount in our Parent too?

Parent constructor
Parent render
child constructor
child render
child component is mounted
parent component is mounted

Thats how parent-child lifeCycle methods work

## why do we use componentDidMount()?

? It is used to make API CALLS - WHY?

> Just like how in our functional components we make use of useEffect where the pageloads we quickly render some data then make a API call and quickly render the data similarly we make use of componentDidMount in class based components for the same reaso
