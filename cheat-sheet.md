# Image & Text Cheat Sheet — index.html

---

## 1. Hero image (full-width banner at the top)

**Where the file goes:** `images/` folder
**Filename in use:** `silhouette.jpg`

**To swap it**, replace this line in the HTML (~line 374):
```html
<img src="images/silhouette.jpg" alt="">
```
Change `silhouette.jpg` to your new filename.

**Title** (large text over the image, ~line 376):
```html
<h1>Thank you for clicking the link.</h1>
```

**Subtitle** (small caps line beneath the title, ~line 377):
```html
<p class="hero-sub">Aidan J. Sinclair &nbsp;·&nbsp; Curator and Exhibition Manager &nbsp;·&nbsp; Application</p>
```

---

## 2. Single exhibition image (below the page header)

**Where the file goes:** `images/` folder
**Filename in use:** `havoc-hendricks.jpg`

**To swap it or change the caption**, find this block (~line 391):
```html
<div class="image-block">
  <figure>
    <img src="images/havoc-hendricks.jpg" alt="Installation view, Havoc Hendricks, Gallery Nua, Houston">
    <figcaption>Installation view — Havoc Hendricks, Gallery Nua, Houston</figcaption>
  </figure>
</div>
```

- Change the `src` to point to your new file
- The `alt` attribute is the screen-reader description — keep it the same as the caption, or close
- The `<figcaption>` is the visible caption that appears below the image

---

## 3. Carousel (the scrolling image gallery in the letter)

**Where files go:** `images/` folder
**Expected filenames:** `carousel-1.jpg` through `carousel-10.jpg`

**To add images and captions**, find the `slides` array near the bottom of the file (~line 452):
```js
const slides = [
  { src: 'images/carousel-1.jpg',  caption: '' },
  { src: 'images/carousel-2.jpg',  caption: '' },
  // ... and so on through carousel-10.jpg
];
```

- The `src` value is the filename — change it if your file is named differently
- The `caption` value (between the `''` quotes) is the text that appears below the carousel when that image is active
- You can add or remove `{ src: ..., caption: ... }` lines to change the number of slides — just make sure each line (except the last) ends with a comma

**Example with captions filled in:**
```js
{ src: 'images/carousel-1.jpg', caption: 'Installation view — Some Exhibition, Gallery Name, 2024' },
{ src: 'images/carousel-2.jpg', caption: 'Opening night, Gallery Nua, Houston' },
```

---

## Quick file-placement summary

| What | File location | Notes |
|---|---|---|
| Hero image | `images/silhouette.jpg` | Full-width; any aspect ratio works |
| Exhibition image | `images/havoc-hendricks.jpg` | Displays at full column width (680px) |
| Carousel images | `images/carousel-1.jpg` … `carousel-10.jpg` | 2:3 portrait ratio looks best |

All image files go in the `images/` folder alongside the existing ones.
