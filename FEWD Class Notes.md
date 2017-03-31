# jQuery Intro - Lession 8


## JavaScript Jot-Pair-Share

On the note card in front of you...

------

Take 60 seconds to **independently** answer the following questions as best you can, based on your experience with psuedocode/js so far:

- What is Pseudocode?
- Why is pseudocode useful?
- What is a practical application of Javascript on a webpage?


## JavaScript Jot-Pair-Share

Now, take 60 seconds and **share** your answers with your closest classmate


## JavaScript Jot-Pair-Share

- Pseudocode is a mixture of natural language and high-level programming constructs
- Pseudocode allows developers to think/sketch programmatically without being bound to a particular language or worrying about syntax
- Detecting a button click and changing colors of elements (event listening and DOM manipulation)


## Learning Objectives

- Differentiate between jQuery and JavaScript, describe benefits of using them
- Recognize jQuery Syntax
- Use selectors and jQuery functions to effectively manipulate the DOM


## Agenda

- Intro To Programming Review
- Intro To jQuery
- jQuery Basics
  - File Structure
  - Syntax
- FAQ Class Lab



#### Javascript Event listeners
![](../../img/extra/eventhandler.png)

Note:
Taken from  http://docplayer.net/docs-images/31/15119971/images/13-0.png on 5/16/16


## Objects, properties, methods

JavaScript sees the world in terms of objects, properties and methods

![](../../img/extra/js_object.png)

Note: Image from http://www.w3schools.com/js/js_objects.asp on 11/5/15


![](../../img/extra/js_object.png)

- All cars have the same **properties**, but the **property** **values** differ from car to car.
- All cars have the same **methods**, but the **methods** are performed at **different times**.


### Objects, properties, methods

#### Selecting an element in Javascript

![](../../img/extra/jsselector.jpg)

Note:
taken from https://www.safaribooksonline.com/library/view/head-first-html5/9781449314712/httpatomoreillycomsourceoreillyimages1345369.png.jpg on 5/16/16


### Objects, properties, methods

#### Responding to an event in JavaScript/Event Listeners

![](../../img/extra/jseventlistener.png)

Note:
taken from http://appendto.com/wp-content/uploads/2016/03/image00-1.png on 5/16/16


## Traffic light example

#### Where have we seen these?

http://codepen.io/barryross/pen/RaOajB


### Is there an easier way to do all of this ?

Let's look at how jQuery can help


## Javascript example

```
document.getElementById('grayButton').onclick = switchGray;
document.getElementById('whiteButton').onclick = switchWhite;
document.getElementById('blueButton').onclick = blueButton;
document.getElementById('greenButton').onclick = greenButton;

function switchGray() {
  document.body.style.backgroundColor = 'gray';
 document.body.style.color = 'white';
}

function switchWhite() {
  document.body.style.backgroundColor = 'white';
  document.body.style.color = 'black';
}

function blueButton() {
  document.body.style.backgroundColor = 'blue';
  document.body.style.color = 'black';
}

function greenButton() {
  document.body.style.backgroundColor = 'green';
  document.body.style.color = 'black';
}
```


## jQuery Example

```
$("#grayButton").click(switchGray)
function switchGray(){
  $("body").css(
    {"backgroundColor":"gray", color:"white"}
  )
}

$("#whiteButton").click(switchWhite)
function switchWhite(){
  $("body").css(
    {"backgroundColor":"white", color:"black"}
  )}

$("#blueButton").click(blueButton)
function switchBlue(){
  $("body").css(
    {"backgroundColor":"blue", color:"black"}
  )}

$("#greenButton").click(greenButton)
function switchGreen(){
  $("body").css(
    {"backgroundColor":"green", color:"black"}
  )}
```



### Intro to jQuery

jQuery provides the jQuery() function which lets us select elements using CSS selectors (and some unique to jQuery)

```
jQuery('li') //selects all <li>s on the page

it can be re-written as

$('li')
```

Note:
valid var names do not begin with numbers and don't contain hyphens http://jqfundamentals.com/chapter/jquery-basics https://learn.jquery.com/about-jquery/how-jquery-works/


### Intro to jQuery
#### What is it?

- jQuery is a JavaScript library (pre-written code that allows for easier development)  
- jQuery is written in JavaScript
- jQuery is cross-browser compatible
- jQuery makes DOM manipulation simple
- Document traversal (document-tree cherry picking)
- CSS Manipulation
- Event Handling
- Animation
- and more!


### Intro to jQuery
#### Adding jQuery to your website
##### jQuery.com

<iframe src="https://jquery.com/" width="800" height="400">


### Adding jQuery to your website
#### Linking to a local copy of jQuery.js

```
<script src="js/jquery-1.8.3.min.js"></script>
```


### Adding jQuery to your website
##### Linking to an external file (CDN)

```
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
```


### Intro to jQuery
#### Let's start using it!

- Examples
- Traffic light switcher code-along


## Syntax

__Syntax:__ Spelling and grammar rules of a programming language.

Note:
Like with any language, there are formal rules around how to write it. This is the syntax.


### jQuery syntax is like JS syntax
#### (for the most part)

- Semicolon
- Brackets
- Parentheses
- Quotation Marks


### Javascript

```
document.getElementById('uniqueObject').onclick = doSomething;

function doSomething(){
	alert("I am doing something ");
}
```

### jQuery

```
$("#uniqueObject").click(doSomething);

function doSomething(){

	alert("I am doing something ");
	}
```


### jQuery syntax is like JS syntax
#### Comments are the same

```
//Single Line Comments
```

```
/* Multi line comments /*
```



## jQuery Syntax - Selectors

Selectors are just like CSS

```
Selecting an element by its class -> $(".class").click();

Selecting an element by its id -> $("#id").click();
```

```
$('.class').click(doSomething);
function doSomething() {
	// make something happen here
}

$('#id').click(doSomething);
function doSomething() {
	// make something happen here
}
```

Note:
We will certainly be discussing this in more detail, but in general jQuery let’s us grab some element from the page ($('slector')), and do something with it ($('selector').click(doSomething);). In this case, we grabbed an element with the id thingy and used .click() to make a function run when the user clicks on #thingy.


## jQuery Click Event
### .click()

```
	$('#uniqueObject').click(doSomething);

	function doSomething() {
		// make something happen here
   	}
```

Can also be written shorthand, like this:

```
 	$('#uniqueObject').click(function(){
  	//make something happen here
	});
```


### jQuery - how does it all work?
![](../../img/extra/jquery-how-it-works.gif)


### Some jQuery Functions

```
.click()
.slideToggle()
.hide()
.show()
.slideUp()
.slideDown()
.children()
.attr()
```


![GeneralAssemb.ly](../../img/icons/code_along.png)

## jQuery Traffic Light

Note:

- Download jQuery library
- Add it after index.js


- change `<p>` tags to have the text display white
- change size of all the boxes
- make purple box bigger than the rest
- prevent link from its default behavior
- When the blue box is clicked, make the purple one disappear
- When the red box is clicked, make the purple appear again

**More difficult:**

- Create 2 new boxes , one yellow and one orange.  (hint: lookup after() or before() or *append()*)
- When the "Do Something" button is clicked, make the orange box slide up and disappear,


## Adding Interactivity

![GeneralAssemb.ly](../../img/icons/exercise_icon_md.png)


## FAQ Lab

![GeneralAssemb.ly](../../img/icons/exercise_icon_md.png)
