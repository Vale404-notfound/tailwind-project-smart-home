# HomeSmart — Landing Page (Vite + Tailwind CSS)

**Demo:** https://tailwind-landing-page-smarthome.netlify.app/  

A responsive, accessible smart-home landing page built with **Vite** and **Tailwind CSS 3**.  
Highlights: an amber-themed navbar with mobile menu, gradient hero with overlapping images, feature “Qualities” tiles, partner logos grid, a promo/feature block with decorative rings, and a **floating-label contact form**. Dark mode follows the OS preference.

---

## Tech Stack
- **Vite** + TypeScript config (`vite.config.ts`)
- **Tailwind CSS 3** (+ **@tailwindcss/forms**)
- **PostCSS**, **Autoprefixer**, **cssnano**
- **Vanilla JS** (`main.js`)

---

## Quick Start

```bash
# install
pnpm install        # or: npm install

# dev
pnpm dev            # or: npm run dev

# production build
pnpm build          # or: npm run build

# preview built app
pnpm preview        # or: npm run preview
```

---

## Project Structure

```
├── assets
│   ├── app.svg
│   ├── couch.png
│   ├── dots.svg
│   ├── lamp.png
│   ├── logo.svg
│   ├── logomark.svg
│   ├── partner1.svg
│   ├── partner2.svg
│   ├── partner3.svg
│   ├── partner4.svg
│   ├── partner5.svg
│   ├── partner6.svg
│   ├── partner7.svg
│   └── table.png
├── favicon.svg
├── index.html
├── main.js
├── package.json
├── pnpm-lock.yaml
├── postcss.config.js
├── README.md
├── style.css
├── tailwind.config.js
└── vite.config.ts
```

---

## Tailwind Setup

- Dark mode uses **`media`** (default) — `dark:` classes follow the OS theme.
- Forms styled via **@tailwindcss/forms**.
- `style.css` contains:
  ```css
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
  ```
- Ensure `tailwind.config.js` scans your files:
  ```js
  module.exports = {
    content: ["./index.html", "./**/*.{js,ts}"],
    theme: { extend: { maxWidth: { '16': '16rem' } } },
    plugins: [require('@tailwindcss/forms')],
  }
  ```

---

## Accessibility

- Mobile menu uses proper ARIA (`aria-expanded`, `role="menubar"` / `menuitem"`).
- Consistent focus rings (`focus-visible:ring-4` + ring offsets).
- Informative `alt` text; decorative images can be `aria-hidden="true"`.

