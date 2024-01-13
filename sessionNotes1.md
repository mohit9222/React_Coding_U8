/** Let's get classy **/

E8 P1 - TOPICS
Class based components
Syntax
class vs function components
why do we need to use a super(props)? Cant we avoid it?

---

Class based components

> Older way to create components in react
> Helps understanding react better
> We will make use of About page and show the team members using class based components

## objective - showcase fetch data from github and show in the About us page

> creating a user component using functional and class component

> Class components - Are normal javascript class
> Syntax:

class componentName extends React.Component {
render(){
return(
// piece of JSX
)
}
}

> A class based component is a class which has a "render() method" which returns some piece of JSX which is displayed on the UI
> A functional component is a function which returns some piece of JSX which is displayed on the UI

## React.Component

> This is basically a class which is given to us by react and the component is inherting some properties from it
> React.Component comes from react package

## passing and receiving props(properties) in a class based component

<UserClass name={"Mohit (Class)"}>

- We need to create a constructor in the class component to receive the props

constructor(props){
super(props)
}

> we cannot avoid writing super(props), it will give an error
> We will always have to use the "this" keyword to access our props in class components anywhere
> {this.props.name}
> whenever the instance of the particular class is created a contstuctor is called, props are extracted and can be used anywhere in the code
> This is how we get props from our parent component
> All the props will be combined into a single object and it is passed
> It can also be destructured
> Super is a keyword in JavaScript and is used to call super or parent class in the hierarchy and the purpose of getting access to this keyword inside our constructor
