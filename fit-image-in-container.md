---
title: Fit image in container
tags: layout,visual,intermediate
---

# Changes the fit and position of an image within its container while preserving its aspect ratio. Previously only possible using a background image and the `background-size` property.

- `object-fit: contain` fits the entire image within the container while preserving its aspect ratio.
- `object-fit: cover` fills the container with the image while preserving its aspect ratio.
- `object-position: [x] [y]` positions the image within the container.

```html
<img class="image image-contain" src="https://picsum.photos/600/200" /> <img class="image image-cover" src="https://picsum.photos/600/200" />
```

```css
.image {
  background: #34495e;
  border: 1px solid #34495e;
  width: 200px;
  height: 200px;
}

.image-contain {
  object-fit: contain;
  object-position: center;
}

.image-cover {
  object-fit: cover;
  object-position: right top;
}
```
