# testimonials-grid
Testimonials grid layout from Frontend Mentor

# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot


### Links

- Solution URL: [Solution](https://github.com/zitescody/testimonials-grid)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS Grid
- Mobile-first workflow

### What I learned

I further learned how to create a responsive webpage based on preselected media queries. In this example, The text and size of boxes move with the resizing of the screen.

```css
:root {
    /* Primary Colors */
    --moderateviolet: hsl(263, 55%, 52%);
    --verydarkgrayishblue: hsl(217, 19%, 35%);
    --verydarkblackishblue: hsl(219, 29%, 14%);
    --white: hsl(0, 0%, 100%);

    /* Neutral Colors */
    --lightgray: hsl(0, 0%, 81%);
    --lightgrayishblue: hsl(210, 46%, 95%);

    /* 
    1. "Verified Graduate" has the same color as the person's name with 50% opacity
    2. Review paragraphs inside the quotations have the same color as well, but are at 70% opacity
    */
}
```
```css
/* Grid Styles */
div.container-one {
    grid-column-start: second;
    grid-column-end: third;
    grid-row-start: second;
    grid-row-end: third;
    justify-self: center;
    align-self: top;
    grid-area: one;
}

div.container-two {
    grid-column-start: second;
    grid-column-end: third;
    grid-row-start: third;
    grid-row-end: fourth;
    justify-self: center;
    align-self: top;
    grid-area: two;
}

div.container-three {
    grid-column-start: second;
    grid-column-end: third;
    grid-row-start: fourth;
    grid-row-end: fifth;
    justify-self: center;
    align-self: top;
    grid-area: three;
}

div.container-four {
    grid-column-start: second;
    grid-column-end: third;
    grid-row-start: fifth;
    grid-row-end: sixth;
    justify-self: center;
    align-self: top;
    grid-area: four;
}

div.container-five {
    grid-column-start: second;
    grid-column-end: third;
    grid-row-start: sixth;
    grid-row-end: seventh;
    justify-self: center;
    align-self: top;
    grid-area: five;
}

main.container {
    display: grid;
    grid-template-columns: [first] 5% [second] 90% [third] 5% [end];
    grid-template-rows: [first] 0% [second] 23% [third] 14% [fourth] 13% [fifth] 22% [sixth] 25% [seventh] 1% [end];
    grid-template-areas: 
        ". . ."
        ". one ."
        ". two ."
        ". three ."
        ". four ."
        ". five ."
        ". . ."
    ;
    row-gap: 30px;
}
```
```js
@media (min-width: 1000px) {
    /* Grid Styles */
    div.container-one {
        grid-column-start: second;
        grid-column-end: fourth;
        grid-row-start: second;
        grid-row-end: third;
        justify-self: center;
        align-self: top;
        grid-area: one;
    }
    
    div.container-two {
        grid-column-start: fourth;
        grid-column-end: fifth;
        grid-row-start: second;
        grid-row-end: third;
        justify-self: center;
        align-self: top;
        grid-area: two;
    }
    
    div.container-three {
        grid-column-start: second;
        grid-column-end: third;
        grid-row-start: third;
        grid-row-end: fourth;
        justify-self: center;
        align-self: top;
        grid-area: three;
    }
    
    div.container-four {
        grid-column-start: third;
        grid-column-end: fifth;
        grid-row-start: third;
        grid-row-end: fourth;
        justify-self: center;
        align-self: top;
        grid-area: four;
    }
    
    div.container-five {
        grid-column-start: fifth;
        grid-column-end: sixth;
        grid-row-start: second;
        grid-row-end: fourth;
        justify-self: center;
        align-self: top;
        grid-area: five;
    }
    
    main.container {
        display: grid;
        grid-template-columns: [first] 10% [second] 20% [third] 20% [fourth] 20% [fifth] 20% [sixth] 10% [end];
        grid-template-rows: [first] 2.5% [second] 47.5% [third] 47.5% [fourth] 2.5% [end];
        grid-template-areas: 
            ". . . . . ."
            ". one one two five ."
            ". three four four five ."
            ". . . . . ."
        ;
        row-gap: 20px;
        column-gap: 20px;
    }
}
```
### Continued development

I had trouble keeping the text within the boundaries of the boxes. Sometimes there was overflow. Hiding it did not solve my problem for then the text would not be seen.

## Author

- Website - [Cody Zites](https://github.com/zitescody)
- Frontend Mentor - [zitescody](https://www.frontendmentor.io/profile/zitescody)
