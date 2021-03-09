---
title: Popout menu
tags: interactivity,intermediate
---

# Reveals an interactive popout menu on hover and focus.

- `position: relative` on the reference parent establishes a Cartesian positioning context for its child.
- `position: absolute` takes the popout menu out of the flow of the document and positions it in relation to the parent.
- `left: 100%` moves the the popout menu 100% of its parent's width from the left.
- `visibility: hidden` hides the popout menu initially and allows for transitions (unlike `display: none`).
- `.reference:hover > .popout-menu` means that when `.reference` is hovered over, select immediate children with a class of `.popout-menu` and change their `visibility` to `visible`, which shows the popout.
- `.reference:focus > .popout-menu` means that when `.reference` is focused, the popout would be shown.
- `.reference:focus-within > .popout-menu` ensures that the popout is shown when the focus is within the reference.

```html
<div class="reference" tabindex="0">
  <div class="popout-menu">Popout menu</div>
</div>
```

```css
.reference {
  position: relative;
  background: tomato;
  width: 100px;
  height: 80px;
}

.popout-menu {
  position: absolute;
  visibility: hidden;
  left: 100%;
  background: #333;
  color: white;
  padding: 16px;
}

.reference:hover > .popout-menu,
.reference:focus > .popout-menu,
.reference:focus-within > .popout-menu {
  visibility: visible;
}
```
