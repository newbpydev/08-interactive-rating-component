# Frontend Mentor - Interactive rating component solution

This is a solution to the [Interactive rating component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/interactive-rating-component-koxpeBUmI). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Frontend Mentor - Interactive rating component solution](#frontend-mentor---interactive-rating-component-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
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

This is my solution to the Interactive Rating Component challenge. It is an
interactive rating component that will receive input from the user, the user
must select a value from 1 to 5 and submit the form. The user receives a thank
you note with the selected rating our of 5 and a thank you message.

### Screenshot

![](./src//assets//images//screenshot-desktop.png)
![](./src//assets//images/screenshot-mobile.png)

### Links

- Solution URL: [GitHub](https://github.com/newbpydev/08-interactive-rating-component)
- Live Site URL: [Live Site](https://earnest-fox-cf8611.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Svelte + Vite + TypeScript

### What I learned

I have learned on this project that we need to practice everyday and work hard
to really understand how everything works, specially with the flexbox. Flexbox
is very powerful and useful but we much mind the margin spaces that might
influence the final spacing inside a flexbox. I must further study this topic.

```css
.interactive-rating {
  max-width: 32.7rem;
  height: 36rem;
  padding: 2.4rem 2.4rem 3.2rem 2.4rem;
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  background: radial-gradient(
    98.96% 98.96% at 50% 0%,
    #232a34 0%,
    #181e27 100%
  );
  border-radius: var(--border-radius);
}
```

### Continued development

For future development, I will continue to use flexbox to help me with the
layout of my components. For the next project I would like to try new ways of
using flexbox. I have also used the input with a button type, I will futher
study this topic as well.

### Useful resources

- [MDN - input type="button"](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/button) - input elements of type button are rendered as simple push buttons, which can be programmed to control custom functionality anywhere on a webpage as required when assigned an event handler function (typically for the click event).
- [MDN - Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox) - Flexbox is a one-dimensional layout method for arranging items in rows or columns. Items flex (expand) to fill additional space or shrink to fit into smaller spaces. This article explains all the fundamentals.

## Author

- Website - [Juan Gomez](https://www.newbpydev.com)
- Frontend Mentor - [@newbpydev](https://www.frontendmentor.io/profile/newbpydev)
- Twitter - [@Newb_PyDev](https://twitter.com/Newb_PyDev)

## Acknowledgments

The code may not be perfect compared to my sensei @jonasschmedtman but I need
to thank him because he has shown me the ropes and now I am a confident web
designer.
