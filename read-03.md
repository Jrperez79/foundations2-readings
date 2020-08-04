# Reading 03

## Shay Howe's intro to RWD
With the growth in mobile Internet usage comes the question of how to build websites suitable for all users. The industry response to this question has become responsive web design, also known as RWD.

Responsive web design is the practice of building a website suitable to work on every device and every screen size, no matter how large or small, mobile or desktop.

Responsive and adaptive web design are closely related, and often transposed as one in the same. Responsive generally means to react quickly and positively to any change, while adaptive means to be easily modified for a new purpose or situation, such as change. 

Mobile, on the other hand, generally means to build a separate website commonly on a new domain solely for mobile users. While this does occasionally have its place, it normally isn’t a great idea. Mobile websites can be extremely light but they do come with the dependencies of a new code base and browser sniffing, all of which can become an obstacle for both developers and users.

### Flexible Layouts
Responsive web design is broken down into three main components, including flexible layouts, media queries, and flexible media. The first part, flexible layouts, is the practice of building the layout of a website with a flexible grid, capable of dynamically resizing to any width. Flexible grids are built using relative length units, most commonly percentages or em units. These relative lengths are then used to declare common grid property values such as width, margin, or padding.

Flexible layouts do not advocate the use of fixed measurement units, such as pixels or inches. Reason being, the viewport height and width continually change from device to device. Website layouts need to adapt to this change and fixed values have too many constraints.

### Flexible Grid
Using the flexible grid formula we can take all of the fixed units of length and turn them into relative units.

The flexible layout approach alone isn’t enough. At times the width of a browser viewport may be so small that even scaling the the layout proportionally will create columns that are too small to effectively display content. Specifically, when the layout gets too small, or too large, text may become illegible and the layout may begin to break. In this event, media queries can be used to help build a better experience.

### Media Queries
Media queries were built as an extension to media types commonly found when targeting and including styles. Media queries provide the ability to specify different styles for individual browser and device circumstances, the width of the viewport or device orientation for example.

Generally speaking it is recommend to use the @media rule inside of an existing style sheet to avoid any additional HTTP requests.

One popular technique with using media queries is called mobile first. The mobile first approach includes using styles targeted at smaller viewports as the default styles for a website, then use media queries to add styles as the viewport grows.

## All About Floats
Float is a CSS positioning property. 

In page layout programs, the boxes that hold the text can be told to honor the text wrap, or to ignore it. Ignoring the text wrap will allow the words to flow right over the image like it wasn’t even there. This is the difference between that image being part of the flow of the page (or not).

There are four valid values for the float property. Left and Right float elements those directions respectively. None (the default) ensures the element will not float and Inherit which will assume the float value from that elements parent element.

Aside from the simple example of wrapping text around images, floats can be used to create entire web layouts.

Floats often get beat on for being fragile. The majority of this fragility comes from IE 6 and the slew of float-related bugs it has. As more and more designers are dropping support for IE 6, you may not care, but for the folks that do care here is a quick rundown.

## Don't Overthink It Grids
The vast majority of websites out there use a grid. They may not explicitly have a grid system in place, but if they have a “main content area” floated to the left a “sidebar” floated to the right, it’s a simple grid.

- Context
- Columns
- Clearing Context
- Gutters
- Outside Gutters

## CSS Floats Explained By Riding An Escalator
Floats create alternate flows. This is the hardest part to understand. And once you introduce them, you then need to write your code so that it accounts for up to three flows: normal, left and right. This is a whole new set of rules, as opposed to manipulating the width of elements or their positioning.

Floats allow you to create these new relationships between flows.

This allows you to create more readable and understandable code, because the float property also gives an indication of an element’s relationship to surrounding elements.

Clear allows elements to specify where they should align in comparison to the floated elements.

One of the most frequent uses of the clear property is “clear:both”. This allows you to reset the flow of elements, as opposed to continuing to maintain a right, left and normal flow.

