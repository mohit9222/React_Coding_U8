/** Let's get classy **/

E8 P2 - TOPICS
creating state/local variables in a class component

--

In a functional component we make use of a hooks
Creating a state variable in a class component (old way)

## creating state/local variables in a class component

State was created when a instance of a class was created

invoking - loading/mounting a function
instance of class - loading a class based components

constructor - Best place to create state variables
we make use of :

this.state = {
.. object which contains state variables
}

accessing state variables:
{this.state.count}

## how to create two state variables in functional and class components?

functional component

> const [count2] = useState(1);

<h1>Count2 = {count2}</h1>

class component

> state is big object which contains all the state variables

this.state = {
count: 0,
count2: 1,
};

> accessing state variables in class components

<h1>Count2: {this.state.count2}</h1>
