# Frontend Mentor - Product preview card solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GOMdtbVl1v). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### Screenshot

![Product Preview Card](./preview.jpg)

### Links

- Solution URL: [GitHub Repository](https://github.com/K0Teu4/ProductPreview)
- Live Site URL: [GitHub Pages](https://k0teu4.github.io/ProductPreview/)

## My process

### Built with

- Semantic HTML5 markup (article, picture, source, s for strikethrough price)
- CSS Custom Properties
- CSS Grid with a responsive layout switch
- Mobile-first workflow
- Google Fonts (Montserrat + Fraunces)
- Inline SVG icon with currentColor

### What I learned

This challenge was about responsive layout: the card is stacked vertically on mobile and horizontal on desktop.

#### picture element for art direction
Used a picture with two source elements so the browser picks the right image (mobile vs desktop crop) without needing JavaScript or duplicate img tags. The mobile version is the default fallback.

#### CSS Grid for the layout switch
Started mobile-first with grid-template-columns: 1fr. At the 40em breakpoint, switched to grid-template-columns: 2fr 3fr so the image takes ~40% and the content takes ~60% — matching the design proportions.

#### overflow hidden on the card
Instead of adding border-radius to the image on specific corners, I put overflow: hidden on the .product container so the image's top corners (on mobile) or side corners (on desktop) get clipped naturally.

#### semantic pricing
Used the s element for the original (now crossed-out) price — it semantically means "no longer accurate", which is exactly what a strikethrough discount price is.

#### SVG with currentColor
The cart icon uses fill="currentColor" so it inherits the button's text color, and will automatically change if I update the button styling.

### Useful resources

- [MDN — picture](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture)
- [MDN — s element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/s)
- [MDN — grid-template-columns](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-columns)
- [MDN — currentColor keyword](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#currentcolor_keyword)

## Author

- GitHub — [@K0Teu4](https://github.com/K0Teu4)
- Frontend Mentor — [@K0Teu4](https://www.frontendmentor.io/profile/K0Teu4)
