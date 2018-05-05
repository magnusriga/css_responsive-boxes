# Responsive Boxes in HTML and CSS

<a href="http://www.youtube.com/watch?feature=player_embedded&v=62s46CjiCwE
" target="_blank"><img src="http://img.youtube.com/vi/62s46CjiCwE/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>

## Introduction

* Bootstrap 4's card feature is not yet fully responsive
* Moreover, it has a few other features that may not be desired (such as filling the full width of the page)
* This HTML and CSS code offers a template for responsive boxes

## Features

* Responsive across device-sizes. Dynamically changes:
  * Width of boxes
  * Spacing between boxes (narrower for smaller screens)
  * Number of rows (boxes fall to a new row before width shrinks)
* All HTML/CSS (no JavaScript)
* No third-party libraries

## Usage

* For each desired box, just copy and paste the div with the column and columnMargin classes on it, one below the other.
* Each column (box) is "display: inline-block;", which has a default margin-right: 4px. This is removed by keeping the column div's next to each other (no line-break). See more info here [Fighting the Space Between Inline Block Elements | CSS-Tricks][1].
* Width of the boxes overall is set in the cardbox class. If changing it, remember to adjust the size of child divs as well
* Don't put other elements inside the negativeMargin div. It will not display correctly, because the positive margin of previous box will push it away, then the negative margin of the ancestor div will drag other elements on top of it.

## Implementation notes

* Note on use of negative margins: When a positive margin is introduced on each box (column class), elements to the top and right are pushed away from border. Thus, we add a negative margin to the parent div, in order to pull surrounding elements closer (i.e. negating the column margins). Unfortunately, this also means that the content is pulled out on the right hand side of the screen, causing a horizontal overflow. To hide that, we apply "overflow-x: hidden" to parent div.

[1]: https://css-tricks.com/fighting-the-space-between-inline-block-elements/