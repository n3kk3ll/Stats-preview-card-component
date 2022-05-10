# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![Screenshot](desktop-preview.jpg)

### Links

- Solution URL: [Frontend Mentor](https://www.frontendmentor.io/solutions/stats-preview-card-component-rJKue7OL9)
- Live Site URL: [Vercel](https://stats-preview-card-component-zeta-olive.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Simple @keyframes animation to make card appear.

### What I learned

The only one thing that was hard to me, is apply a color to image. First thing I thought about was filter() function, but it doesn't applied to image. The problem was solved with few minutes of google and the solution is mix-blend-mode property. This property blends element's content with the content of element's parent and element's background (MDN).

```css
image-wrapper {
    max-width: 540px;
    width: 100%;
    min-height: 100%;
    position: relative;
    &::before {
      content: "";
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
      background-color: hsla(277, 64%, 61%, 0.9);
      mix-blend-mode: multiply;
    }
  }
```
``multiply`` value mixes the colors of the element and the element's parent content.

### Useful resources
 
- [mix-blend-mode on W3C](https://www.w3schools.com/cssref/pr_mix-blend-mode.asp) - This is an amazing article which helped me finally understand this property clearly. I strongly recommend it to anyone still learning this concept.
- [@keyframes rule on W3C](https://www.w3schools.com/cssref/css3_pr_animation-keyframes.asp) - So if I used custom property in my project, I give the most detailed article about this rule.

## Author

- GitHub - [@n3kk3ll](https://github.com/n3kk3ll)
- Frontend Mentor - [@n3kk3ll](https://www.frontendmentor.io/profile/n3kk3ll)
- LinkedIn - [Andrii Zhemchuzhnyi](https://www.linkedin.com/in/andrii-zhemchuzhnyi-26019b221/)
