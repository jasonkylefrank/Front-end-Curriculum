
# Redux Introduction
Redux is the Flux implementation that we are using to tie our components together.  Flux is an architectural pattern that works especially well with React to handle data flow on the client.  

I think Redux is simpler to use than Facebook's Flux implementation. It also has the advantage of supporting **hot-reloading** and **"time travel"**.  More on those topics in a bit. 

In a nutshell, the main things to understand about Redux is that:
1. **It lets us avoid tightly coupling our React components**.  By using Redux, the React components don't need to know as much about each other.  They can simply fire Redux "actions" and other React components can receive modified data from the Redux "store".  
2. Pieces of your Redux code (not your React components) will **request and receive data from the server**. 

As a reference, you can think of the data flow illustrated in the following diagram (**React** would be our "View Provider").  Other resources that I will provide in the next sections will explain the details.

![](_assets/redux-diagram.png)

<p class="todo-note">
<strong>Todo:</strong> Somewhere discuss the notion of the Redux <code>store</code> being like a <strong>"model"</strong>, and React <strong>components</strong> taking on the role of both <strong>"view-model"</strong> and <strong>"view"</strong>.
</p>

## A note about learning Redux
When I was first learning React (without Redux), I found it easy to get started by learning just a few concepts.  I didn't feel like I had to understand a bunch of things just to reach a "critical mass" that would allow me to get going. 

In contrast, Redux (and even more so Facebook's Flux) requires you to understand more pieces before you can be comfortable doing much.  Its one of those things where you just need to reach a certain plateau of concepts, and then you'll be fine.

