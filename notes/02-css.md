# CSS

the S in the SOLID principles - Single Responsibility. Our index.html is responsible for content and our style.css is responsible for how that content is presented. Our code is now easier to read and maintain resulting in quicker debugging and less bugs overall.
Selectors are how you pick which element to apply styles to.

selector {
  property: value;
}
=
body {
  background: #f60;
}

/--!SECTION: SELECTOR {}

When a selector is just a name without any punctuation marks or symbols, eg., ., #, [], then the rule is applied to any elements on the DOM with that tagName. 
In the above example we see that we are setting the background of our website to be the color orange. This is because the selector is targeting the <body> tag and all of our content is rendered within that tag.

example	-  every element with the tagName "example"
.example	-  every element with "example" in their classList
#example	-  the element with the id "example"
[required]	-  every element with the attribute `required` present - utilizing []'s is commonly combined with additional selectors eg., `.username[required]`
[href="#"]	every element with a `href` attribute whose value is "#"
example:hover	the element with the tagName "example" that is also at that same time being hovered over
- this is an example of a `pseudo-selector`
and more...	css diner

Just as selectors are used to specify which elements to target, properties are used to specify how to modify the presentation of the targeted element. In our example above we see that the background of the body is being modified, namely the background is being set to orange.

/--!SECTION: COMMON PROPERTIES
Common Properties:
color - font/text
background - 	background presentation eg., color, gradient, image, etc. this property has overloads available determined by number of values provided
height x width - these two properties set the size of the element
margin x padding - space between edge of element and border, and edge of border and content respectively (these property have overloads available determined by number of values provided)
display x position - how and where the element should be rendered and if it is or isn't part of the default render process

/--!SECTION: VALUE /
After targeting both the element and the property of the element to modify, we use values to specify exactly how to modify the presentation. In the example above we see that the value used was #f60. This is the hexcode value for the color orange. In this specific example we could have used other units of color to assign the presentation of the background, eg., rgba, name of the color, linear-gradient, etc.
inherit, auto, initial, unset, none
Some properties, like background and margin for example, allow for a variable amount of values to be assigned. This is overloading. Let’s look at a specific example with margin:
UNITS:
----------- Relative Lengths
px - pixels (1px = 1/96th of 1in)
em - Relative to the font-size of the element (2em means 2 times the size of the current font)
rem - Relative to font-size of the root element
vh - Relative to 1% of the height of the viewport*
vw - Relative to 1% of the width of the viewport*
% - Relative to the parent element
-----------
ex - Relative to the x-height of the current font (rarely used)
ch - Relative to the width of the "0" (zero)
vmin - Relative to 1% of viewport's* smaller dimension
vmax - relative to 1% of viewport's* larger dimension
----------- Absolute Length
cm	centimeters
mm	millimeters
in	inches (1in = 96px = 2.54cm)
px *	pixels (1px = 1/96th of 1in)
pt	points (1pt = 1/72 of 1in)
pc	picas (1pc = 12 pt)
-----------
10px - 10 px of space applied to every side of the element
10px 5px - 10 px of space applied to the top and bottom and 5px of space applied to the left and right
10 px 3px 5px - 10px of space applied to the top, 3px applied to the right and left, 5px applied to bottom
10px 3px 0px 5px - 10px of space applied to the top, 3px applied to the right, 0px applied to the bottom, 5px applied to the left

Tip: The em and rem units are practical in creating perfectly scalable layout!
* Viewport = the browser window size. If the viewport is 50cm wide, 1vw = 0.5cm.


Common Units for Values:
spacial - px, em, rem, vh, vw, %;. Pixels are the least responsive of the units listed
color - literal name of the color, hex-code, rgba, linear-gradient
background - same units as color plus, url(), blur(), and others

/!SECTION: CSS SPECIFICITY
one rule to rule them all
Specificity is built into css to determine which rule should be applied in the chance that multiple rules are targeting both the same element and property on that element, but assigning different values.

specificity overrules load order

selector: example: value:
tagName - span - 1
class - .title - 100
attributes - [required] - 10
some pseudo-elements - :after & :before - 1
other ppsuedo-elements - :hover - 10px

------example:
div.box {
  background: purple;
}

.box {
  background: red;
}

div {
  background: green;
}
-------!SECTION now the box is purple. It's specific.
We remember that tagName selectors are worth 1 and that class selectors are worth 10, so a selector that includes both a tagName and a class is worth 11! Every individual selector thats combined to target an element adds their value to the cummulative value for the complex selector.

“Though technically !important has nothing to do with specificity, it interacts directly with it. When an important rule is used on a style declaration, this declaration overrides any other declarations.” - MDN

In like manner inline-style always overwrite any styles in external stylesheets (except !important’s).

Both of these avenues for styling are bad practices and should in almost all cases be avoided. You need to know about them, but that doesn’t mean you should use them.


LISTS
<ol> - Ordered List, or Numbered List (ex: 1. Aries, 2. Taurus)
    <ol><li>1. Aries</li><li>2. Taurus</ol>
<ul> -Unordered List, or Bulleted List
    <ul><li>1. Aries</li><li>2. Taurus</ul> (*Aries, *Taurus,)
<dl> - Description List, or Definition List
    <dl> tag defines the start of the list.
    <dt> tag defines a term.
    <dd> tag defines the term definition (description).
    example:
    <dl>
        <dt>Aries</dt>
            <dd>The First Sign.</dd>
        <dt>Taurus</dt>
            <dd>The Second Sign.</dd>
    </dl>
    output:
    Aries
        -The First Sign.
    Taurus
        -The Second Sign.


/!SECTION: FLEXBOX

When working with flexbox you need to think in terms of two axes — the main axis and the cross axis. 
The **main axis** is defined by flex-direction, which has four possible values:

row - your main axis will run along the row in the inline direction.
row-reverse - your main axis will run along the row in the inline direction.
column - Choose column or column-reverse and your main axis will run from the top of the page to the bottom — in the block direction.
column-reverse - Choose column or column-reverse and your main axis will run from the top of the page to the bottom — in the block direction.

The **cross axis** runs perpendicular to the main axis, therefore if your flex-direction (main axis) is set to row or row-reverse the cross axis runs down the columns. (up or down)
If your main axis is column or column-reverse then the cross axis runs along the rows. (LEFT OR RIGHT)

If the flex-direction is row and I am working in English, then the start edge of the main axis will be on the left, the end edge on the right.

The flex container
An area of a document laid out using flexbox is called a flex container. To create a flex container, we set the value of the area's container's display property to flex or inline-flex. As soon as we do this the direct children of that container become flex items. As with all properties in CSS, some initial values are defined, so when creating a flex container all of the contained flex items will behave in the following way.

Items display in a row (the flex-direction property's default is row).
The items start from the start edge of the main axis.
The items do not stretch on the main dimension, but can shrink.
The items will stretch to fill the size of the cross axis.
The flex-basis property is set to auto.
The flex-wrap property is set to nowrap.

The result of this is that your items will all line up in a row, using the size of the content as their size in the main axis. If there are more items than can fit in the container, they will not wrap but will instead overflow. If some items are taller than others, all items will stretch along the cross axis to fill its full size.

If we change flex-direction to column the main axis switches and our items now display in a column. Set column-reverse and the start and end lines are again switched.

   .box {
          display: flex;
          flex-direction: row-reverse;
        }

The live example below has flex-direction set to row-reverse. Try the other values — row, column and column-reverse — to see what happens to the content.

To make it wrap to the next line:

      .box {
        display: flex;
        flex-wrap: wrap;
    }

.box {
  display: flex;
  flex-flow: row wrap;
  }

  flex-grow
flex-shrink
flex-basis

         .box {
            display: flex;
            align-items: flex-start;
          }


          Try the following values of justify-content in the live example:

/!SECTION --------LINK - JUSTIFY CONTENT

justify-content - property is used to align the items on the main axis, the direction in which 'flex-direction' has set the flow.

flex-start - The initial value, which will line the items up at the start edge of the container
flex-end - to line them up at the end, or center to line them up in the center.
center - line content up in the center
space-around - cause an equal amount of space on the right and left of each item use the value 
space-between - take all the spare space after the items have been laid out, and share it out evenly between the items so there will be an equal amount of space between each item. With space-around, items have a half-size space on either end.
space-evenly - to cause items to have equal space around them use the value space-evenly. With space-evenly, items have a full-size space on either end.

example: makes the list of items spaced out equally in one line.
          .box {
            display: flex;
            justify-content: space-evenly;
          }
                  <div class="box">
          <div>One</div>
          <div>Two</div>
          <div>Three</div>
        </div>