# Frontend Mentor - Coding bootcamp testimonials slider solution

This is a solution to the [Coding bootcamp testimonials slider challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/coding-bootcamp-testimonials-slider-4FNyLA8JL). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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


## Overview

### The challenge

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- Navigate the slider using either their mouse/trackpad or keyboard

### Screenshot

![](./src/images/screenshot.png).

### Links

- Solution URL: [github](https://github.com/Diego2Drm/Coding-bootcamp-testimonials-slider)
- Live Site URL: [Coding-bootcamp-testimonials-slider](https://diego2drm.github.io/Coding-bootcamp-testimonials-slider/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- JavaScript

### What I learned

"I learned how to make a slider with HTML and JavaScript."


```html
 <section class="carousel">
    <div class="carousel-inner">
      <article class="carousel-item">
      </article>

      <article class="carousel-item">
      </article>
    </div>

    <div class="icons-container">
    </div>
  </section>

```
```css
.carousel {
  width: 100%;
  overflow: hidden;
}

.carousel-inner {
  display: flex;
  transition: transform 0.5s ease-in-out;
}

.carousel-item {
  min-width: 100%;
  padding-top: 4rem;
  transition: opacity 0.5s ease-in-out;
}
```
```js
    let currentIndex = 0;

    function showSlide(index) {
      const slides = document.querySelectorAll(".carousel-item");

      if (index >= slides.length) {
        currentIndex = 0;
      } else if (index < 0) {
        currentIndex = slides.length - 1
      } else {
        currentIndex = index
      }

      const offset = -currentIndex * 100;
      document.querySelector('.carousel-inner').style.transform = `translateX(${offset}%)`;
    }

    function nextSlide() {
      showSlide(currentIndex + 1);
    }
    function prevSlide() {
      showSlide(currentIndex - 1);
    }

    document.addEventListener('DOMContentLoaded', () => {
      showSlide(currentIndex);
    });

```

### Continued development

-JavaScript

## Author

- Frontend Mentor - [@Diego2Drm](https://www.frontendmentor.io/profile/Diego2Drm)
