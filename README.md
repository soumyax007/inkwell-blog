# Inkwell — Personal Blog
**CS106 · Fundamentals of Web Design · Assignment 2**

---

## Overview

Inkwell is a multi-page personal blog built with semantic HTML5 and a single external CSS stylesheet. The design follows an editorial/magazine aesthetic — warm off-white paper tones, Playfair Display headings, and Source Serif 4 body text — to create a reading-first experience.

---

## File Structure

```
blog-site/
├── index.html        Homepage with hero + 5-post grid
│   └──ASSETS/
│       └── blog.html         Full blog listing (all 5 posts)
│       └── about.html        Author bio page
│       └── contact.html      Contact page with styled form
├── css/
│   └── style.css     Single external stylesheet (all styling)
├── images/           (Placeholder — images loaded from Unsplash CDN)
│   └──soumya.png
└── README.md
```

---

## CSS Features Implemented

### Selectors
- **Element selectors** — `body`, `h1–h6`, `p`, `a`, `img`, `ul`, `blockquote`
- **Class selectors** — `.card`, `.container`, `.btn`, `.post-row`, etc.
- **ID selectors** — `#navToggle`, `#navMenu`, `#contactForm`, `#formSuccess`
- **Grouping selectors** — `h1, h2, h3, h4, h5, h6 { ... }`
- **Attribute selectors** — `input[type="text"]`, `input[type="email"]` targeted via `.form-group input`
- **Combinator selectors** — `.card:first-child .card-title`, `.hero-content > *`, `.nav-menu li a`

### Box Model
Margin, padding, border, width, and height are used throughout — notably on `.card`, `.card-body`, `.form-group input`, `.btn`, `.post-row`, and the hero section.

### Typography & Colors
- Custom Google Fonts: Playfair Display (display/headings), Source Serif 4 (body), JetBrains Mono (UI labels)
- Full color palette defined as CSS custom properties in `:root`
- Heading sizes scale with `clamp()` for fluid type
- Paragraph line-height and spacing set per context

### Navigation Bar
- Horizontal flex layout in the sticky header
- Hover and active states on all nav links
- Focus ring using `outline: 2px dashed`
- Collapses to hamburger on mobile (JS toggle)

### Layout System
- **CSS Grid** — 3-column posts grid on homepage; first card spans 2 columns (featured)
- **Flexbox** — header inner, nav menu, card-body, post-row-meta, footer-inner, form layout, contact-info-list
- Both systems used together across different sections

### Pseudo-classes
- `:hover` — cards, nav links, buttons, images, skill chips, footer links
- `:active` — `.btn-primary:active`, `a:active`
- `:focus` — all form inputs and nav links get visible focus rings
- `:nth-child` — `.contact-form .form-group:nth-child(even)` for alternating label color; `.posts-grid .card:first-child` for featured card

### Responsive Design
Three breakpoints via media queries:
- **≤ 900px (tablet)** — 2-column grid, about sidebar goes horizontal, contact stacks
- **≤ 600px (mobile)** — single column, nav collapses to hamburger menu

### Form Styling
Contact form on `contact.html` includes:
- Name, email, subject, message textarea, submit button
- `:focus` border glow, `:hover` border color change
- JS validation with success banner on submit

### Bonus Features
- **CSS animations** — `@keyframes fadeUp` on hero section with staggered `animation-delay` per child
- **Dark mode** — `@media (prefers-color-scheme: dark)` block remaps all CSS variables
- **Smooth scroll** — `scroll-behavior: smooth` on `html`

---

## How to Run

Open `index.html` in any modern browser. No build step or server required.

---

## Academic Integrity

All HTML and CSS written from scratch. Images sourced from [Unsplash](https://unsplash.com) (free to use). No templates used.

## Editing the final part

ALL HTML and CSS code are checked and all the links are woking fine