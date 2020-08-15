# Reading 11 Styling a HTML5 Form
See The Net Ninja github for more details!

## Intro
HTML
Link the input (for in input and id in label) to match with the label thus connecting them. Associates the two.

CSS
- body
- header
- form
- form p for p-tags

## Styling Radio Buttons
CSS
- input [type="radio"] 
- label [for="male], label[for="female"]
- input:checked + label[for="male"]
- input:checked + label[for="female"]

## Styling CheckBoxes
CSS
- input [type="checkbox"]
- label [for="web"], label[for="photoshop"], label[for="madona"]
- input:checked + label[for="web"], input:checked + label[for="photoshop"], input:checked + label[for="madona"]

## Styling Text Inputs
- fieldset
- legend
- input [type="email"], input [type="telephone"] display: block

## Styling Select Boxes
- select -webkit-appearance: none (also add for Mozilla, O, MS)
- input [type="submit"]

## Validation Styles
- span 
- input type="telephone" placeholder="Phone Number" required (need for validation via HTML)
- input [type="email"]:valid
- input [type="telephone"]:valid
- input [type="email"]:valid + .tick
- input [type="telephone"]:valid + .tick

Best video I have watch on CSS so far!


