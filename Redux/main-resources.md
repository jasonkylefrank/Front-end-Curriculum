## Main Redux Resources
The best resources I've found so far are:
1. [**Hot Reloading with Time Travel at react-europe 2015**](https://www.youtube.com/watch?v=xsSnOQynTHs). This video is a 30 minute talk by Dan Abramov – creator of the React Hot Loader and Redux.  This talk is primarily about the hot reloading and time-travel capabilities that these two technologies are capable of. However, you'll also begin to learn about programming concepts that are core to Redux, such as pure functions.  If nothing else, this video should get you pretty pumped up about this architecture!

 ![](_assets/2015-12-18_18-02-41.jpg)
 <br /><br />
 
2. [**Cleaning the Tar: Using React within the Firefox Developer Tools**](https://www.youtube.com/watch?v=qUlRpybs7_c) by James Long.  This video (~40 minutes) is a talk by James Long, a developer on the Firefox team at Mozilla.  What’s interesting about this video is that it is a completely different source (different from Dan Abromov talking about his products), but it corroborates the same architecture principles of React and Redux that make these new tools possible.  Like Dan’s talk, this one talks about React’s pure functions and such.  James also shows a completely different implementation of the “time travel” concept that Dan Abromov shows.  James’ implementation uses a UI slider to walk forward or backward in time.  If you only have time to watch one of these 2 videos, however, watch the first one by Dan Abramov.
![](_assets/2015-12-18_18-10-09.jpg) What is shown in this screenshot is a representation of an app's state at different points in time.  With React and Redux, you can step through these points in time simply by capturing the "actions".  

 I should point out one thing that confused me the first time I saw this video.  The speaker is using the Firefox dev tools for his demonstration... but what I didn't understand was that the dev tools *is* the UI in this case (not something that he's using to debug a different UI):
 ![](_assets/2015-12-18_22-13-59.jpg)
<br /><br />

3. Now for a resource that actually teaches you how Redux works and how to use it in an application.  [**Getting started with Redux**](https://egghead.io/series/getting-started-with-redux) is a video series of 30 short videos by Dan Abramov, creator of Redux.  In this series he explains both the concepts of Redux and how to implement the pieces.  It is very down to earth and easy to follow.  Along the way, he shows a few benefits of ES6 (but that’s not the focus).  If you only have a very limited amount of time, you could watch just the first 4 videos (totaling about 8 minutes) to get a sense of both what Redux is like and the quality of this resource.  
![](_assets/2015-12-18_18-33-59.jpg)
<br /><br />

4. The [**official Redux documentation**](http://rackt.org/redux/index.html) is excellent. If nothing else, you should check out the [Basics section](http://rackt.org/redux/docs/basics/index.html), which is a good written counterpart to the 30-video series mentioned above (it creates a Todo app).
<br /><br />

5. [**Immutable Data and React**](https://www.youtube.com/watch?v=I7IdS-PbEgI) from React.js Conf 2015.  As you'll learn in the other resources for Redux, immutability is a key component to Redux.  When we first presented Redux to our architecture team, they had questions about the **memory usage** and about **how the change-detection works**.  These are 2 key aspects of using immutable data.  

 ![](_assets/2015-12-18_19-00-01.jpg)

 This video shows:
     1. How **memory usage** can be efficient (via “structural sharing”)
     2. How **change-detection** becomes:
        1. very *easy* to check for (just comparing the reference of the “before” and “after”), and,
        2. extremely *fast* (O(1)). 
 <br /><br />
 
 Note that the *implementation* of immutability in this video uses the Immutable.js library – but that is just one way to go about this.  (Recall that Dan Abromav shows doing without that library in his Egghead videos.)  So the *implementation* that he shows is not the important part here – the 2 key aspects mentioned above are.  

 <p class="g2-note"> <span class="g2-note__heading">G2 Note</span>: as of December 2015, we have not determined whether or not we will use the <span class="bold">Immutable.js</span> library.</p>


