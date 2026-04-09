# Frontend Mentor - Huddle landing page with single introductory section solution

This is a solution to the [Huddle landing page with single introductory section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/huddle-landing-page-with-a-single-introductory-section-B_2Wvxgi0). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the page depending on their device's screen size
- See hover states for all interactive elements on the page

### Screenshot

![Design screenshot](https://github.com/TheCoder-Rahul/frontend_mentor_huddle_landing_page/blob/main/project_screenshot.png)

### Links

- 👉 [Solution URL](https://github.com/TheCoder-Rahul/frontend_mentor_huddle_landing_page.git)
- 👉 [Live Site URL](https://thecoder-rahul.github.io/frontend_mentor_huddle_landing_page/)

## My process

### Built with

- 👉 **Markup:** Semantic HTML5 for better accessibility and SEO.
- 👉 **Styling:** CSS3 with Custom Properties (variables) for a maintainable color scheme, font-properties, and different sizes.
- 👉 **Layout:** Flexbox for centering the card and managing the internal alignment.
- 👉 **Workflow:** Mobile-first approach and Responsive Design using Media Queries.

### What I learned

Check my code snippets below:

```html
<main class="container">
  <header>
    <img src="./images/logo.svg" alt="Huddle Transparent Scalable Logo">
  </header>
  <section class="elements">
    <figure>
      <img src="./images/illustration-mockups.svg" alt="Mockups Illustration">
    </figure>
    <article>
      <h1>Build The Community Your Fans Will Love</h1>
      <p>Huddle re-imagines the way we build communities. You have a voice, but so does your audience. Create connections with your users as you engage in genuine discussion.</p>
      <button type="button">Register</button>
    </article>
  </section>
  <section class="social_links">
    <a class="social_icon" href="#" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-facebook-f"></i></a>
    <a class="social_icon" href="#" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-twitter"></i></a>
    <a class="social_icon" href="#" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-instagram"></i></a>
  </section>
</main>
```
```css
*, *::before, *::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
:root {
  --white: hsl(0, 0%, 100%);
  --purple-700: hsl(257, 40%, 49%);
  --magenta-400: hsl(300, 69%, 71%);
  --body-font: "Open Sans", sans-serif;
  --heading-font: "Poppins", sans-serif;
}
body {
  font-size: 1rem;
  color: var(--white);
  font-family: var(--body-font);
  background: url(./images/bg-mobile.svg) no-repeat var(--purple-700);
}
h1 {
  font-weight: 600;
  font-family: var(--heading-font);
  font-size: clamp(1.5rem, calc(3vw + 1rem), 2.9375rem);
}
img {
  height: auto;
  max-width: 100%;
}
main {
  gap: 4rem;
  display: flex;
  margin: auto;
  padding: 2.25rem;
  flex-direction: column;
  width: min(90rem, 100%);
}
header img {
  max-width: 50%;
  display: flex;
}
.elements {
  gap: 3rem;
  display: grid;
}
article {
  gap: 1.5rem;
  display: flex;
  line-height: 1.5;
  text-align: center;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}
button {
  width: 70%;
  cursor: pointer;
  font-size: 0.875rem;
  border-radius: 5rem;
  padding: 0.5rem 1rem;
  color: var(--purple-700);
  border-color: transparent;
  font-family: var(--heading-font);
  box-shadow: 0 0.5rem 1rem hsla(192, 76%, 10%, 0.2);
  -webkit-transition: all 0.2s ease-in-out;
  -moz-transition: all 0.2s ease-in-out;
  -ms-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;

  &:hover, &:focus {
    color: var(--white);
    background-color: var(--magenta-400);
  }
}
.social_links {
  gap: 0.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
}
.social_icon {
  width: 2rem;
  height: 2rem;
  padding: 0.125rem;
  border-radius: 50%;
  text-align: center;
  color: var(--white);
  font-size: 0.875rem;
  line-height: 1.675rem;
  border: 1px solid var(--white);
  -webkit-transition: color 0.2s ease-in-out, border 0.2s ease-in-out;
  -moz-transition: color 0.2s ease-in-out, border 0.2s ease-in-out;
  -ms-transition: color 0.2s ease-in-out, border 0.2s ease-in-out;
  -o-transition: color 0.2s ease-in-out, border 0.2s ease-in-out;
  transition: color 0.2s ease-in-out, border 0.2s ease-in-out;

  &:hover, &:focus {
    color: var(--magenta-400);
    border-color: var(--magenta-400);
  }
}
.attribution { font-size: 0.6875rem; text-align: center; }
.attribution a { color: var(--magenta-400); }
@media (min-width: 48rem) {
  body {
    height: 100vh;
    background-image: url(./images/bg-desktop.svg);
    background-size: cover;
  }
  main {
    height: 100%;
    padding: 4rem;
    justify-content: space-between;
  }
  .elements {
    grid-template-columns: minmax(50%, auto) 1fr;
  }
  article {
    text-align: start;
    font-size: 1.125rem;
    align-items: flex-start;
  }
  button {
    width: auto;
    font-size: 1rem;
    padding: 0.75rem 4rem;
  }
  .social_links {
    gap: 1rem;
    justify-content: flex-end;
  }
  .social_icon {
    width: 2.5rem;
    height: 2.5rem;
    font-size: 1rem;
    line-height: 2.125rem;
  }
  .attribution { position: absolute; inset: auto 0 0.5rem; }
}
```

## Author

- 👉 GitHub - [TheCoder-Rahul](https://github.com/TheCoder-Rahul)
- 👉 Frontend Mentor - [@TheCoder-Rahul](https://www.frontendmentor.io/profile/TheCoder-Rahul)
- 👉 LinkedIn - [@Rahul Kumar](https://www.linkedin.com/in/rahul-the-developer/)
