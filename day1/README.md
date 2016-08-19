##Day 1
<br>

| **Learning Objectives** |
| :---- |
| Distinguish between front-end and back-end development |
| Learn about some of the tools of the trade: Git, Sublime, and Chrome Developer Tools  |
| Learn and apply some basic HTML tags and CSS properties |
| Apply what you've learned|
| All of the things|

<br>
<img src="http://rationalreactor.com/wp-content/uploads/2013/09/learnallthethings.png">

## Front-end Web Development
<hr>


**Front-end web development** consists of two overlapping components: *front-end web development* and *web design*.

<img src="http://image.slidesharecdn.com/ixda-russweakley-2015-02-02-v2-150202161632-conversion-gate02/95/specialise-or-crossskill-9-638.jpg">

The front-end developer's job is to program the *layout* and *functionality* of a website. Everything that you see when using the web is a combination of HTML, CSS, and JavaScript all being controlled by your computer’s browser (and not a central server). These include things like **fonts, drop-down menus, buttons, transitions, sliders, contact forms, etc.**

<img src="http://freestock.ca/antique_anatomy_illustration__human_skeleton_circa_1911_sjpg3242.jpg">

- **HTML** describes the structure and the semantic content of a web document. It is the scaffold that adds various layout elements to your website. (The bones!)
- **CSS** is a set of style properties that give your page its look and feel. (The skin?)
- **JavaScript** (and its libraries) adds interactivity to the page.  When the user clicks a button, or submits a form, or there is some other kind of **event**, Javascript knows what to do. (The muscle.)
-- There are also tons of **front-end [frameworks](https://www.airpair.com/js/javascript-framework-comparison) and [libraries](https://www.javascripting.com/)** that make web applications prettier and more functional.

Demo in [Chrome Dev Tools](https://developer.chrome.com/devtools)

<br>

## Back-end Web Development (server + application + database)

- Provides core behind-the-scenes functionality
  - Manage user accounts
  - Database stuff - CRUD operations (Create, Read, Update, Destroy)
  - Reliability
  - Security

- Languages
  - Ruby
  - Python
  - PHP
  - C++

<img src="http://media.giphy.com/media/AqWimIaM4ao4U/giphy.gif">

## Developer Tools

- [Sublime](http://www.sublimetext.com/)
  - file types
  - "open in browser" command
  - multi-window
  - [keyboard shortcuts](http://sublime-text-unofficial-documentation.readthedocs.org/en/latest/reference/keyboard_shortcuts_osx.html)! (⌘+ everything)

- Chrome Developer Tools (⌘ + option + J)
  - Inspect and edit HTML elements and CSS style properties
  - Program "what-if" scenarios
  - Look at file structure
  - Examine network activity

- Git/Github
  - Version control
  - Collaboration

- CSS Frameworks
  - Bootstrap
  - Foundation
  - Tons more

- [Javascript Libraries](https://www.javascripting.com/)
  - jQuery
  - Underscore
  - Tons more

## What is the benefit of UX Designers understanding FEWD?

- Marketability ($$$)
- Better communication with your development team
- Better understanding of existing web applications and code stacks
- Work with Axure-generated HTML, CSS, and JS

<br>


##HTML

**Elements** are the basic HTML building blocks of a web page. They are comprised of a *tag, attribute, value, and some sort of content.* 

**Tags** define the element and any attributes it has. (e.g. headers, paragraphs, images)

**Attributes** modify an element in some way. They bridge the gap between HTML and CSS. (e.g. class, id)

**Values** define how the element will be modified. (based on CSS)



<br>

![alt text](https://github.com/rycwilson/FEWD-UXDI-2day/blob/master/img/html_element.png?raw=true)

<br>

- Most elements have attributes that provide additional meaning or behavior

![alt text](https://github.com/rycwilson/FEWD-UXDI-2day/blob/master/img/element_attribute.png?raw=true)


<br>

##Common  HTML Elements
For a comprehensive list: [MDN HTML Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference)


###Required elements - \<html>, \<head>, \<body>
- `<!DOCTYPE html>` identifies the doc as HTML5
- `<html>` encompasses everything in the document, tells the browser to interpret the document as html
- `<head>` is a section for data about the document, or inclusion of other files (CSS, Javascript).  Tags here aren't displayed in the browser
- `<body>` is the content of the page that will be displayed in the browser
- `<title>` creates a title to be displayed in the browser tab

```
<!DOCTYPE html>
<html>
<head>
  <title>BEST WEBSITE EVERRR</title>
</head>
<body>
  <!-- Contents of the page go here -->
</body>
</html>
```

###\<div>
- Like empty rectangular containers that help organize content on the page
- An arbitrary number of other elements can be nested inside of a `<div>`, including other `<div>` elements

```
 <div class='row'>
   <div class='column1'>
     <!-- column 1 content here -->
   </div>
   <div class='column2'>
     <!-- column 2 content here -->
   </div>
 </div>
```

###\<span>
- Generic container like a `<div>`, but `<span>` is for **inline** elements while `<div>` is for **block-level** elements
- usually used to single out some snippet of text for styling

```
 <p>Learning about web design is <span class='best-class-ever'>THE BEST.</span></p>
```

###\<a>
- Anchor link: clickable link to any URL or to any element in the same page

```
 <!-- link to some external site -->
 <a href="http://google.com">Google</a>
```
```
 <!-- link to an anchor on the same page -->
 <a href="#target">Go to Section 3</a>
 ...
 <a id="target">Section 3</a>
```

###\<input>
- Interactive controls for accepting user input.  There are several different types...
- The `type` attribute allows for different forms of user input (e.g. text, checkbox, radio button, date)
- Like the anchor tag, it's a **self-closing element**, i.e. no closing tag is required

```
<label for="name">Name: </label>
<input type="text" id="name">
```
... will display this:

<label for="name">Name: </label>
<input type="text" id="name">

<br>

###\<form>
- Forms are one of the most common ways to send user input to a server
- Inputs contained within the form get sent to the server on **submit** event 
  - What triggers a submit?  Usually `<input type="submit">` is clicked.  
- The inputs of a form are collectively referred to as **form controls**

<br>


###\<h1> .. \<h6> - heading elements
```
 <h1>Largest Heading</h1>
 ...
 <h6>Smallest Heading</h6>
```

###\<p>
```
 <p>Paragraphs are my fave.</p>
```


###\<button>

```
<button type="submit">Click here!</button>
```


###\<ul>
- unordered list (aka bulleted lists)

```
 <ul>My to-do list
   <li>item 1</li>
   <li>item 2</li>
   <li>item 3</li>
 </ul>
```
###\<ol>
-  ordered lists (aka numbered lists)

```
<ul>
   <li>One</li>
   <li>Dos</li>
   <li>Trois</li>
</ul>
```

###\<img>
- display an image
- must specify the `src` attribute
- self-closing element (no closing tag needed)

```
<img src="/path/fluffykittens.jpg">
```


###Including CSS with HTML
- In order to run external CSS, you need to link it to the HTML file. This usually goes in the `head` tag:

```
<link rel="stylesheet" href="/css/main.css">
```

- Including CSS internally:

```
 <head>
   <style>
     <!-- style rules here -->
     p{
     font-size: 36px;
     }
     
     h2{
     color: blue;
     }
     
   </style>
 </head
```

###Including Javascript with HTML
- put your javascript code between `<script>` tags at the end of your document, or...
- use the `src` attribute to specify an external file containing the javascript

```
 <script src="/path/to/app.js"></script>
```
<br>

##HTML Form Lab

1. Open `html_form/index.html`
2. For each comment denoted by <!-- --> replace the comment text with the correct HTML as per the instruction to create the form
3. Link to an external Google stylesheet in order to import a font-family.  Then change the font-family property in your CSS file to see the changes.
4. Use the autofocus attribute to place focus on the first input field when the page loads
4. Bonus: Use CSS to change the background color of the page. Experiment with using images as backgrounds as well.
5. Double Bonus: Review the CSS transition property documentation and try to create a small animation anywhere on the form. An example may be to highlight a border around a form field when it is clicked.

<br>


##DOM structure

A web page is structured like a tree

- Node/Branch
- Parent/Child relationships
- Demo Mozilla 3D viewer

<br>




##Cookie Recipe Lab

1. Open `day1/cookie_recipe_lab/cookie_recipe.html` in your Sublime Editor
2. Right-click the open file in Sublime and select `Open in Browser`
  - oops, needs some work
3. Use some of the tags we just learned about to make our recipe page more presentable
4. Reference [the docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference) as necessary
5. Bonus challenge
  - turn round bullet points into square bullet points

<br><br>




##CSS - Cascading Style Sheets

###Including with HTML
There are several different ways to incorporate CSS rules into your HTML file.  It is best practice to include them from an external `.css` file (first option below), so that will be our focus.

- External `.css` file
  - Include a `<link>` to the CSS file in your `<head>` tag


```
<link rel="stylesheet" href="path/to/main.css">
```

- Internal `<style>` tag
  - Rules go in the `<style>` tag, which goes in the `<head>` tag
  - The rules will only apply to this page

```
<head>
  <title>My Page</title>
  <style>
    <!-- CSS rules go here -->
  </style>
</head>
```

- Inline
  - Style settings can be applied directly to an element through the `style` attribute
  - Separate settings by a semicolon, include as many as you like
  - This approach should be used sparingly

```
 <div style="background-color:blue; font-size:12">
   <!-- content here will have a blue background and a font size of 12 -->
 </div>
```
<br>

###What is a stylesheet?
A stylesheet consists of a collection of style **rules**.  Each rule contains an arbitrary number of **declarations** (or property settings) and is targeted at elements in the page that are matched by the rule **selector(s)**.

<br>

![alt text](https://github.com/rycwilson/FEWD-UXDI-2day/blob/master/img/css_syntax.png?raw=true)

(Demo)

###"Cascading"
CSS rules can come from a number of different sources.  Like:

- Browser default settings (user-agent stylesheet)
- Developer settings (`.css` files linked to the HTML)
  - CSS frameworks (e.g. Bootstrap)
  - developer's own `.css` file(s)
- User settings
  - user can change the browser defaults

With all these sources, it is inevitable that settings will overlap and conflict with one another.  For two or more settings that apply to the same element, the browser has to decide which setting to apply.  This is the meaning of "cascading."

So how does the browser decide? ...  

###Selectors and Specificity
In order to create a CSS rule, we first have to select the element(s) it applies to.  There are A LOT of different ways to do this, some more **specific** than others.  This is the solution to the "cascading" problem.  The browser will examine all the rules that apply to a given element and **compute** which one is most specific.  In the event that two rules are equi-specific, the LAST one that was loaded into the browser will win.

**Tag** - Select all `<p>` elements

```
p {
  ...
}
```

**Class** - Select all elements with `class="my_class"`

```
.my_class {
  ...
}
```

**ID** - Select the element with `id="my_element"`  

- Obviously, you'll want to avoid giving two elements the same ID.

```
 #my_element {
   ...
 }
```


[Learn more](http://code.tutsplus.com/tutorials/the-30-css-selectors-you-must-memorize--net-16048)


###Selectors Exercise - Bento Box (20 mins)
[Have fun!](http://flukeout.github.io)

<br>


## CSS Properties

###The Box Model
Each HTML element in a web page is represented as a rectangular box. The box model describes the content of the space taken by an element. There are four essential edges in the model: margin, border, padding, and content.  The margin, border, and padding properties exist for ALL elements.  So let's start with those...

![alt text](https://github.com/rycwilson/FEWD-UXDI-2day/blob/master/img/box_model.png?raw=true)

###CSS Properties of the Box Model
- `margin`

```
 <!-- in order: top, right, bottom, left -->
 margin: 10px 5px 10px 5px;

 <!-- individual -->
 margin-top: 10px;
```
- `border`

```
 <!-- width, type, color -->
 border: 1px solid black

 <!-- individual -->
 border-top: 1px solid black;
```

- `padding` - similar to margin


####Other common CSS properties

...

##Advanced CSS
- Pseudo-classes
- Layout: Display and Position properties
- Responsive Design




