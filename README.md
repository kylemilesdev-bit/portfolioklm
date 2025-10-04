# Thisis Kyle Miles — Software Developer Portfolio

![Static Badge](https://img.shields.io/badge/Stack-HTML%20%7C%20CSS%20%7C%20JavaScript-informational)
![Static Badge](<https://img.shields.io/badge/Lib-AOS%20(Animate%20On%20Scroll)-blue>)
![Static Badge](https://img.shields.io/badge/Icons-Font%20Awesome-9cf)
![Static Badge](https://img.shields.io/badge/Status-Active-brightgreen)

A fast, responsive, and accessible single‑page portfolio to showcase projects, skills, and contact info.

> **Live site:** _add your URL here_ > **Repo:** [https://github.com/kylemilesdev-bit/\_this-portfolio-repo](https://github.com/kylemilesdev-bit/_this-portfolio-repo)\_

---

## ✨ Features

- **Hero with typing effect** (`texts[]` in `script.js`) and parallax accent shape
- **Dark mode** with `localStorage` persistence
- **Sticky header** with auto‑hide on scroll + active link highlighting
- **Responsive nav** (hamburger on mobile)
- **Projects grid** with tech tags and link slots
- **Animated skill bars** via `IntersectionObserver`
- **Counters** for About stats (50+, 2+, ∞)
- **Contact form** with success modal & ripple feedback (mock submit — swap with your API)
- **Scroll‑to‑top** button
- **Lazy‑loading hook** for images (via `data-src` observer)
- **Konami code Easter egg** 🌈
- **AOS scroll animations** (fade/offset/duration presets)

## 🧱 Tech Stack & Dependencies

- **Frontend:** Vanilla HTML, CSS, JavaScript
- **Fonts:** Google Fonts — Inter
- **Icons:** Font Awesome 6 (CDN)
- **Animations:** AOS (CDN)
- **No build step required** — works as a static site

CDNs used in `index.html`:

```html
<link
  href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap"
  rel="stylesheet"
/>
<link
  rel="stylesheet"
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css"
/>
<link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet" />
<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
```

## 📂 Project Structure

```
.
├── index.html
├── style.css
├── script.js
└── attached_assets/
    ├── thisklmLOGO_1750965952082.jpg
    └── headshot_1750969646181.jpg
```

## 🚀 Getting Started (Local)

1. **Clone**

   ```bash
   git clone https://github.com/kylemilesdev-bit/_this-portfolio-repo_.git
   cd _this-portfolio-repo_
   ```

2. **Open** `index.html` in your browser (double‑click or use a tiny server):

   ```bash
   npx serve .            # or: python3 -m http.server 5173
   ```

No npm install/build needed.

## 🌐 Deploy

Any static host works:

### GitHub Pages

1. Push the repo to GitHub
2. Settings → **Pages** → Deploy from **main** (root)

### Netlify

- Drag‑and‑drop the folder, or connect the repo (no build command)

### Vercel

- "Add New Project" → Import repo → Framework **Other** → Output dir: `/`

## ⚙️ Configuration & Customization

### Typing Text (Hero)

In `script.js`, edit the rotating titles:

```js
const texts = [
  "Student.",
  "Developer.",
  "Problem Solver.",
  "Creative Thinker.",
];
```

### Skills

Set the displayed percent via the `data-width` attribute in `style.css`/HTML:

```html
<div class="skill-progress" data-width="80"></div>
```

### Projects

Edit the cards in `index.html` (title, description, tech tags, links). Replace placeholders with real **Live Demo** and **GitHub** URLs.

### Contact Info

Update the email/phone/location blocks in the **Contact** section and footer links:

```html
<a href="https://github.com/kylemilesdev-bit" target="_blank" rel="noopener">
  <a href="https://linkedin.com/in/kylemiles" target="_blank" rel="noopener"></a
></a>
```

### Contact Form Submission

Currently simulated with `setTimeout` for a success modal. To make it real:

- **Formspree**: set `action="https://formspree.io/f/yourid"` and `method="POST"`; remove JS mock
- **Netlify Forms**: add `data-netlify="true" name="contact"` to `<form>` and include a hidden `form-name` input
- **Custom API**: replace the mock in `script.js` with a `fetch()` call

## 🧰 Developer Notes

- **Dark mode** toggles `data-theme="dark"` on `<body>` and swaps icon
- **Active nav link** updates on scroll against section offsets
- **Header** gets `.scrolled` class (style as needed)
- **Lazy images**: any `<img>` with `data-src` will be swapped when visible (add that attribute to use it)
- **Performance**: scroll handlers are throttled; animations respect `transition` tokens

## 🔐 Accessibility & SEO

- Semantic landmarks: `<header>`, `<nav>`, `<section>`, `<footer>`
- Sufficient color contrast; focus styles via default UA + hover states
- `aria-label` on buttons (e.g., theme toggle, scroll‑top)
- Suggested meta tags (add to `<head>`):

```html
<meta
  name="description"
  content="Thisis Kyle Miles — Software Developer Portfolio"
/>
<meta property="og:title" content="Thisis Kyle Miles — Software Developer" />
<meta
  property="og:description"
  content="Projects, skills, and contact information."
/>
<meta property="og:image" content="https://your-cdn.com/og.png" />
<meta name="twitter:card" content="summary_large_image" />
```

## 🧪 Testing (optional)

- Lighthouse for performance/SEO/a11y
- Manual checks for mobile nav, theme persistence, and form modal

## 🗺️ Roadmap Ideas

- Project data as JSON + render via JS
- Tag filters / search
- Blog section (Markdown)
- Real contact endpoint + validation
- Replace CSS with Tailwind (optional)

## 📄 License

MIT — see `LICENSE`.

## 👋 Author

**Kyle Miles** — [GitHub](https://github.com/kylemilesdev-bit) • [LinkedIn](https://linkedin.com/in/kylemiles) • [kylemiles1020@gmail.com](mailto:kylemiles1020@gmail.com)

---

### Screenshots (optional)

Drop 1–2 images or GIFs here showing the hero, projects grid, and dark mode.
