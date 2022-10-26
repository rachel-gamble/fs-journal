# Bootstrap

Bootstrap provides thousands of pre-written CSS code.
Think:

mb-6 - margin bottom 6

CONTAINERS + ROWS + COLUMNS

Use color and weight to create hierarchy instead of size

A common mistake when styling UI text is relying too much on font size to control your hierarchy.
“Is this text important? Let’s make it bigger.”
“Is this text secondary? Let’s make it smaller.”
Instead of leaving all of the heavy lifting to font size alone, try using color or font weight to do the same job.
“Is this text important? Let’s make it bolder.”
“Is this text secondary? Let’s use a lighter color.”

Try and stick to two or three colors:
A dark (but not black) color for primary content (like the headline of an article)
A grey for secondary content (like the date an article was published)
A lighter grey for ancillary content (maybe the copyright notice in a footer)

Two font weights is usually enough for UI work:
A normal font weight (400 or 500 depending on the font) for most text
A heavier font weight (600 or 700) for text you want to emphasize

Stay away from font weights under 400 for UI work; they can work for large headings but are too hard to read at smaller sizes. If you’re considering using a lighter weight to de-emphasize some text, use a lighter color or smaller font size instead.

Note: Don't use grey text on colored backgrounds, it is hard to read. Looks good on white background to de-emphasize.
Gray on white is *reduced contrast*
Making the text closer to the background color is what creates hierarchy, not making it light grey.

container-fluid - goes to the edges

think of containers as the big picture: your header, body, footer
rows: think of the smaller boxes; for example the title row, the logo row, the row with site navigation links, the video or text content rows, the bottom row of links, the row with cart, the bottom row with 


---------------------------
QUICK KEYS
---------------------------
col*x - where x equals the number of columns you want to quickly create. (col*3 creates 3 columns)
bs5-$ - provides bootstrap code in html; such as the HTML set up with bootstrap





affect mouse hover with css and html:

.select:hover {
    background-color: whitesmoke;
    cursor: pointer;
    transition: all 2.s linear;
}

<section class="row select" on click="window.close()"> - closes window 

col-sm-10 - makes small screens size 10
col-md-5 - makes medium screens size 5
  <div class="col-sm-10 col-md-5">

  good practice, to add 2 sizes for big and small screens
 <div class="col-12 col-md-7">

 if you want a flexbox, make a row.


 Making the text closer to the background color is what actually helps create hierarchy, not making it light grey.

 Two ways to reduce contrast when working with colorful backgrounds: 
 1. Reduce the opacity of the white text. Use white, lower the opacity. It lets the background bleed thru a little, de-emphasizing the text in a way that doesn't clash with the background.
 2. Hand-pick a color that is based on the background color. Works better than option 1 when the background is an image or pattern, or when reducing the opacity makes the text feel too dull or washed out. - choose a color that's the same hue as the background (adjust saturation and lightness)

-----BORDERS, SEPARATION, BOX SHADOW------
When you need to create separation between two elements, try to resist immediately reaching for a border.

While borders are a great way to distinguish two elements from one another, they aren’t the only way, and using too many of them can make your design feel busy and cluttered.

Instead use a:
box shadow
two different background colors
add extra spacing ('margin-bottom: 48px;')

Don't blow up icons that are meant to be small - it looks bad. (such as a small logo blown up 4x):
icon intended small size - 20px
icon intended for large sized - 48px
- if small is all you have, enclose them inside another shape and give the shape a background color.
- with a budget: buy premium icon set designed to be used at larger sized; like Heroicons or Iconic

Use accent borders to add color to a bland design:
'border-top: 6px solid #purple'

-----ACCENT BORDERS------
- side accent border colored
- highlight active navigation items (when hovored cect)
- across top of entire layout


--------BUTTONS------
Not all buttons need a background.
To make a background:

<button  type="button" class="btn btn-primary">Primary</button>
<button  type="button" class="btn btn-secondary">Secondary</button>
<button  type="button" class="btn btn-warning">Warning</button>

where the button class decides which color/button action you choose from your css.

---------------------------
-------hierarchy-----------
Every action on a page sits somewhere in a pyramid of importance. Most pages only have one true primary action, a couple of less important secondary actions, and a few seldom used tertiary actions.
when designing, communicate their place in the hierarchy.

Primary - actions should be obvious. Solid, high contrast background colors work great here.
Secondary - actions should be clear but not prominent. Outline styles or lower contrast background colors are great options.
Tertiary - actions should be discoverable but unobtrusive. Styling these actions like links is usually the best approach.

If a destructive action isn’t the primary action on the page, it might be better to give it a secondary or tertiary button treatment rather than make it a red delete button.






