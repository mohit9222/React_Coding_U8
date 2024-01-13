/** Let's get classy **/

E8 P6 - TOPICS

## How to make an api call in compountDidMount()

> We can make the compentDidMount() a async function while fetching the data

## Updating Phase

> As soon as the class was loaded, the constructor was called with the state variables(In the render phase) after this render was called.
> The state variable had default values, so the render happens with a default value (React update the DOM/component with the dummy data)
> Now the componentDidMount() was called with the API call, then it called the setState our updating cycle begins
> Mounting cycle finishes when the render cycle is finished once
> Component is quicky rendered with the dummy data in the Mounting phase
> Now the setState is called, this updates the state variables
> when the state variable is updated, react triggers render once again (Constructor is called only once) with the updated value (Compare the diff and updates the DOM)
> Once react updates our DOM, react calls a method called componentDidUpdate()

## componentDidUpdate()

---MOUNTING----
Constructor(dummy)
Render(dummy)

<HTML with DUMMY>
componentDidMount()
<API call is made>
<this.setState> --> state variable is updated

--UPDATE-----
render(API data)

<HTML is loaded (With API data)>
componentDidUpdate()

Mounting cycle -> Updating Cycle -> Unmounting Cycle

--UNMOUNTING-----

## Unmounting

componentWillUnmount()
This will unmount just before our component is unmounting
unmount - > When this component will disappear from the HTML
When we go to a different page this will umount
