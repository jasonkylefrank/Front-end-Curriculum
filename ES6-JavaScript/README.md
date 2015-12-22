#ES6 JavaScript

ES6 (or ES2015) is the latest standard version of JavaScript.  More specifically, ECMAScript (ES) is the language *specification* for JavaScript implementations.

We are seeing the JavaScript community using ES6, and much of the *React* community in particular seems to favor using it over the older ES5.  And from my experience using ES6 and reading other people's ES6 code, it is a welcome update.

Overall I think ES6 makes JavaScript coding *easier* and *safer* to write and understand.  And I think the learning curve is fairly low. 

Perhaps I will eventually break down this chapter into more detailed subsections.  But for now I just list some learning resources and brief commentary about them.  

## Learning Resources

### Preface

#### What to learn first
I would categorize ES6's main additions as: 
1. Syntax additions
2. New methods on native objects (like Array, String, and Math).

When you're first learning ES6, I think a good first goal is to be able to understand other people's ES6 code.  With that goal in mind, I recommend starting with the new *syntax* additions.  In contrast, the new *methods* will syntactically look the same, and will thus not trip you up - you can just look up what they do when you get to them.

#### Tips that I've not seen well-explained

**TODO**... grab the stuff from my email to David and Chad.



### Resources List

1. **[ECMAScript 6 (ES6): What’s New In The Next Version Of JavaScript](http://www.smashingmagazine.com/2015/10/es6-whats-new-next-version-javascript/)** by Lars Kappert (Smashing Magazine): This article talks about features in a to-the-point manner - focusing mostly on examples.  As stated in the preface above, I would skip over the sections that talk about new methods on the String, Math, and Array objects for now.  
2. **[Top 10 ES6 Features Every Busy JavaScript Developer Must Know](http://webapplog.com/es6/)** by Webapplog: This one complements the Smashing Magazine article above because it talks about a few different features than what that one does. 
3. **[ECMASCript 6 - New Features: Overview & Comparison](http://es6-features.org/#Constants)**:  One of the biggest ways to appreciate what ES6 gives you is to compare how it compares to the equivalent ES5 code.  That's what this resource excels at!  In fact, it provides not much of anything else.  Thus its not a great place to *start* your learning (since it does not try to explain things).  But is a great resource once you are ready to *compare* the two versions.
5. [**Exploring ES6**](http://exploringjs.com/es6/index.html) by Dr. Axel Rauschmayer:  This is a full ebook.  Its probably not the best place to start your learning. But if you want a larger reference or more-detailed explanations, this looks like a good source.  The author seems to be well-respected in the industry.

### Try out ES6 coding online

**TODO**... Show the Babel "try it out" page with an [example of block scope](https://babeljs.io/repl/#?experimental=false&evaluate=true&loose=false&spec=false&code=%0A%0A%0A%2F%2F%20*************%20%22let%22%20and%20%22const%22%20tests%20******************%0A(function()%20%7B%0A%20%20var%20x%20%3D%20%22Cat%22%3B%0A%20%20var%20y%20%3D%201%3B%0A%20%20const%20myConst%20%3D%20%22Some%20message%22%3B%0A%20%20%0A%20%20console.log(%22before%20the%20loop%2C%20x%20is%3A%20%22%20%2B%20x)%3B%0A%20%20console.log(%22before%20the%20loop%2C%20y%20is%3A%20%22%20%2B%20y)%3B%0A%20%20%0A%20%20%2F%2F%20a%20hundred%20lines%20later...%20(change%20x%20and%20y%20to%20%22let%22%20instead%20of%20%22var%22%20to%20see%20the%20difference)%0A%20%20for(var%20x%20%3D%200%3B%20x%20%3C%204%3B%20x%2B%2B)%20%7B%0A%20%20%20%20%2F%2F%20Unnamed%20developer%20with%20a%20name%20that%20sounds%20exactly%20like%20%22Jason%22%20has%20done%20this%2C%0A%20%20%20%20%2F%2F%20%20expecting%20this%20y's%20scope%20to%20be%20the%20loop%20(thinking%20that%20after%20the%20loop%20the%20outer%20y%20would%20still%20have%20its%20original%20value)%0A%20%20%20%20var%20y%20%3D%200%3B%0A%20%20%20%20%2F%2Flet%20y%20%3D%205%3B%0A%20%20%20%20%2F%2Fconsole.log(%22In%20the%20loop%2C%20x%20is%3A%20%22%20%2B%20x)%3B%0A%20%20%20%20%2F%2Fconsole.log(%22In%20the%20loop%2C%20y%20is%3A%20%22%20%2B%20y)%3B%0A%20%20%7D%0A%20%20console.log(%22%22)%3B%0A%20%20console.log(%22after%20the%20loop%2C%20x%20is%3A%20%22%20%2B%20x)%3B%0A%20%20console.log(%22after%20the%20loop%2C%20y%20is%3A%20%22%20%2B%20y)%3B%0A%20%20%0A%20%20%2F%2F%2FmyConst%20%3D%20%22bla%22%3B%0A%7D)()%3B%0A%2F%2F%20-------------------------------------%0A%0A%2F*%0A%2F%2F%20**************%20class%20and%20arrow%20function%20tests%20%20*******************%0Aclass%20David%20%7B%0A%20%20constructor()%20%7B%0A%20%20%20%20this.x%20%3D%205%3B%0A%20%20%20%20this.y%20%3D%206%3B%0A%20%20%7D%0A%20%20%0A%20%20doSomething()%20%7B%0A%20%20%20%20console.log(%22before%20setTimeout%3A%20%22%20%2B%20this.x)%3B%0A%20%20%20%20%2F%2F%20ES5%20problem%20child...%0A%20%20%20%20setTimeout(function()%20%7B%0A%20%20%20%20%20%20console.log(%22In%20the%20setTimeout%2C%20without%20arrow%20func%3A%20%22%20%2B%20this.x)%3B%0A%20%20%20%20%7D%2C%20%20%20%20%2F%2F%20Would%20have%20to%20add%20%20%22.bind(this)%22%20to%20the%20end%20of%20the%20anonymous%20func%20to%20get%20it%20to%20work%0A%20%20%20%201000)%3B%20%0A%20%20%20%20%0A%20%20%20%20%2F%2F%20Using%20ES6%20arrow%20function%0A%20%20%20%20setTimeout(%0A%20%20%20%20%20%20()%20%3D%3E%20%7B%0A%20%20%20%20%20%20%20%20console.log(%22In%20the%20setTimeout%2C%20WTIH%20arrow%20func%3A%20%22%20%2B%20this.x)%3B%20%0A%20%20%20%20%20%20%7D%2C%20%0A%20%20%20%20%20%201000)%3B%0A%20%20%7D%0A%7D%0A%0Avar%20myDavid%20%3D%20new%20David()%3B%0AmyDavid.doSomething()%3B%0A*%2F)



More to come...