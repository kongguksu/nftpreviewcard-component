# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](/screenshot.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Absolute positioning
- Desktop-first workflow

### What I learned

How to overlay color on an image during a hover state.

```html
  <body>
    <main class="nftcard">
      <div class="nftcard-container">
        <div class="nftcard-main">
          <div class="nftcard-img-box">
            <img
            class="nftcard-img"
            src="images/image-equilibrium.jpg"
            alt="Transparent cube with red light through it"
            />
            <div class="overlay">
            </div>
            <span class="overlay-eye">
              <ion-icon class="overlay-icon" name="eye">
            </span>
          </div>
```

```css
.nftcard-img-box {
  width: 15.6rem;
  height: 15.6rem;
  border-radius: 7px;
  position: relative;
}

.nftcard-img {
  width: 100%;
  height: 100%;
  border-radius: 7px;
}

.overlay {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100%;
  width: 100%;
  border-radius: 7px;
  opacity: 0;
  transition: all 0.3s;
  background-color: hsl(178, 100%, 50%);
}

.overlay-eye {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  visibility: hidden;
  transition: all 0.1s;
}

.nftcard-img-box:hover .overlay,
.nftcard-img-box:active .overlay {
  opacity: 0.5;
}

.nftcard-img-box:hover .overlay-eye,
.nftcard-img-box:active .overlay-eye {
  visibility: visible;
```

### Continued development

I struggled to find a way to overlay color on the image. I tried absolute positioning in the end, but before I did that, I tried using the filter property on the image and tried playing around with different values like hue rotate, brightness, sepia, but it didn't seem to work out.

When hovering over the image, the cyan color does not come on right away on certain parts of the image(e.g. red parts of the transparent cube), so I'm unsure if what I did is correct.

## Author

- Frontend Mentor - [@kongguksu](https://www.frontendmentor.io/profile/kongguksu)
