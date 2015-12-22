# React Tips


## Should your component have `state` or only `props`?

React's concepts and API and pretty simple.  But like many things in software development, figuring out how to *architect* things can be more difficult.  This topic is one of those architectural items.

React's website has good resources to explain the main issues to think about.  Under under the "Getting Started" section, they have a page called "[Thinking in React](http://facebook.github.io/react/docs/thinking-in-react.html)" that you should read.

In general, React seems to caution against Components holding `state` - saying that more often they should rely on `props`.  

### A tricky case: Component needs `state` from external data
One tricky case that I've come across is where it does make sense for a Component to hold its own `state`, but it needs to get the *data* for its `state` from somewhere else (like from the server).  How should you handle this case?

<p class="todo-note">
<strong>TODO:</strong> Explain the situation with an example about a table component and its subcomponents (a subcomponent may need to store the list of rows in its own presentational way such as sorted and search-filtered).  
</p>

You may have seen in the React docs the tip which declares that "[Props in getInitialState is an Anti-Pattern](http://facebook.github.io/react/tips/props-in-getInitialState-as-anti-pattern.html)".  The gist is that, "Using props, passed down from parent, to generate state in getInitialState often leads to duplication of "source of truth", i.e. where the real data is".  However, they go on to say that "it's not an anti-pattern if you make it clear that *synchronization*'s not the goal here:".

```var Counter = React.createClass({
  getInitialState: function() {
    // naming it initialX clearly indicates that the only purpose
    // of the passed down prop is to initialize something internally
    return {count: this.props.initialCount};
  },

  handleClick: function() {
    this.setState({count: this.state.count + 1});
  },

  render: function() {
    return <div onClick={this.handleClick}>{this.state.count}</div>;
  }
});

ReactDOM.render(<Counter initialCount={7}/>, mountNode);```


We must also consider how our use of the Flux pattern comes into play (and specifically Redux)...
