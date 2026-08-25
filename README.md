# Flip Card Digital Business Card

**Live site:** https://omoleyeabigail82-dot.github.io/Flip-Card-Digital-Business-Card/
**Repo:** https://github.com/omoleyeabigail82-dot/Flip-Card-Digital-Business-Card

## What it is
An interactive digital business card built with pure HTML, CSS, and JavaScript. The card flips on click to reveal contact details on the back, styled in a black-and-gold theme.

## Why I built it
I wanted a small, focused project to practice a few specific skills I hadn't applied hands-on yet: CSS 3D transforms, JavaScript DOM event handling, and responsive design with media queries — while building something genuinely useful for my portfolio instead of another generic beginner project.

## Tech stack
- HTML for structure
- CSS for styling and the 3D flip animation
- Vanilla JavaScript for the click interaction
- Deployed with GitHub Pages

## Key concepts practiced
- **CSS 3D transforms** — `perspective`, `transform-style: preserve-3d`, `backface-visibility`, and `rotateY()` to create the flip effect
- **Flexbox** — centering content both on the page and within each card face
- **DOM manipulation** — using `classList.toggle()` in JavaScript to trigger the flip on click
- **Responsive design** — using a media query with `vw` units so the card scales properly on smaller screens instead of staying a fixed pixel size

## Challenges & how I solved them

**1. Script tag placement bug**
I initially placed my `<script>` tag inside `<head>`, which meant it ran before the HTML body existed. The JavaScript couldn't find the `.card` element, so the click listener never attached and nothing flipped. Fixed by moving the script tag to just before `</body>`, so it runs after the DOM has loaded.

**2. Testing on `file://` vs a local server**
Chrome threw a security warning when testing responsive/mobile view directly from an opened file. Switched to VS Code's Live Server extension to serve the page over `localhost`, which resolved it and also gave me live-reload while I worked.

**3. Deployment/visibility**
Initially published the repo as private, which meant GitHub Pages couldn't serve it publicly. Switched the repo visibility to public to get a working live link.

## What I'd do differently next time
- Add a custom favicon (currently using the default, which throws a harmless 404 in the console)
- Consider adding a subtle animation on page load, not just on click, to make the first impression stronger
- Write semantic HTML tags (e.g. `<section>`, `<article>`) instead of relying solely on `<div>`s, for better accessibility and structure

## Features
- Click-to-flip card animation (front: name + title, back: bio + contact links)
- Black-and-gold themed design
- Profile photo
- Fully responsive layout
