# Vlad’s Jewelers

A snazzy, single-page static e-commerce **showcase** for a luxury jewelry brand — built to drop straight into **GitHub Pages**. Everything (sample products + admin state) runs in-memory and via `localStorage` for demonstration; it can later be upgraded to a full-stack app.

## ✨ Features

- **Luxury aesthetic** — deep charcoal theme, elegant serif headings, gold/champagne (`#D4AF37`) accents.
- **Sticky nav + hero banner** introducing the brand.
- **Live search & filter** — filters products by title or description in real time.
- **Purchase integration** on every card:
  - **Buy via Venmo** → opens the Venmo profile/payment link.
  - **Inquire via Email** → `mailto:` with the subject pre-filled `Inquiry: [Product Name]`.
- **Hidden admin dashboard ("Vlad’s Panel")**:
  - Hidden from regular users by default.
  - Unlock via the subtle **◆ diamond** button in the footer, **or** the secret combo **Ctrl/Cmd + Shift + V**.
  - Log in with username **`Vlad`** (case-insensitive).
  - Add products (Title, Price, Description, Image URL, Venmo Link) — new items **prepend** to the gallery and **persist** in `localStorage`.
  - Reset to the default collection at any time.
- **Fully responsive** with smooth hover effects (image zoom + gold glow).
- Seeded with **10 realistic high-end products** using Unsplash placeholder imagery.

## 🚀 Usage

1. Open `index.html` locally in any browser, **or**
2. Push to GitHub and enable **Settings → Pages → Deploy from branch** (root `/`).

No build step required — Tailwind is loaded via CDN.

## 🔧 Customize

Edit the `OWNER` config near the top of the `<script>` block in `index.html`:

```js
const OWNER = {
  venmo: 'https://venmo.com/u/Vlads-Jewelers',
  email: 'vlad@example.com',
  adminUsername: 'vlad',
};
```

Replace the `SEED_PRODUCTS` array to change the default catalog.

> **Note:** The "admin login" is a client-side demo gate only — it is **not** real security. Treat it as a UI demonstration until you add a real backend.
