# Redux tips

## Actions
Actions are a core concept of Redux.  Generally something in the UI will trigger an action.  "Reducers" will determine what to do to the app's state based on the action.  Per React's normal rendering paradigm, the UI will re-render when the state changes.

![](_assets/2015-12-18_16-27-13.jpg)


### Asynchronous actions (e.g., web requests)
Actions which should not execute synchronously require a slightly different approach.  This YouTube [video](https://youtu.be/764wvf8KuTw?t=1121) explains the concept.

![](_assets/2015-12-18_16-07-28.jpg)


This section of the video has a nice illustration of how action creators can fire a "start" and an "end" action.

![](_assets/2015-12-18_16-28-44.jpg)

This way the UI can respond to the fact that a web request is in progress (perhaps displaying a spinner).  Then when the "end" action fires, the UI can display new data.  The key idea here is that the UI only needed to dispatch one action (by an action creator) - and that action creator initiated the "start" and the "end" actions.


See the Redux docs for the full explanation about [async actions](http://rackt.org/redux/docs/advanced/AsyncActions.html).


## Where to put **react-redux's `connect()`** calls?

### First, what is **react-redux**?
[React-redux](https://github.com/rackt/react-redux) is a very small add-on library that makes it easy for React components to connect to Redux stores.  Connected React components receive new data automatically when the Redux store state changes.

Redux's docs explain how to setup this connection in its "[usage with React](http://rackt.org/redux/docs/basics/UsageWithReact.html)" section.

### Now, what's the problem?




...we wrap the components we want to connect to Redux with the connect() function from react-redux. Try to only do this for a top-level component, or route handlers. While technically you can connect() any component in your app to Redux store, avoid doing this too deeply, because it will make the data flow harder to trace.