# Blog-Website  

![GitHub license](https://img.shields.io/github/license/imaakarsh/Blog-Website) ![GitHub stars](https://img.shields.io/github/stars/imaakarsh/Blog-Website) ![GitHub forks](https://img.shields.io/github/forks/imaakarsh/Blog-Website) ![GitHub last commit](https://img.shields.io/github/last-commit/imaakarsh/Blog-Website)  

> A clean, responsive static blog website built with vanilla HTML5 & CSS3. Perfect for personal portfolios, tech blogs, or any content‑driven site that needs a lightweight, zero‑dependency foundation.

---

## Table of Contents  

- [Overview](#overview)  
- [Features](#features)  
- [Tech Stack](#tech-stack)  
- [Architecture](#architecture)  
- [Getting Started](#getting-started)  
  - [Prerequisites](#prerequisites)  
  - [Installation](#installation)  
  - [Configuration](#configuration)  
- [Usage](#usage)  
- [Development](#development)  
- [Deployment](#deployment)  
- [Contributing](#contributing)  
- [Roadmap](#roadmap)  
- [Troubleshooting & FAQ](#troubleshooting--faq)  
- [License & Credits](#license--credits)  

---

## Overview  

**Blog-Website** is a minimalistic, fully responsive static site that showcases a personal blog layout. It ships with a single HTML page (`index.html`) and a CSS stylesheet (`style.css`). The design follows modern web standards, ensuring accessibility, fast load times, and easy customization.

**Why use this?**  
- No build tools or server‑side dependencies – just open the HTML file in any browser.  
- Ideal as a starter template for developers learning web fundamentals.  
- Easily hostable on any static‑site platform (GitHub Pages, Netlify, Vercel, etc.).

**Current version:** `v1.0.0` (January 2026)

---

## Features  

| Feature | Description | Status |
|---------|-------------|--------|
| **Responsive Layout** | Fluid grid that adapts from mobile to desktop. | ✅ Stable |
| **Semantic HTML5** | Proper use of `<header>`, `<nav>`, `<article>`, `<section>`, and `<footer>`. | ✅ Stable |
| **Customizable Theme** | Colors, fonts, and spacing are defined in CSS variables for easy theming. | ✅ Stable |
| **SEO‑Friendly** | Meta tags, Open Graph, and structured data placeholders. | ✅ Stable |
| **Accessibility** | Keyboard‑navigable, ARIA landmarks, and sufficient colour contrast. | ✅ Stable |
| **Dark Mode (optional)** | Toggleable dark theme via CSS class (`.dark`). | ⚙️ Experimental |
| **Image Placeholder** | `image.png` demonstrates how to embed hero images. | ✅ Stable |

---

## Tech Stack  

| Layer | Technology | Reason |
|-------|------------|--------|
| **Markup** | HTML5 | Semantic structure, native browser support. |
| **Styling** | CSS3 (Flexbox & Grid) | Modern layout techniques, no external libraries. |
| **Version Control** | Git + GitHub | Collaboration and CI badge generation. |
| **Hosting** | Any static‑site host (GitHub Pages, Netlify, Vercel) | Zero‑cost, instant deployment. |

---

## Architecture  

```
Blog-Website/
├── README.md          # This documentation
├── index.html         # Main page – contains HTML structure
├── style.css          # Global stylesheet – layout, theme, utilities
└── image.png          # Sample hero image used in the demo
```

- **`index.html`** – Contains the page skeleton, navigation, blog post placeholders, and footer. All content is static; replace the placeholder text with your own articles.  
- **`style.css`** – Holds all visual styling. CSS variables at the top (`:root`) allow quick theme changes.  
- **`image.png`** – Demonstrates how to embed responsive images; replace with your own assets.

---

## Getting Started  

### Prerequisites  

| Tool | Minimum Version |
|------|-----------------|
| Web browser (Chrome, Firefox, Safari, Edge) | Latest stable |
| Git (optional, for cloning) | 2.30+ |
| Node.js (optional, for live‑server) | 14+ |

> No additional runtime or build tools are required.

### Installation  

1. **Clone the repository** (or download the ZIP)  

   ```bash
   git clone https://github.com/imaakarsh/Blog-Website.git
   cd Blog-Website
   ```

2. **Open the site**  

   - **Option A – Directly**: Double‑click `index.html` or open it via `File → Open` in your browser.  
   - **Option B – Live Server (recommended for development)**  

     ```bash
     # If you have npm installed
     npx live-server
     ```

   The site will be served at `http://127.0.0.1:8080` (or similar) and will auto‑reload on file changes.

### Configuration  

| Variable | Description | Default |
|----------|-------------|---------|
| `--primary-color` | Main brand colour used for links, buttons, etc. | `#3498db` |
| `--background-color` | Page background colour (light theme) | `#ffffff` |
| `--text-color` | Primary text colour | `#333333` |
| `--font-family` | Global font stack | `'Helvetica Neue', Arial, sans-serif` |

These variables are defined at the top of `style.css` inside `:root`. Edit them to match your branding.

**Example `.env` (not required for static site, shown for completeness):**  

```dotenv
# No environment variables needed for this project.
```

---

## Usage  

### Basic Customization  

1. **Replace the hero image** – swap `image.png` with your own image and update the `<img>` `src` attribute in `index.html`.  
2. **Edit blog posts** – locate the `<article>` elements inside the `<section id="posts">` block and replace the placeholder titles, dates, and content.  
3. **Change the theme** – modify CSS variables in `style.css` or add the `.dark` class to the `<body>` tag to enable dark mode.

### Code Snippets  

**Adding a new post**

```html
<article class="post">
  <h2 class="post-title">Your New Post Title</h2>
  <p class="post-meta">January 15, 2026 • 5 min read</p>
  <p class="post-excerpt">
    Write a short excerpt that entices readers to click through...
  </p>
  <a href="your-post.html" class="read-more">Read more →</a>
</article>
```

**Toggling Dark Mode with JavaScript (optional)**

```html
<button id="theme-toggle">Toggle Dark Mode</button>

<script>
  const btn = document.getElementById('theme-toggle');
  btn.addEventListener('click', () => {
    document.body.classList.toggle('dark');
  });
</script>
```

### Screenshots  

![Blog Homepage Screenshot](image.png)

---

## Development  

| Task | Command |
|------|---------|
| **Run a local dev server** | `npx live-server` |
| **Lint CSS** (optional) | `npx stylelint "**/*.css"` |
| **Format HTML** (optional) | `npx prettier --write "**/*.html"` |

**Code Style Guidelines**  

- **HTML** – Use semantic tags, keep indentation to 2 spaces.  
- **CSS** – Follow the BEM naming convention (`block__element--modifier`).  
- **Comments** – Add descriptive comments for sections that may be confusing to future contributors.

**Debugging Tips**  

- Open the browser’s DevTools (F12) to inspect layout issues.  
- Use the “Elements” panel to experiment with CSS variable changes in real time.  

---

## Deployment  

### GitHub Pages (one‑click)  

1. Push your changes to the `main` branch.  
2. In the repository settings → **Pages**, set the source to `main` / `root`.  
3. GitHub will publish the site at `https://<username>.github.io/Blog-Website/`.

### Netlify (alternative)  

1. Sign in to Netlify and click **New site from Git**.  
2. Connect your GitHub repo, keep the build command empty, and set the publish directory to `/`.  
3. Netlify will automatically deploy on each push.

### Docker (for static serving)  

```dockerfile
# Dockerfile (optional)
FROM nginx:alpine
COPY . /usr/share/nginx/html
EXPOSE 80
```

```bash
docker build -t blog-website .
docker run -p 8080:80 blog-website
```

Visit `http://localhost:8080` to see the site.

---

## Contributing  

We welcome contributions! Follow these steps:

1. **Fork** the repository.  
2. **Create a feature branch**: `git checkout -b feat/your-feature`.  
3. **Make your changes** – ensure the site still builds and looks correct.  
4. **Run tests / lint** (if you added any).  
5. **Commit** with a clear message: `git commit -m "feat: add dark‑mode toggle"`.  
6. **Push** to your fork and open a **Pull Request** against `main`.  

### Pull Request Checklist  

- [ ] Code follows the style guidelines.  
- [ ] All new content is reflected in the README (e.g., new features).  
- [ ] No broken links or missing assets.  
- [ ] If you added new images, they are optimized (< 100 KB).  

---

## Roadmap  

- **v1.1** – Add optional Markdown-to-HTML pre‑processor for authoring posts.  
- **v1.2** – Implement a lightweight search index (Lunr.js).  
- **v2.0** – Convert to a JAMstack architecture with a headless CMS (e.g., Netlify CMS).  

---

## Troubleshooting & FAQ  

| Issue | Solution |
|-------|----------|
| **Images don’t load** | Verify the image path is correct and that the file resides in the repository root (or adjust the `src` attribute). |
| **Layout breaks on mobile** | Ensure you’re not overriding the `meta viewport` tag. The default is `<meta name="viewport" content="width=device-width, initial-scale=1">`. |
| **CSS changes not reflected** | Clear the browser cache or open the page in an incognito window. |
| **Live Server not starting** | Make sure Node.js is installed and run `npm install -g live-server` or use `npx live-server`. |
| **How to add a new page** | Duplicate `index.html`, rename it (e.g., `about.html`), update navigation links, and push the new file. |

**Need more help?** Open an issue on GitHub or contact the maintainer via the repository’s **Discussions** tab.

---

## License & Credits  

**License:** MIT License – see the [LICENSE](https://github.com/imaakarsh/Blog-Website/blob/main/LICENSE) file for details.  

**Author:** *Karsh* – [GitHub Profile](https://github.com/imaakarsh)  

**Acknowledgments**  

- Inspired by the “Simple Blog” template from the HTML5 Boilerplate project.  
- Icons from [Font Awesome](https://fontawesome.com) (used via CDN).  

---  

*Happy coding!* 🚀