# Revalix – Physiotherapy & Performance Clinic

Production-ready static website for Revalix Physiotherapy.

## Project Structure

```
revalix/
├── index.html          # Main HTML entry point
├── css/
│   └── style.css       # All styles
├── js/
│   └── main.js         # All JavaScript (hero animation, body map, nav, form)
├── images/
│   ├── brand_logo_white.png   # White logo — use on dark backgrounds
│   ├── brand_logo_black.png   # Black logo — use on light backgrounds
│   ├── submark_white.png      # Icon mark — white version
│   ├── submark_black.png      # Icon mark — black version (also used as favicon)
│   └── body_map.svg           # T-pose anatomical SVG body diagram
└── README.md
```

## Getting Started

### Option 1 — Open locally
Just open `index.html` in any browser. No build step needed.

### Option 2 — Local dev server (recommended)
```bash
# Using Python
python3 -m http.server 3000
# Then open http://localhost:3000

# Using Node / npx
npx serve .
```

### Option 3 — Deploy to Netlify (free)
1. Go to [netlify.com](https://netlify.com) and sign up
2. Drag and drop the entire `revalix/` folder onto the Netlify dashboard
3. Done — live in seconds with HTTPS

### Option 4 — Deploy to Vercel (free)
```bash
npm i -g vercel
cd revalix
vercel
```

### Option 5 — GitHub Pages (free)
1. Push this folder to a GitHub repo
2. Go to Settings → Pages → Deploy from branch `main`
3. Your site is live at `https://yourusername.github.io/revalix`

## Dependencies

All loaded via CDN — no npm install needed:
- [Three.js r128](https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js) — hero particle animation
- [Google Fonts](https://fonts.google.com) — Playfair Display + Outfit

## Sections

| Section | ID | Description |
|---|---|---|
| Hero | `#hero` | Full-screen with Three.js particle network |
| Treatments | `#treatments` | 7 specialty cards |
| Body Map | `#technology` | Interactive 5-slide anatomical diagram |
| Team | `#team` | Practitioners grid |
| Testimonials | — | Client reviews carousel |
| Contact | `#contact` | Booking enquiry form |

## Customisation

**Colours** — edit CSS variables at the top of `style.css`:
```css
:root {
  --navy:       #0d1f3c;
  --terra:      #c4622d;
  --terra-light:#e07a45;
  ...
}
```

**Contact form** — the form currently shows a success animation only.
To wire it up to a real backend, replace `handleSubmit()` in `main.js` with a `fetch()` POST to your endpoint (e.g. Formspree, Netlify Forms, or your own API).

**Body map regions** — edit the `SLIDES` array in `main.js` to add/remove pressure points or change descriptions.

## Browser Support

Chrome, Firefox, Safari, Edge — all modern browsers. IE not supported.
