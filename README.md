<div align="center">

# 🏔️ Parallax Effect Website

**A hands-on CSS learning project exploring depth, layering, and scroll-driven visual design.**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)](https://siddharth-parallex-effect.netlify.app/)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Status](https://img.shields.io/badge/Status-Learning%20Project-blue?style=for-the-badge)

[**View Live Demo**](https://siddharth-parallex-effect.netlify.app/) · [**Report a Bug**](https://github.com/siddharthkumarrai/parallex_effect-_websites/issues) · [**Request a Feature**](https://github.com/siddharthkumarrai/parallex_effect-_websites/issues)

</div>

---

## 📖 Table of Contents

- [About the Project](#-about-the-project)
- [Live Demo](#-live-demo)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [How It Works](#-how-it-works)
- [What I Learned](#-what-i-learned)
- [Getting Started](#-getting-started)
- [Customization](#-customization)
- [Deployment](#-deployment)
- [Roadmap](#-roadmap)
- [Author](#-author)
- [Acknowledgements](#-acknowledgements)

---

## 📌 About the Project

> *Parallax is the observed displacement of an object caused by the change of the observer's point of view.*

This repository is a **single-page adventure-themed website** built with **pure HTML and CSS** (no frameworks, no JavaScript). It was created while learning the **core fundamentals of CSS and front-end design**, with the goal of understanding how layered visuals and different scroll behaviours can create an illusion of depth on the web.

The page opens with a layered hero section (a background image, a foreground image, and a bold **ADVENTURE** headline) and then continues into content sections about **Biking**, **Para Gliding**, and **Surfing**, each separated by a full-width image band.

This project is intentionally simple. The point is to master the building blocks before moving on to larger projects.

## 🌐 Live Demo

**👉 [siddharth-parallex-effect.netlify.app](https://siddharth-parallex-effect.netlify.app/)**

Scroll through the page to see the parallax effect in action.

<!-- Add a screenshot or GIF of the site here, for example:
<p align="center">
  <img src="./screenshot.png" alt="Parallax Effect Website preview" width="800">
</p>
-->

## ✨ Features

- **Layered hero section**: separate background and foreground images stacked with a large headline between them to create depth.
- **Parallax image bands**: full-width image sections (Biking, Para Gliding, Surfing) that separate the text content.
- **Clean typographic hierarchy**: distinct styles for the hero title, section headings, band headings, and body text.
- **Zero dependencies**: no build step, no package manager, no JavaScript. Open the file and it works.
- **Responsive viewport setup**: includes the `viewport` meta tag as the foundation for mobile-friendly layouts.
- **Semantic structure**: content organised with `section`, `h1`/`h2`, and `p` elements.

## 🛠️ Tech Stack

| Technology | Purpose |
| --- | --- |
| **HTML5** | Page structure and semantic markup |
| **CSS3** | Layout, layering, typography, and the parallax effect |
| **Netlify** | Static hosting and deployment |
| **Git & GitHub** | Version control and source hosting |

## 📁 Project Structure

```
parallex_effect-_websites/
├── index.html            # Page markup: hero + content sections
├── style.css             # All styling, including the parallax effect
├── background.jpg.jpg    # Hero background layer
├── foreground.jpg.png    # Hero foreground layer (transparent PNG)
├── biking.jpg            # Image for the "Biking" band
├── para.jpg              # Image for the "Para Gliding" band
├── surfing.jpg           # Image for the "Surfing" band
└── README.md             # Project documentation
```

## ⚙️ How It Works

### Page anatomy

```
.wrapper
├── .container                  ← Hero
│   ├── img.background          ← Back layer
│   ├── img.foreground          ← Front layer
│   └── h1  "ADVENTURE"         ← Headline placed between the layers
│
└── section                     ← Scrolling content
    ├── h2.hedsec               "ADVENTURE TIME"
    ├── p.text                  Intro copy
    ├── div.bg.bg1 > h2.des     "BIKING"        (image band)
    ├── p.text
    ├── div.bg.bg2 > h2.des     "PARA GLIDING"  (image band)
    ├── p.text
    ├── div.bg.bg3 > h2.des     "SURFING"       (image band)
    └── p.text
```

### The core idea

Parallax works by making layers of a page appear to move at **different rates** as the user scrolls. Because nearer layers seem to move faster than distant ones, the brain reads the page as having depth.

In this project the effect is built from three ingredients:

1. **Layered images**: the hero stacks a background image and a foreground cut-out so the headline appears to sit *between* them.
2. **Image bands**: `.bg` blocks (`.bg1`, `.bg2`, `.bg3`) act as visual dividers between text sections and carry the scroll effect.
3. **Stacking and positioning**: CSS positioning and `z-index` control which layer sits in front of which.

## 🎓 What I Learned

This project served as a practice ground for several fundamental CSS concepts:

<!-- Trim or edit this list so it matches exactly what your style.css uses. -->

- **The box model**: how `margin`, `padding`, `border`, and content size interact.
- **Positioning**: `relative`, `absolute`, and `fixed` positioning, and when to use each.
- **Layering with `z-index`**: controlling stacking order between the background, headline, and foreground.
- **Background properties**: `background-image`, `background-size`, `background-position`, and `background-attachment`.
- **Viewport units**: sizing sections relative to the screen with `vh` and `vw`.
- **Typography**: font sizing, weight, letter-spacing, and text alignment for a strong visual hierarchy.
- **Class-based styling**: reusable classes (`.bg`, `.text`, `.des`) with modifier classes (`.bg1`, `.bg2`, `.bg3`).
- **Project organisation**: separating structure (HTML) from presentation (CSS).
- **Deployment**: publishing a static site on Netlify from a GitHub repository.

## 🚀 Getting Started

### Prerequisites

You only need a modern web browser. No installation is required.

### Run locally

**1. Clone the repository**

```bash
git clone https://github.com/siddharthkumarrai/parallex_effect-_websites.git
```

**2. Move into the project folder**

```bash
cd parallex_effect-_websites
```

**3. Open the site**

Double-click `index.html`, or serve it with a local server (recommended):

```bash
# Using Python
python -m http.server 8000

# Or using Node.js
npx serve .
```

Then visit `http://localhost:8000` in your browser. If you use VS Code, the **Live Server** extension also works well.

## 🎨 Customization

| I want to... | Do this |
| --- | --- |
| Change the hero images | Replace `background.jpg.jpg` and `foreground.jpg.png`, or update the `src` in `index.html` |
| Change a band image | Replace `biking.jpg`, `para.jpg`, or `surfing.jpg`, or update the URL in `style.css` |
| Edit the headline | Change the text inside the `<h1>` in `index.html` |
| Add a new section | Duplicate a `.bg` block and `p.text` pair, add a `.bg4` class, and give it a background image in `style.css` |
| Change fonts or colours | Edit the typography and colour rules in `style.css` |

> 💡 **Tip:** For the foreground layer, use a **transparent PNG** with the subject cut out, so the headline can appear to sit behind it.

## ☁️ Deployment

This site is a static site and is deployed on **Netlify**.

1. Push the project to GitHub.
2. In Netlify, choose **Add new site → Import an existing project**.
3. Select this repository.
4. Leave the build command empty and set the publish directory to the repository root (`/`).
5. Click **Deploy**.

Every push to `main` will automatically redeploy the site.

## 🗺️ Roadmap

Planned improvements as my skills grow:

- [ ] Add descriptive `alt` text to all images for accessibility
- [ ] Rename image files to clean names (for example, `background.jpg`, `foreground.png`)
- [ ] Make the layout fully responsive with media queries
- [ ] Disable or simplify the effect on mobile and for `prefers-reduced-motion` users
- [ ] Add a sticky navigation bar with smooth scrolling
- [ ] Add hover and reveal animations using CSS transitions
- [ ] Add an image-optimisation pass (WebP, `loading="lazy"`)
- [ ] Rebuild a scroll-speed variant using JavaScript for comparison
- [ ] Add a screenshot or GIF preview to this README

## 👤 Author

**Siddharth Kumar Rai**

- GitHub: [@siddharthkumarrai](https://github.com/siddharthkumarrai)
- Live project: [siddharth-parallex-effect.netlify.app](https://siddharth-parallex-effect.netlify.app/)

## 🙏 Acknowledgements

- [MDN Web Docs](https://developer.mozilla.org/) for CSS references
- [Netlify](https://www.netlify.com/) for free static hosting
- The wider front-end community for parallax tutorials and inspiration

---

<div align="center">

⭐ If this project helped you learn something, consider giving it a star!

*Built while learning the fundamentals of CSS and front-end design.*

</div>
