---
title: Box-sizing reset
tags: layout,beginner
---

# Resets the box-model so that `width` and `height` are not affected by `border` or `padding`.

- `box-sizing: border-box` makes the addition of `padding` or `border`s not affect an element's `width` or `height`.
- `box-sizing: inherit` makes an element respect its parent's `box-sizing` rule.

```html
<div class="box">border-box</div>
<div class="box content-box">content-box</div>
```

```css
div {
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: inherit;
}

.box {
  display: inline-block;
  width: 120px;
  height: 120px;
  padding: 8px;
  background: #f24333;
  color: white;
  border: 1px solid #ba1b1d;
  border-radius: 4px;
}

.content-box {
  box-sizing: content-box;
}
```
