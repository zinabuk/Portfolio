# Mohammed Farhan — Personal Portfolio

> **AI Engineer & Founder** · Chantilly, VA  
> [Live Site](https://github.com/Far-hantech/portfolio) · [Email](mailto:farhanay916@gmail.com)

---

## 📌 Overview

A world-class, single-file personal portfolio website for **Mohammed Farhan** — AI Engineer, Founder of [Studygy.io](https://studygy.io), and AI Icon Award 2026 recipient. Built for speed, aesthetics, and full mobile responsiveness.

Inspired by elite designer portfolios (editorial typography, cinematic hero sections, interactive project reveals), the site ships as a **zero-dependency single HTML file** — no build step, no framework, just open and run.

---

## ✨ Features

- **Custom loader animation** with staggered letter reveal
- **Hero section** — illustrated avatar, animated blob, scroll-triggered reveal
- **Diagonal skill marquees** — infinite scrolling skill tickers
- **Door-open project cards** — 3D perspective CSS animation on hover
- **Editorial experience timeline** — magazine-style layout
- **Animated stats strip** — count-up numbers
- **Skills cloud** — colored, rotated chips
- **Light / Dark mode** — toggle with smooth theme transitions
- **Custom cursor** — dot + ring with hover expand effects
- **Scroll progress bar** — top-of-page reading indicator
- **Fully mobile responsive** — tested at 390px, 480px, and 360px
- **Easter eggs** 🥚
  - Type `farhan` anywhere → color inversion
  - Konami code `↑↑↓↓←→←→BA` → terminal overlay

---

## 🗂 Project Structure

```
my portfolio/
├── index.html              # Main portfolio (single-file, all CSS + JS inline)
├── images/
│   ├── hero_avatar.png     # Profile avatar (extracted from original inline base64)
│   ├── avatar.png          # Original avatar asset
│   └── hero page.png       # Design reference screenshot
├── portfolio-app/          # Next.js companion app (optional — see below)
│   ├── app/
│   │   ├── page.tsx        # Main page
│   │   ├── layout.tsx      # Root layout + Google Fonts
│   │   └── globals.css     # Design system tokens
│   ├── components/ui/
│   │   ├── hero-parallax.tsx     # Parallax hero component
│   │   └── davincho-hero-1.tsx   # shadcn-compatible component
│   └── next.config.ts      # Remote image domains config
└── README.md
```

---

## 🚀 Quick Start

### Option 1 — Static HTML (recommended, zero setup)

```bash
# Clone the repo
git clone https://github.com/Far-hantech/portfolio.git
cd portfolio

# Open directly in your browser
open index.html
```

That's it. No dependencies, no build step. Works offline.

---

### Option 2 — Next.js App (advanced)

The `portfolio-app/` directory contains a full [Next.js](https://nextjs.org) project with TypeScript, Tailwind CSS, and shadcn/ui.

**Requirements**
- Node.js ≥ 18
- npm ≥ 9

```bash
cd portfolio-app

# Install dependencies
npm install

# Start development server
npm run dev
```

Then open [http://localhost:3000](http://localhost:3000).

**Build for production**
```bash
npm run build
npm start
```

---

## 🎨 Design System

| Token | Value | Usage |
|---|---|---|
| `--bg` | `#F7F3EC` | Page background (light) |
| `--text` | `#1A1501` | Primary text |
| `--accent` | `#E63311` | Red accent (light) / `#00DDFF` (dark) |
| `--blue` | `#1B5FFF` | Secondary blue |
| `--lime` | `#5AE600` | Green highlight |
| `--font-d` | Syne | Display / headings |
| `--font-b` | Plus Jakarta Sans | Body text |
| `--font-s` | DM Serif Display | Italic pull quotes |
| `--font-n` | Nunito | Project names |

---

## 🛠 Technologies Used

**Static site (`index.html`)**
- Vanilla HTML5 · CSS3 · JavaScript (ES6+)
- [GSAP 3](https://gsap.com) — scroll-triggered animations & loader
- [Font Awesome 6](https://fontawesome.com) — icons
- [Google Fonts](https://fonts.google.com) — Syne, Plus Jakarta Sans, DM Serif Display, Nunito
- Pure CSS: custom cursor, 3D door animation, marquees, morph blob, dark mode

**Next.js app (`portfolio-app/`)**
- [Next.js 14](https://nextjs.org) (App Router)
- [TypeScript](https://typescriptlang.org)
- [Tailwind CSS](https://tailwindcss.com)
- [shadcn/ui](https://ui.shadcn.com)
- [Framer Motion](https://www.framer.com/motion/) (`motion` package)

---

## 📱 Mobile Responsiveness

The site is tested and optimized across three breakpoints:

| Breakpoint | Target devices |
|---|---|
| `≤ 900px` | Large phones, tablets |
| `≤ 480px` | Standard phones (iPhone 14, Galaxy S23) |
| `≤ 360px` | Small/budget phones |

Key mobile behaviors:
- Hero avatar shrinks to top-center, text stacks below
- Name scales using `min(7.8vw, 2.65rem)` — never overflows
- Buttons stack full-width on small screens
- Decorative elements (orbit icons, background text, floating tags) are hidden
- Door-open project cards collapse to always-visible reveal mode (no hover required)

---

## ✏️ Customization

All content lives directly in `index.html`. Here's where to update things:

### Personal info
Search for these strings and replace:
- `Mohammed Farhan` — your name
- `farhanay916@gmail.com` — your email
- `Studygy.io` — your company/project
- `Chantilly, VA` — your location

### Avatar
Replace `images/hero_avatar.png` with your own photo. The image is cropped into a circle via CSS (`border-radius: 50%`).

### Projects (Door cards)
Find the `<!-- PROJECTS -->` section in the HTML and edit each `.door-card` block. Each card has:
- `.dp-accent` — emoji/icon
- `.dp-name` — project name
- `.dr-title` — card detail title
- `.dr-desc` — description
- `.dr-tags` — tech tags
- `.dr-link` — link URL

### Skills
Find the `<!-- SKILLS -->` section and add/remove `.skill-chip` elements.

### Experience
Find `<!-- EXPERIENCE -->` and edit the `.exp-item` blocks.

### Colors / Dark mode
Edit the CSS variables at the top of the `<style>` block:
```css
:root { --accent: #E63311; ... }
[data-theme="dark"] { --accent: #00DDFF; ... }
```

---

## 🚢 Deployment

### Netlify (drag & drop)
1. Go to [netlify.com](https://netlify.com)
2. Drag the entire `portfolio/` folder onto the deploy zone
3. Done — live in seconds

### GitHub Pages
1. Go to your repo → **Settings → Pages**
2. Set source to `main` branch, root `/`
3. GitHub will serve `index.html` automatically

### Vercel (Next.js app only)
```bash
cd portfolio-app
npx vercel
```

---

## 📄 License

MIT — free to use, modify, and deploy. Attribution appreciated but not required.

---

<p align="center">Built with ❤️ by <strong>Mohammed Farhan</strong> · AI Engineer & Founder</p>
