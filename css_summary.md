# topics 

## define css
**css** stands for Cascading Style Sheets , used to describe the presentation of a document written in HTML or XML (including XML dialects such as SVG, MathML or XHTML)
, CSS is not a programming language. It's not a markup language either. CSS is a style sheet language


![css syntax](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics/css-declaration-small.png)
|Selector name|What does it select|Example|
|-------------|-------------------|-------|
|UNIVERSAL SELECTORS| Rather than selecting elements of a specific type, the universal selector quite simply matches the name of any element type| ` * {    color: #000000;  }`|
|Element selector (sometimes called a tag or type selector)|All HTML elements of the specified type.| `p` selects `<p>`|
|ID selector|The element on the page with the specified ID. On a given HTML page, each id value should be unique.|`my_id` selects `<p id="my_id">`|
|Class selector	|The element(s) on the page with the specified attribute.| `img[srs]` selects `<img src="project\image.jpg">`|
|DESCENDANT SELECTORS "combinator"|Suppose you want to apply a style rule to a particular element only when it lies inside a particular element. As given in the following example, the style rule will apply to the em element only when it lies inside the ul tag.|`ul em { color: #000000; }`|
|Pseudo-class selector|The specified element(s), but only when in the specified state. (For example, when a cursor hovers over a link.	| `a:hover` selects `<a>` but only when the mouse hovers over the link|
|GROUPING SELECTORS| If you have elements with the same style definitions|`h1, h2, p { text-align: center;  color: red;`}
|Child Selector (>)|The child selector selects all elements that are the children of a specified element.|`div > p {background-color: yellow;}`|  
|Adjacent Sibling Selector (+)| used to select an element that is directly after another specific element.|`div + p { background-color: yellow;}`|   
|General Sibling Selector (~)|selects all elements that are next siblings of a specified element.|`div ~ p {background-color: yellow;}`|


### There are three types of CSS which are given below:
- **Inline** : Inline CSS contains the CSS property in the body section attached with the element known as inline CSS.
- **Internal or Embedded** : The CSS ruleset should be within the HTML file in the head section i.e the CSS is embedded within the HTML file. 
- **External** : External CSS contains a separate CSS file that contains only style property with the help of tag attributes.
 
### Cascading Order 
1-Inline style (inside an HTML element). <br/>
2-External and internal style sheets (in the head section).<br/>
3-Browser default.<br/>


## phase 1

### link css
- how to link the external style sheet to your html web page :  <br/>
`<link href="style.css" rel="stylesheet" type="text/css">`
<br/>
### comments in css <br/>
`/* this is a comment */`

### colors in css <br/>
- rgb (red , green , blue)
- rgba (red , green , blue , alpha)
- hsl (hue , saturation , lightness)
- hsla (hue, saturation, lightness, alpha)
- hexa color 
<br/>

### CSS background properties:
- `background-color : color ;`.
Opacity / Transparency
-  `Opacity : 0.3;` takes values from 0 to 1.
-  ` background-image: url("paper.gif");`.
-  `background-repeat: repeat-x;` other values : `repeat` `repeat-y` `repeat-x` `no-repeat` .
- `background-position: top right ;` other values : `top` `right` `left` `bottom` `center` `x% y%` ` 30px 60px`.
- ` background-attachment: fixed;` other values : `scroll` `local`.
background - Shorthand property
- ` background: #ffffff url("img_tree.png") no-repeat fixed right top;` the order of property values : `background-color` `background-image` `background-repeat` `background-attachment` `background-position`.
- `background-size: cover;` other values : `cover` `50%` `150px` `auto` .


### CSS Borders
- `border-style :none;` other values : `dotted` `dashed` `solid` `groove` `double` `ridge` `inset` `outset` `hidden`.
in case of one value : the whole border takes this styling.
in case of two values : first> top&bottom , second> right&left.
in case of three values : first> top , second> right&left , third> bottom.
in case of four values : first>top , second >right , third>bottom , fourth>left .
- ` border-width: 5px;` other values : `thin` `thick` `medium` .
- `border-color: red;` , `border-color: red green blue yellow;` red>top , green>right , blue>bottom , yellow >left.
CSS Border - Shorthand Property
- ` border: 5px solid red;` the order of property value : `border-width` , `border-style` , `border-color`
- ` border-radius: 5px;` for rounded edges .


### Margin 
used to create space around elements, outside of any defined borders.<br/>
Individual Sides:<br/>
- `margin-top`.
- `margin-right`.
- `margin-bottom`.
- `margin-left`. <br/>
All the margin properties can have the following values:<br/>
- `auto` -the browser calculates the margin.
- `length` -specifies a margin in px, pt, cm, etc.
- `%` -specifies a margin in % of the width of the containing element.
- `inherit` -specifies that the margin should be inherited from the parent element.
<br/>
**Margin - Shorthand Property** : <br/>

- `margin: 25px 50px 75px 100px;` the order of property value : `margin-top` `margin-right` `margin-bottom` `margin-left`.

- `margin: 25px 50px` top & bottom.

- `margin: 25px 50px 75px` top , right&left , bottom. <br/>

**Margin Collapse:** <br/>
Top and bottom margins of elements are sometimes **collapsed** into a **single margin** that is equal to the largest of the two margins.
This does not happen on left and right margins! Only top and bottom margins! <br/>
example : <br/>
```
h1 {
  margin: 0 0 50px 0;
}

h2 {
  margin: 20px 0 0 0;
}
```
### CSS Padding
used to create space around an element's content, inside of any defined borders. <br/> <br/>
**Padding - Individual Sides** : <br/>
`padding-top` ,
`padding-right` ,
`padding-bottom`, 
`padding-left`.
<br/>
All the padding properties can have the following values:
- `length` specifies a padding in px, pt, cm, etc.
- `%` specifies a padding in % of the width of the containing element.
- `inherit` specifies that the padding should be inherited from the parent element .
<br/>

**Padding - Shorthand Property** :

specify the values for the following properties : `padding-top` , `padding-right` , `padding-bottom` , `padding-left` . <br/>

**CSS Height, Width, min-width & Max-width**

used to set the maximum width of an element, very usefull if we want a responsive design . <br/>

**CSS height and width Values** : 
- `auto` This is default. The browser calculates the height and width.
- `%` Defines the height/width in percent of the containing block.
- `initial` Sets the height/width to its default value.
- `length`  Defines the height/width in px, cm, etc.
- `inherit` The height/width will be inherited from its parent value. <br/>


### CSS Box Model

![CSS_Box_Model](https://th.bing.com/th/id/OIP.dJuai1RcRybMuLjV93dw8AAAAA?pid=ImgDet&rs=1) 

- **Content** : The content of the box, where text and images appear .
- **Padding** : Clears an area around the content. The padding is transparent.
- **Border** :  A border that goes around the padding and content .
- **Margin** : Clears an area outside the border. The margin is transparent .

> **Important** : When you set the width and height properties of an element with CSS , you just set the width and height of the content area. To calculate the full size of an element, you must also add padding, borders and margins.
Example :
``` 
div {
  width: 320px;
  padding: 10px;
  border: 5px solid gray;
  margin: 0;
}
``` 
the calculation : <br/>
> 320px (width)+ 20px (left + right padding)+ 10px (left + right border)+ 0px (left + right margin) = 350px
<br/>

### CSS outline

```
p {
  border: 2px solid black;
  outline: #4CAF50 solid 10px;
  margin: auto;  
  padding: 20px;
  text-align: center;
}
```
CSS has the following outline properties: <br/>
- `outline-style` 
- `outline-color`
- `outline-width`
- `outline-offset`
- `outline`

> outline-style ,  outline-width , outline-color, property has the same values that border propery takes .

**CSS Outline - Shorthand property**
a shorthand property for setting the following individual outline properties:
<br/>
- `outline-width`
- `outline-style` (required)
- `outline-color`
**CSS Outline Offset :**
adds space between an outline and the edge/border of an element.

### CSS Text

**Text Color** :
- `color` for coloring the text.
-  `background-color` for coloring the background of the text.

**CSS Text Alignment** :
- `text-align` used to set the horizontal alignment of a text `left` or `right` `aligned` , `centered`, or `justified`.

**Text Decoration** :
- `text-decoration-line`
- `text-decoration-style`
- `text-decoration-thickness`
- `text-decoration`

> `text-decoration-line` property is used to add a decoration line to text.
values : `overline` , `line-through` , `underline` 

> `text-decoration-style` property is used to set the style of the decoration line.
values : same as broder property's values.

> `text-decoration-thickness` property is used to set the thickness of the decoration line.
values : by px , em , pt etc

> `text-decoration` Sets all the text-decoration properties in one declaration
values : (best practise) `none` . <br/>

**CSS Text Transformation** 
 used to specify uppercase and lowercase letters in a text. <br/>
 Example:
 ```
 p.uppercase {
  text-transform: uppercase;
}

p.lowercase {
  text-transform: lowercase;
}

p.capitalize {
  text-transform: capitalize;
}
```

**CSS Text Spacing** :

- `text-indent`
 used to specify the indentation of the first line of a text 
 ```
 p {
  text-indent: 50px;
}
```
- `letter-spacing` letter-spacing property is used to specify the space between the characters in a text.
```
h1 {
  letter-spacing: 5px;
}
h2 {
  letter-spacing: -2px;
}
```

- `line-height`line-height property is used to specify the space between lines
```
p.small {
  line-height: 0.8;
}
```
- `word-spacing` word-spacing property is used to specify the space between the words in a text.
```
p.one {
  word-spacing: 10px;
}

```
- `white-space` white-space property specifies how white-space inside an element is handled.
```
p {
  white-space: nowrap;
}
```
### Text Shadow
In its simplest use, you only specify the horizontal shadow and the vertical shadow.
```
h1 {
  text-shadow: 2px 2px;
}
```
add a color (red) to the shadow:
```
h1 {
  text-shadow: 2px 2px red;
}
```
add a blur effect (5px) to the shadow:
```
h1 {
  text-shadow: 2px 2px 5px red;
}
```
### CSS Fonts
`font-family` property to specify the font of a text. <br/>
```
.p1 {
  font-family: "Times New Roman", Times, serif;
}

.p2 {
  font-family: Arial, Helvetica, sans-serif;
}

.p3 {
  font-family: "Lucida Console", "Courier New", monospace;
}
```

> Fallback Fonts : add a list of similar "backup fonts" in the font-family property. If the first font does not work, the browser will try the next one, and the next one, and so on.

**Font Style** :
```
p.normal {
  font-style: normal;
}

p.italic {
  font-style: italic;
}

p.oblique {
  font-style: oblique;
}
```
**Font weight** : specifies the weight of a font
```
p{
  font-weight: 700;
}
```
**CSS Font Size** :
```
h2 {
  font-size: 30px;
}

p {
  font-size: 14px;
}
```
> EM = time , this value tells the brower to inherit the mean value from the parent ; ex : the parent font size is 20 px , then 1em to the child equals 20 px , 2em equals 40px and so on .
>NOTE: the root element (html) defalut font size is 16px , so the defalut value for any element inside the root has a 1em=16px value , unless it's a DESCENDANT element

**Font Size With Em** :
```
h2 {
  font-size: 1.875em; /* 30px/16=1.875em */
}

p {
  font-size: 0.875em; /* 14px/16=0.875em */
}
```
### CSS Google Fonts
**Example**
```
<head>
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia">
<style>
body {
  font-family: "Sofia", sans-serif;
}
</style>
</head>
```
**Font shorthand  Property** 
 shorthand property for :
- `font-style`
- `font-variant`
- `font-weight`
- `font-size/line-height`
- `font-family`
```
p.a {
  font: 20px Arial, sans-serif;
}
p.b {
  font: italic small-caps bold 12px/30px Georgia, serif;
}
```
### how to pair with google fonts
1- search for **google fonts**.<br/>
![google fonts](https://i.pinimg.com/originals/4a/2c/67/4a2c675940f228403abc2d9dc021d96a.png)

2- choose the font you want then copy the link element to your project
![google fonts](https://static.tildacdn.com/tild3461-3032-4734-a563-616266336264/Screenshot__2020-12-.png)
3- then choose import and copy the code to your stylesheet .<br/>
4- copy the css code and put it in universal selector to add the font family to the whole project .<br/>

### Font Awesome Icons
```
<!DOCTYPE html>
<html>
<head>
<script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</head>
<body>

<i class="fas fa-cloud"></i>
<i class="fas fa-heart"></i>
<i class="fas fa-car"></i>
<i class="fas fa-file"></i>
<i class="fas fa-bars"></i>

</body>
</html>
```
**tutorial for adding icons** : <br/>
1- go to [font awesome](https://fontawesome.com/) .<br/>
2- click start for free .<br/>
3- choose the icon you desire . <br/>
4- copy the code to you stylesheet .<br/>
### CSS Links
```
a {
  color: hotpink;
}
```
> links can be styled differently depending on what state they are in.

The four links states are:

- `a:link` a normal, unvisited link
- `a:visited` a link the user has visited
- `a:hover` a link when the user mouses over it
- `a:active` a link the moment it is clicked

```
/* unvisited link */
a:link {
  color: red;
}

/* visited link */
a:visited {
  color: green;
}

/* mouse over link */
a:hover {
  color: hotpink;
}

/* selected link */
a:active {
  color: blue;
}
```
> a:hover MUST come after a:link and a:visited ,a:active MUST come after a:hover.

### CSS Lists

**Different List Item Markers** : 
```
ul.a {
  list-style-type: circle;
}
ul.b {
  list-style-type: square;
}
ol.c {
  list-style-type: upper-roman;
}
ol.d {
  list-style-type: lower-alpha;
}
```
`list-style-image` property specifies an image as the list item marker . <br/>
```
ul {
  list-style-image: url('sqpurple.gif');
}
```
`list-style-position` property specifies the position of the list-item markers (bullet points).
>`list-style-position: outside;` means that the bullet points will be outside the list item. The start of each line of a list item will be aligned vertically. This is default check [list styling](https://www.w3schools.com/Css/css_list.asp) <br/> 
>`list-style-position: inside;` means that the bullet points will be inside the list item. As it is part of the list item, it will be part of the text and push the text at the start. 
<br/>

**Remove Default Settings** : <br/>

```
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
```

### CSS Tables 

**Table Borders** : <br/>
Example : 
```
table, th, td {
  border: 1px solid;
}
```
**Collapse Table Borders** : <br/>
`border-collapse` property sets whether the table borders should be collapsed into a single border.
```
table {
  border-collapse: collapse;
}
```
**Horizontal Alignment**
```
td {
  text-align: center;
}
```
**Vertical Alignment**
```
td {
  height: 50px;
  vertical-align: bottom;
}
```
**Horizontal Dividers** 
```
th, td {
  border-bottom: 1px solid #ddd;
}
```
**Hoverable Table**
```
tr:hover {background-color: coral;}
```
**Striped Tables** <br/>
for zebra-striped tables, use the `nth-child()` selector and add a `background-color` to all even (or odd) table rows. 
```
tr:nth-child(even) {background-color: #f2f2f2;}
```

### CSS Layout - The display Property
> Every HTML element has a default display value depending on what type of element it is. The default display value for most elements is block or inline.

**Block-level Elements** : <br/>
> A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).
Examples of block-level elements: <br/>
- `<div>`
-  `<h1>`, `<h6>`
- `<p>`
- `<form>`
- `<header>`
- `<footer>`
- `<section>`

**Inline Elements** :
> An inline element does not start on a new line and only takes up as much width as necessary.
Examples of inline elements: <br/>

- `<span>`
- `<a>`
- `<img>`

**flex box** 
> `display: none;` is commonly used with JavaScript to hide and show elements without deleting and recreating them. Take a look at our last example on this page if you want to know how this can be achieved.The `<script>` element uses `display: none;` as default. 

>Notice that when the `flex direction` is a column, `justify-content` changes to the vertical and `align-items` to the horizontal.

>Sometimes reversing the row or column order of a container is not enough. In these cases, we can apply the `order` property to individual items. By default, items have a value of 0, but we can use this property to also set it to a positive or negative integer value (-2, -1, 0, 1, 2). NOTE that the start of any block is 0

>Another property you can apply to individual items is `align-self`. This property accepts the same values as align-items and its value for the specific item.

>This can be confusing, but `align-content` determines the spacing between lines, while align-items determines how the items as a whole are aligned within the container. When there is only one line, align-content has no effect.

**Hide an Element - display:none or visibility:hidden?** : <br/>
> Hiding an element can be done by setting the display property to none. The element will be hidden, and the page will be displayed as if the element is not there
```
h1.hidden {
  display: none;
}
```
> `visibility:hidden;` also hides an element. However, the element will still take up the same space as before. The element will be hidden, but still affect the lay
```
h1.hidden {
  visibility: hidden;
}
```

### CSS Calculation
```
p{
width : calc(((100%-60))/4);
margin-left: 15px;
}
/*
space 15px
total boxes = 4 , total spaces = 4*15=60px
margin-left : 15px
box width = ((100%-60))/4

*/
```
### CSS Layout - The position Property 
position property specifies the type of positioning method used for an element (static, relative, fixed, absolute or sticky). <br/>

- `static`
- `relative`
- `fixed`
- `absolute`
- `sticky`
> Elements are then positioned using the `top`, `bottom`, `left`, and `righ`t properties. However, these properties will not work unless the position property is set first.

> `position: static;` is not positioned in any special way; it is always positioned according to the normal flow of the page,HTML elements are positioned static by default.

> `position: relative;` is positioned relative to its normal position.Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element

> `position: fixed;` is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The top, right, bottom, and left properties are used to position the element.

> `position: sticky;` is positioned based on the user's scroll position. A sticky element toggles between relative and fixed, depending on the scroll position. It is positioned relative until a given  <br/>offset position is met in the viewport - then it "sticks" in place (like position:fixed).

### CSS Layout - The z-index Property
`z-index` property specifies the stack order of an element. <br/>
Example :
```
img {
  position: absolute;
  left: 0px;
  top: 0px;
  z-index: -1;
}
```
> Note: `z-index` only works on positioned elements ( `position: absolute` , `position: relative` , `position: fixed` , or `position: sticky` ) and flex items (elements that are direct children of `display: flex;` elements).

> If two positioned elements overlap each other without a z-index specified, the element defined last in the HTML code will be shown on top

### CSS Layout - Overflow
 `overflow` property controls what happens to content that is too big to fit into an area. <br/>
 
  overflow property has the following values:

- `visible`  Default. The overflow is not clipped. The content renders outside the element's box
- `hidden` The overflow is clipped, and the rest of the content will be invisible
- `scroll` The overflow is clipped, and a scrollbar is added to see the rest of the content
- `auto` Similar to scroll, but it adds scrollbars only when necessary

> Note: The overflow property only works for block elements with a specified height.

**overflow-x and overflow-y** <br/>
- `overflow-x` specifies what to do with the left/right edges of the content.
- `overflow-y` specifies what to do with the top/bottom edges of the content.

**CSS overflow-wrap Property**
```
div.a {
  overflow-wrap: normal;
}

div.b {
  overflow-wrap: break-word;
}

div.c {
  overflow-wrap: anywhere;
}
```

### CSS Layout - display: inline-block
> Compared to `display: inline;` the major difference is that `display: inline-block;` allows to set a width and height on the element.

> with `display: inline-block;` the top and bottom margins/paddings are respected, but with `display: inline;` they are not.

> Compared to `display: block;` the major difference is that `display: inline-block;` does not add a line-break after the element, so the element can sit next to other elements.

### CSS Pseudo-classes
> A pseudo-class is used to define a special state of an element.

For example, it can be used to:

- Style an element when a user mouses over it
- Style visited and unvisited links differently
- Style an element when it gets focus

**The syntax of pseudo-classes:**
```
selector:pseudo-class {
  property: value;
}
```
**Anchor Pseudo-classes**
```
/* unvisited link */
a:link {
  color: #FF0000;
}

/* visited link */
a:visited {
  color: #00FF00;
}

/* mouse over link */
a:hover {
  color: #FF00FF;
}

/* selected link */
a:active {
  color: #0000FF;
}
```
> Note: a:hover MUST come after a:link and a:visited in the CSS definition in order to be effective! a:active MUST come after a:hover in the CSS definition in order to be effective! Pseudo-class names are not case-sensitive.

**Pseudo-classes and HTML Classes**
```
a.highlight:hover {
  color: #ff0000;
}
```
**CSS - The :first-child Pseudo-class**
```
p:first-child {
  color: blue;
}
```
**CSS - The :lang Pseudo-class**
The `lang`pseudo-class allows you to define special rules for different languages.
In the example below, `lang`defines the quotation marks for <q> elements with lang="no":
 ```
 <html>
<head>
<style>
q:lang(no) {
  quotes: "~" "~";
}
</style>
</head>
<body>

<p>Some text <q lang="no">A quote in a paragraph</q> Some text.</p>

</body>
</html>
 ```
### CSS Pseudo-elements
 **Syntax**
 ```
 selector::pseudo-element {
  property: value;
}
 ```
 > Notice the double colon notation - ::first-line versus :first-line , The double colon replaced the single-colon notation for pseudo-elements in CSS3. This was an attempt from W3C to distinguish between pseudo-classes and pseudo-elements.
 
 **CSS - The ::before Pseudo-element**
 The `::before` pseudo-element can be used to insert some content before the content of an element.
 
 ```
 h1::before {
  content: url(smiley.gif);
}
 ```
 **CSS - The ::after Pseudo-element**
 The ::after pseudo-element can be used to insert some content after the content of an element.
 
 ```
 h1::after {
  content: url(smiley.gif);
}
 ```
 **CSS - The ::marker Pseudo-element**
 The `::marker` pseudo-element selects the markers of list items.
 ```
 ::marker {
  color: red;
  font-size: 23px;
}
 ```
 **CSS - The ::selection Pseudo-element**
 The `::selection` pseudo-element matches the portion of an element that is selected by a user.
 ```
 ::selection {
  color: red;
  background: yellow;
}
 ```
 ### vendor prefixes
 to use a feature added to the web development toolkit & that feature is not fully supported we use <br/>
 `-webkit-` and that's for : chrome , safari , new opera , version 
 `-moz-` for firefox
 `-ms-` for ie , edge
 `-o-` for old versions of opera
 
 ### CSS Dropdowns
 Create a dropdown box that appears when the user moves the mouse over an element.
 ```
 <style>
.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  padding: 12px 16px;
  z-index: 1;
}

.dropdown:hover .dropdown-content {
  display: block;
}
</style>

<div class="dropdown">
  <span>Mouse over me</span>
  <div class="dropdown-content">
    <p>Hello World!</p>
  </div>
</div>
 ```
 **Dropdown Menu**
Create a dropdown menu that allows the user to choose an option from a list.
 ```
 <style>
/* Style The Dropdown Button */
.dropbtn {
  background-color: #4CAF50;
  color: white;
  padding: 16px;
  font-size: 16px;
  border: none;
  cursor: pointer;
}

/* The container <div> - needed to position the dropdown content */
.dropdown {
  position: relative;
  display: inline-block;
}

/* Dropdown Content (Hidden by Default) */
.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}

/* Links inside the dropdown */
.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

/* Change color of dropdown links on hover */
.dropdown-content a:hover {background-color: #f1f1f1}

/* Show the dropdown menu on hover */
.dropdown:hover .dropdown-content {
  display: block;
}

/* Change the background color of the dropdown button when the dropdown content is shown */
.dropdown:hover .dropbtn {
  background-color: #3e8e41;
}
</style>

<div class="dropdown">
  <button class="dropbtn">Dropdown</button>
  <div class="dropdown-content">
    <a href="#">Link 1</a>
    <a href="#">Link 2</a>
    <a href="#">Link 3</a>
  </div>
</div>
  ```
  
  
  ### CSS Navigation Bar
  ### CSS Dropdowns
  ### CSS Image Gallery
  ### CSS Image Sprites
  ### CSS Attribute Selectors
  ### CSS Forms
  ### CSS Counters
  ### CSS Website Layout
  ### CSS Units
  ### CSS Specificity
  ### CSS The !important Rule
  ### CSS Math Functions
  
 
## phase 2
  ## CSS advanced
  
  ### CSS Rounded Corners
  ### CSS Border Images
  ### CSS Multiple Backgrounds
  ### CSS Colors
  ### CSS Color Keywords
  ### CSS Gradients
  ### CSS Radial Gradients
  ### CSS Conic Gradients
  ### CSS Shadow Effects
  
  
  ### CSS Box Shadow
  The CSS `box-shadow` property is used to apply one or more shadows to an element.
  
  Specify a Horizontal and a Vertical Shadow
  ```
  div {
  box-shadow: 10px 10px ;
}
  ```
  
  Specify a Color for the Shadow
  ```
 div {
  box-shadow: 10px 10px lightblue;
}
 ```
  
  Add a Blur Effect to the Shadow
  ```
  div {
  box-shadow: 10px 10px 5px lightblue;
}
  ```
  
  Set the Spread Radius of the Shadow
  ```
  div {
  box-shadow: 10px 10px 5px 12px lightblue;
   }
  ```
  > inset & outset better be controlled from the browser
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  ### CSS Text Effects
  ### CSS Web Fonts
  ### CSS 2D Transforms
  ### CSS 3D Transforms
  
  
  
  
  ### CSS Transitions
  CSS transitions allows you to change property values smoothly, over a given duration.
  
  
  
  ### CSS Animations
  ### CSS Tooltip
  ### CSS Styling Images
  ### CSS Image Reflection
  ### CSS The object-fit Property
  ### CSS The object-position Property
  ### CSS Masking
  ### CSS Buttons
  ### CSS Pagination Examples
  ### CSS Multiple Columns
  ### CSS User Interface
  ### CSS Variables - The var() Function
  ### CSS Overriding Variables
  ### CSS Change Variables With JavaScript
  ### CSS Using Variables in Media Queries
  
  
  ### CSS Box Sizing
  The CSS `box-sizing` property allows us to include the padding and border in an element's total width and height. <br/>
  **By default, the width and height of an element is calculated like this:**
>width + padding + border = actual width of an element
>height + padding + border = actual height of an element
  
  **`box-sizing property` allows us to include the padding and border in an element's total width and height**
  ```
  .div1 {
  width: 300px;
  height: 100px;
  border: 1px solid blue;
  box-sizing: border-box;
}
  ```
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  ### CSS Media Queries
  ### CSS Media Queries
  ### CSS Flexbox
  ### CSS Flex Container
  ### CSS Flex Items
  ### CSS Flex Items
  
  
  ### CSS Grid Layout Module
  
  ### CSS Grid Container
  ### CSS Grid Item

  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
## phase 3

