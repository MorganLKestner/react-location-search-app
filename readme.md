##React Google Map Location Search App 
#### Updated for Current React

####Tutorial Article <a href="http://tutorialzine.com/2015/04/first-webapp-react/#comment-720101">Here</a> By  Nick Anastasov
Here you can follow the steps, and I have added the steps to have the app running with the current React version.


### Install 
Packages you need: <br>

<code> 
    browserify 
    moment
    react
    react-dom
    reactify
    uglify-js
    watchify
</code><br>
Use this format:<br>
<code>
npm install packageNameHere --save
</code>

###React-DOM 
The app tutorial is about a year old and you need to use React-Dom
- Here's an article about <a href="https://www.npmjs.com/package/react-dom">Using React-DOM</a><br>

Here are the following places that need React-DOM <br> 
In files Search.js | Map.js | Main.js
at the top <br>
<code> 
var ReactDom = require('react-dom');</code><br>

The original tutorial uses <code>getDOMNode()</code> in the <code>Search.js</code> file. 
React changed a few things. I found this <a href="http://stackoverflow.com/questions/33031516/reactjs-finddomnode-and-getdomnode-are-not-functions">article</a> helpful to understand the changes.

-Old Version <br>
<code><br>
handleSubmit(event){	
  	event.preventDefault();
		this.props.onSearch(this.state.value);
		this.getDOMNode().querySelector('input').blur();
},
</code>

-New Verison<br>
<code><br>
handleSubmit(event){
        event.preventDefault();
        this.props.onSearch(this.state.value);
        ReactDom.findDOMNode(this).querySelector('input').blur();
},
</code>
###CSS & GMAPS
I added this for the icons:

https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css

And this for the GMAPS which makes using google maps API a breeze:

https://cdnjs.cloudflare.com/ajax/libs/gmaps.js/0.4.24/gmaps.js


###Other Notes 
-Reps, Reps Reps
I highly suggest coding it out, and not copy and paste. Certainly sse a working version for reference. 
You will learn more, promise. 
-If there are any problems, submit an issue! 


