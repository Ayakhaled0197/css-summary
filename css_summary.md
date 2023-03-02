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
 
**CSS Outline** 

```
p {
  border: 2px solid black;
  outline: #4CAF50 solid 10px;
  margin: auto;  
  padding: 20px;
  text-align: center;
}
```




## phase 2
## phase 3
