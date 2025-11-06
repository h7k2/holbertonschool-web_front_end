Advanced CSS — Techium (Holberton)

A compact, practical guide and README for the CSS_advanced project.
It gathers the goals, files to create, and what each task expects, so you can build and validate your work fast.

📌 Project Overview

You’ll style the Techium landing page using modern CSS:

Build a scalable CSS architecture with custom properties (CSS variables).

Control typography (fonts, sizes, weights, line-height).

Apply grid-like layouts with floats and clearfix.

Add themes (light/dark) and component states (hover, active, visited).

Use transitions, transformations, and buttons with variables.

Normalize styles for cross-browser consistency.

You will progressively complete styles/1-style.css → styles/32-style.css and plug the right stylesheet into index.html.

🎯 Learning Objectives

Selectors, properties, values

Block vs inline styling

CSS reset / normalization

CSS variables (:root) and reuse

Inline vs embedded vs external CSS

Grid systems using floats

Webfont icons vs SVG icons

Pseudo-classes vs pseudo-elements

Background gradients (later)

CSS animations & transitions

2D/3D transforms

Vendor prefixes (know when/how to use)

🧰 Prerequisites

Editors: vi/vim/emacs/VSCode/Atom

Target browser: Chrome 78.x (per spec)

All files end with a newline and start with a short task description comment

W3C-compliant and validated (except when the task says it doesn’t have to)

Assets stored in images/

📁 Project Structure
holbertonschool-web_front_end/
└── CSS_advanced/
    ├── index.html
    ├── images/
    │   ├── favicon.jpg
    │   ├── logo-black.png
    │   ├── logo-white.png
    │   ├── pic-about-01.jpg
    │   ├── pic-work-01.jpg
    │   ├── pic-work-02.jpg
    │   ├── pic-work-03.jpg
    │   ├── pic-article-01.jpg
    │   ├── pic-article-02.jpg
    │   ├── pic-article-03.jpg
    │   ├── pic-person-01.jpg
    │   ├── pic-person-02.jpg
    │   └── pic-person-03.jpg
    └── styles/
        ├── 1-style.css
        ├── 2-style.css
        ├── ...
        └── 32-style.css


In index.html, replace <link rel="stylesheet" href="#"> with the stylesheet for the task you’re testing (e.g., styles/10-style.css).

🚀 Getting Started

Add assets
Download the 10 Unsplash images (consistent with their section) + the provided favicon and logos. Save under images/.

Use the provided HTML
The starter index.html is included in your brief. Keep class names and IDs exactly as provided (case sensitive!).

Work incrementally
For each task, create the corresponding CSS file in styles/ and link it in index.html.

Validate
Use W3C validator when required. Some tasks explicitly say “Does not need to pass W3C”.

✅ Task-by-Task Checklist

0. Images

Add all images to images/ with exact filenames.

1. Smooth scroll → styles/1-style.css

Make html scroll behavior smooth (e.g., scroll-behavior: smooth;).

2. Color values → styles/2-style.css

body & a: color #161616

.visually-hidden: display: none

.card-category & .section-tagline: color #D73953

3. Variables (colors) → styles/3-style.css

In :root:

--color-primary: #d73953

--color-black: #090909

--color-white: #ffffff

--color-light-grey: #f3f3f3

--color-dark-grey: #353535

--text-color: var(--color-black)

Use variables:

.section-tagline, .card-category → var(--color-primary)

body, a → var(--text-color)

4. Variables (font-family) → styles/4-style.css

:root: --font-family-base, --font-family-title
("Helvetica Neue", Helvetica, Arial, sans-serif)

body { font-family: var(--font-family-base) }

h1–h6 { font-family: var(--font-family-title) }

5. Variables (font-size) → styles/5-style.css

:root: --font-size-small: 1.2rem, --font-size-medium: 1.6rem, --font-size-large: 1.8rem, --font-size-x-large: 2.3rem, --font-size-xx-large: 4.8rem

html { font-size: 62.5%; }

body { font-size: var(--font-size-medium); }

6. Variables (font-weight) → styles/6-style.css

:root: --font-weight-regular: 400, --font-weight-bold: 700

body { font-weight: var(--font-weight-regular) }

h1–h6 { font-weight: var(--font-weight-bold) }

7. Google Fonts → styles/7-style.css

Update variables:

--font-family-base: "Open Sans", ...

--font-family-title: "Raleway", ...
(Keep the fallback stack.)

8. Line-height → styles/8-style.css

:root: --line-height-small: 1.2, --line-height-base: 1.5, --line-height-big: 1.8

body { line-height: var(--line-height-base) }

9. Links decoration → styles/9-style.css

a { text-decoration: none; }

10. Center section titles → styles/10-style.css

:root: --section-header-align: center

.section-header { text-align: var(--section-header-align) }

11. Section tagline styles → styles/11-style.css

:root: --section-tagline-transform: uppercase

.section-tagline { font-family: var(--font-family-title); text-transform: var(--section-tagline-transform); font-weight: var(--font-weight-bold) }

12. Section title styles → styles/12-style.css

:root: --section-title-margin: 0, --section-title-color: var(--color-black)

.section-title { font-family: var(--font-family-title); font-size: var(--font-size-xx-large); font-weight: var(--font-weight-bold); margin: var(--section-title-margin); color: var(--section-title-color) }

13. Pseudo-classes (links) → styles/13-style.css

Target only anchors with href (a[href])

:visited { font-style: italic }

:hover { text-decoration: underline }

:active { background: var(--color-light-grey) }

14. Normalize → styles/14-style.css

Include necolas/normalize.css (specified version).

15. Universal box-sizing → styles/15-style.css

Add *, *::before, *::after { box-sizing: border-box; }

16. Container → styles/16-style.css

.container { width: 960px; margin: 0 auto; }

17. Section paddings → styles/17-style.css

:root:

--section-padding: 5rem 0

--section-header-padding: 0 0 3rem

--section-body-padding: 0 0 3rem

--section-footer-padding: 3rem 0 0

--section-footer-align: center

--footer-padding: 5rem 0 1rem

.section { padding: var(--section-padding) }

.section-header { padding: var(--section-header-padding) }

.section-body { padding: var(--section-body-padding) }

.section-footer { padding: var(--section-footer-padding); text-align: var(--section-footer-align) }

.footer { padding: var(--footer-padding) }

18. Navbar → styles/18-style.css

.navbar-menu { float: right }

.nav { margin:0; padding:0; list-style:none; text-align:center }

.nav .nav-item { font-family: var(--nav-item-font-family); font-weight: var(--nav-item-font-weight); font-size: var(--nav-item-font-size); letter-spacing: var(--nav-item-letter-spacing); display: var(--nav-item-display); margin: var(--nav-item-margin) }

.nav .nav-link { display:block; padding: .5rem 1rem }

.nav .nav-link:hover { color: var(--nav-item-link-hover) }

Vars:

--nav-item-font-family: var(--font-family-title)

--nav-item-font-weight: var(--font-weight-bold)

--nav-item-font-size: var(--font-size-medium)

--nav-item-letter-spacing: 0.4rem (“4% of root” ≈ 0.4rem if root=10px)

--nav-item-display: inline-block

--nav-item-margin: 3rem 0 0 0

--nav-item-link-hover: var(--color-primary)

19. Grid utilities → styles/19-style.css

:root { --section-tagline-margin: 0 }

.section-tagline { margin: var(--section-tagline-margin) }

.row { margin:0; padding:0; list-style:none }

.col-1-3 { width:33.33%; float:left; padding:.5rem }

.col-1-2 { width:50%; float:left; padding:.5rem }

.footer-copyright { margin:0; font-size: var(--font-size-small); color: var(--text-color) }

.footer ul { text-align:right }

20. Clearfix → styles/20-style.css

.row::after { content:""; display:table; clear:both }

21. Simplify col- → styles/21-style.css

[class^="col-"] { float:left; padding:.5rem }

Remove duplicate props from .col-1-3 / .col-1-2 (keep only widths).

22. Dark theme → styles/22-style.css

[data-section-theme="dark"] { --text-color: var(--color-white); --section-title-color: var(--color-white); background: var(--color-black); }

23. Dark theme fixes → styles/23-style.css

.footer-address { color: var(--text-color) }

.social-link { display:block }

.social-link svg { fill: var(--text-color) }

24. Services hover → styles/24-style.css

.card-services .card-title { margin:0 }

.card-services a { display:block; padding:2rem; background: var(--color-light-grey); }

.card-services a:hover { color: var(--color-white); background: var(--color-primary); text-decoration:none }

25. Button variables → styles/25-style.css

In :root:

--button-display: inline-block

--button-padding: 1.5rem 3rem

--button-border: .2rem solid var(--color-primary)

--button-color: var(--color-black)

--button-text-decoration: none

--button-font-size: var(--font-size-large)

--button-hover-color: var(--color-white)

--button-hover-text-decoration: none

--button-hover-background: var(--color-primary)

.button { display: var(--button-display); padding: var(--button-padding); border: var(--button-border); font-size: var(--button-font-size); color: var(--button-color); text-decoration: var(--button-text-decoration); }

.button:hover { color: var(--button-hover-color); text-decoration: var(--button-hover-text-decoration); background: var(--button-hover-background); }

In [data-section-theme="dark"], add --button-color: var(--color-white)

26. Testimonials → styles/26-style.css

.card-testimonial { text-align:center }

.card-testimonial .card-avatar { border-radius:50%; width:10rem; height:10rem }

.card-testimonial .card-quote cite { display:block; padding-top:1rem; color: var(--color-primary) }

27. Hero → styles/27-style.css

.section-hero { background-size: 90rem auto }

.section-hero .section-title { margin-bottom:5rem }

.section-hero .section-inner { padding:10rem 40rem 2rem 0 }

28. Header / logo → styles/28-style.css

Vars:

--header-padding: 4rem 0 0

--header-logo-position: relative

--header-logo-link-display: inline-block

--header-logo-link-position: absolute

--header-logo-link-top: -1rem

--header-logo-link-left: 0

.header { padding: var(--header-padding) }

.header-logo { position: var(--header-logo-position) }

.header-logo a { display: var(--header-logo-link-display); position: var(--header-logo-link-position); top: var(--header-logo-link-top); left: var(--header-logo-link-left) }

29. Nav underline animation → styles/29-style.css

--nav-item-link-hover: var(--color-white)

.nav .nav-link::before { content:""; position:absolute; top:0; left:0; background: var(--color-white); width:0; height:2rem }

.nav .nav-item:hover .nav-link::before { background: var(--color-primary); width:100% }

30. Works card overlay → styles/30-style.css

.card-work .card-outer { position:relative; overflow:hidden }

.card-work .card-image img { height:30rem; width:100%; object-fit:cover; vertical-align:bottom }

.card-work .card-inner { position:absolute; top:-0.1rem; left:-0.1rem; right:-0.1rem; z-index:1 }

.card-work:hover .card-inner { background: rgba(0,0,0,.7) }

.card-work .card-title { text-align:center; margin:0; opacity:0; height:100%; position:relative }

.card-work .card-title a { display:block; text-decoration:none; padding-top:45% }

.card-work .card-title a::after { content:""; position:absolute; top:0; right:0; bottom:0; left:0 }

.card-work:hover .card-title { opacity:1 }

31. Quote decoration → styles/31-style.css

.card-testimonial .card-quote { position:relative }

.card-testimonial .card-quote::before { content:"\201C"; position:absolute; top:-4.5rem; left:-1rem; color:#efeded; font-size:10rem; z-index:-1 }

32. Transitions → styles/32-style.css

Vars:

--transition-duration: .3s

--transition-cubic-bezier: cubic-bezier(0.17, 0.67, 0, 1.01)

.card-work:hover .card-image { transform: scale(1.2); transition: var(--transition-duration) var(--transition-cubic-bezier) }

.card-work:hover .card-outer { transform: scale(0.95) }

.nav .nav-link::before { transition: var(--transition-duration) var(--transition-cubic-bezier) }

.button:hover { transition-duration: var(--transition-duration); transition-property: color, background-color }

.card-work .card-inner { transition: var(--transition-duration) var(--transition-cubic-bezier) }

🔍 Validation & Tips

Precision matters: class names, dashes, casing—follow specs exactly.

Only some tasks require W3C validation. Respect “Does not need to pass W3C”.

Keep variables in :root and reuse them—this is the main learning goal.

For rem: with html { font-size: 62.5% }, 1rem = 10px (easier mental math).

For float grids: always apply a clearfix (.row::after) to avoid collapsed parents.

🧪 How to Run

Open index.html in Chrome.
Change the CSS link to point to the task you’re testing, e.g.:

<link rel="stylesheet" href="styles/19-style.css">

📜 License / Attribution

This is for educational purposes as part of Holberton School – Foundations v2.1 – Advanced CSS.
Logos and images belong to their respective owners. Use Unsplash images per their license.
