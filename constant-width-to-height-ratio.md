---
title: Constant width to height ratio
tags: layout,beginner
---

# Given an element of variable width, it will ensure its `height` remains proportionate in a responsive fashion (i.e. its `width` to `height` ratio remains constant).

- `padding-top` on the `:before` pseudo-element causes the height of the element to equal a percentage of its width. `100%` therefore means the element's height will always be `100%` of the width, creating a responsive square.
- This method also allows content to be placed inside the element normally.

```html
<div class="constant-width-to-height-ratio"></div>
```

```css
.constant-width-to-height-ratio {
  background: #333;
  width: 50%;
}

.constant-width-to-height-ratio:before {
  content: '';
  padding-top: 100%;
  float: left;
}

.constant-width-to-height-ratio:after {
  content: '';
  display: block;
  clear: both;
}
```
