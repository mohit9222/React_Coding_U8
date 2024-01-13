/** Let's get classy **/

E8 P3 - TOPICS

how do we update state variables in functional vs class components

--

# how do we update state variables in functional vs class components

- functional components

> We make use of setState

const [count,setCount] = useState(0);

<button
onClick={() => {
const updateCount = count + 1;
setCount(updateCount);
}} >
Increase Count
</button>

- class components
  > Never update state variables directly in class components
  > Never update state in class components using "="
  > React gives us "this.setState({ we pass an object})"
  > Object contains the updated state values

this.state = {
count: 0,
}

this.setState({
count: this.state.count + 1,
})

## behind the scenes

When the button was clicked, react takes this object and will find out how many variables are there which need to be updated and updates only those values without touching all of them

Updates only the portion of the object(Compares the DOMS and calls the reconcilition algo)
