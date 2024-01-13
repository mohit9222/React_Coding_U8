/** Let's get classy **/

E8 P7 - TOPICS

> Never ever compare Reacts "Life cycle methods" to functional components
> After a subsequent render it is updated
> mount, update, unmount - there is a difference

## One life cycle method that is called after every render?

componentDidUpdate() - called after every update

In a functional component when we call useEffect(),
useEffect(() => {

},[count])

to achieve the above in class component we needed to do the following

componantDidUpdate(prevProps,prevState){
if(this.state.count != prevState.count){
// then do something
}
}

// In functional component if we want to do two different things then ow do we do it?
We make use of two useEffects

useEffect(() => {

},[count1])

useEffect(() => {

},[count2])

// how do we the same in class component?
componentDidUpdate(prevProps, prevState){
if(this.state.count1 != prevState.count1){
//
}
if(this.state.count2 != prevState.count2){
//
}
}

## When will use componentDidUpdate()

## When we are leaving our page/component

Just a single page we will change only the component
Lots of things need to be cleared
It is the issue with SPA, everytime a setInterval is called it creates a new interval while moving between pages
componentDidUpdate(){
this.time = setInterval(() => {

    },1000);

}

## Need to take care of every single line of code

How do we clear the interval?
In the componentWillUnmount()
how do reference it?
We make use of "this" keyword
componentWillUnmount(){
clearInterval(this.timer)
}

In functional component if we add the setInterval inside the componentDidMount it will not stop, behaves how it behaves just like how it does in class component

How do we clear the interal

we can return a function in useEffect.
return = () => {

}

called when we are unmounting it

useEffect(() => {
const timer = setInterval(() =>{

    },1000)
    return = () => {
        clearInterval(timer)

}
}[])

we cannot make the useffect as async in functional component
