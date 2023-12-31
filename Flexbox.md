# Flexbox

Flexbox is a one-dimensional CSS layout that can control the way items are spaced out and aligned within a container.

* Any direct children of a flex container are called flex items.

* The `flex-wrap` property determines how your flex items behave when the flex container is too small. Setting it to `wrap` will allow the items to wrap to the next row or column. `nowrap` (default) will prevent your items from wrapping and shrink them if needed.

* The justify-content property determines how the items inside a flex container are positioned along the main axis, affecting their position and the space around them.

* The align-items property positions the flex content along the cross axis. In the case, flex-direction set to row, the cross axis would be vertical.

* When the images have different aspect ratios, thay can become distorted. Rather than setting each aspect ratio individually, you can use the **object-fit property** to determine how images should behave.    
  ~~~~
  .gallery img {
      width: 100%;
      object-fit: cover;
  }
  ~~~~

* The `gap` CSS shorthand property sets the gaps, also knowns as gutters, between rows and columns. The **`gap` property** and its `row-gap` and `column-gap` sub-properties provide this functionality for flex, grid, and multi-column layout. You apply the property to the container element.

* The **`::after`** pseudo-element **creates an element that is *the last child of* the selected element**. You can use it to add an empty element after the last image. If you give it the same `width` as the images it will push the last image to the left when the gallery is in a two-column layout. Right now, it is in the center because you set `justify-content: center` on the flex container.  
  ~~~~
  .gallery::after {
      content: "";
      width: 350px;
  }
  ~~~~

  