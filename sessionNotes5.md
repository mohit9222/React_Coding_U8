/** Let's get classy **/

E8 P5 - TOPICS

## What if we had multiple children and one parent how would the lifecycle look like?

> We can use the same component and pass different props too
> The following happens:

Parent Constructor
Parent Render

Child1 Constructor
Child1 Render
Child2 Constructor
Child2 Render

<DOM UPDATED - IN A SINGLE BATCH>
Child1 componentDidMount
Child2 componentDidMount
Parent componentDidMount

When the component is mounted, it is mounted in two phases

1. Render phase

   > First the constructor is called, then render is called which are in the render phase
   > It is pure and has no side effects

2. Commit phase

   > Then react updates the DOM and refs and then the componentDidMount is called in the commit phase

> Mounting happens for all the components(parent and child)

## Optimization of React

> Since there are two children, react will batch the render phase for both the children
> Then the commit phase will be called for the children

## Why does react do this?

Since DOM manipulation is very expensive(takes a lot of time)
render - reconciliation process (virtual DOM)
Render phase is fast, commit takes time
It optimises the performance of react app
