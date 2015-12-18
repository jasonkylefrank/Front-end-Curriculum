
# Redux
Redux is the Flux implementation that we are using to tie our components together.


## Actions
Actions are a core concept of Redux.  Generally something in the UI will trigger an action.  "Reducers" will determine what to do to the app's state based on the action.  Per React's normal rendering paradigm, the UI will re-render when the state changes.

![](2015-12-18_16-27-13.jpg)


### Asynchronous actions (e.g., web requests)
Actions which should not execute synchronously require a slightly different approach.  This YouTube [video](https://youtu.be/764wvf8KuTw?t=1121) explains the concept.

![](2015-12-18_16-07-28.jpg)


This section of the video has a nice illustration of how action creators can fire a "start" and an "end" action.

![](2015-12-18_16-28-44.jpg)

This way the UI can respond to the fact that a web request is in progress (perhaps displaying a spinner).  Then when the "end" action fires, the UI can display new data.  The key idea here is that the UI only needed to dispatch one action (by an action creator) - and that action creator handled the "start" and the "end" action.


See the Redux docs for the full explanation about [async actions](http://rackt.org/redux/docs/advanced/AsyncActions.html).
