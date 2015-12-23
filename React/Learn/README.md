# Learn React

## Introduction
There are two main parts of the React ecosystem to learn:
1. The **React** library
2. A **Flux** implementation

**React** is the library that lets you write components for your UI.  If you're brand-new to React, head over to the [Getting Started](/Getting-Started/README.md) sub-chapter.

**Flux** is an architectural pattern that works especially well with React to handle data flow on the client.  For our Flux implementation, we are using the Redux library.  I have an entire chapter dedicated to Redux, so I won't get into it too much yet.  The main thing to understand about Redux at this point is that:
1. **It lets us avoid tightly coupling our React components**.  As you'll see when you get to the Redux chapter, the React components don't need to know as much about each other when they can simply fire Redux "actions" and other React components can receive modified data from the Redux "store".  
2. Peices of your Redux code will usually **fetch and receive data from the server**. 

