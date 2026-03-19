# 🛒 DealsHub — Amazon Associates Splash Page

A high-impact, fully responsive **affiliate marketing splash page** built for Amazon Associates. Designed to be submitted to traffic exchange networks like [EasyHits4U](https://www.easyhits4u.com) to drive clicks and generate affiliate commissions.

---

## 🔥 Live Preview

> Deploy to [Netlify Drop](https://app.netlify.com/drop) or [Tiiny.host](https://tiiny.host) by dragging `index.html` — get a public URL in under 60 seconds.

---

## ✨ Features

- **Animated gradient background** — eye-catching color shift that loops continuously
- **Floating blob effects** — layered depth with pink, yellow and green ambient blobs
- **Clickable Prime Deals badge** — top CTA linking directly to Amazon Prime Deals
- **Bold headline** with "Save up to 60% OFF" messaging
- **6 category chips** — each linked to its own SiteStripe affiliate URL
- **Live countdown timer** — 10-minute urgency loop to drive clicks
- **Pulsing CTA button** — glowing animated "Shop All Deals Now" button
- **6 product mini-cards** — one per category, each with its own affiliate link
- **Trust badges** — Prime Shipping, Secure Checkout, Reviews, Easy Returns
- **Amazon Associates disclosure** — FTC/Amazon policy compliant disclaimer
- **Fully responsive** — works on desktop, tablet, and mobile

---

## 📁 File Structure

```
dealshub-splash/
├── index.html       # Main splash page (single file, no dependencies)
└── README.md        # This file
```

> Everything is self-contained in a single HTML file. No frameworks, no build tools, no npm required.

---

## 🔗 Affiliate Links

All links use the Amazon Associates tag **`amazon000de-20`**.

| Element | Destination |
|---|---|
| ⚡ Top badge | Amazon Prime Deals — `amzn.to/3N9inEw` |
| 🛒 Main CTA button | `amazon.com/?tag=amazon000de-20` |
| 🔗 Secondary link | `amazon.com/?tag=amazon000de-20` |
| 🎧 Headphones chip + card | `amzn.to/4dukgGm` |
| 📱 Smartphones chip + card | `amzn.to/40EQcQU` |
| 🏠 Home & Kitchen chip + card | `amzn.to/4sjHUdl` |
| 👟 Sneakers chip + card | `amzn.to/4uS8M5Y` |
| ✨ Beauty chip + card | `amzn.to/3PhdtWy` |
| 💡 Tech & Gadgets chip + card | `amzn.to/4rBuHLB` |

---

## 🚀 Deployment

### Option 1 — Netlify Drop (Recommended, Free)
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag and drop `index.html`
3. Rename the file to `index.html` if needed
4. Copy your public URL (e.g. `https://amazing-name-123.netlify.app`)

### Option 2 — GitHub Pages
1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Your site will be live at `https://yourusername.github.io/repo-name`

### Option 3 — Tiiny.host (Free, no account needed)
1. Go to [tiiny.host](https://tiiny.host)
2. Upload `index.html`
3. Get instant public URL

---

## 📋 How to Use with EasyHits4U

1. Deploy the page using one of the options above and get your public URL
2. Log in to [EasyHits4U](https://www.easyhits4u.com)
3. Go to **My Sites → Add Site**
4. Paste your public URL
5. Set display time to **15–20 seconds** for maximum impact
6. Submit and start earning traffic credits

---

## 🛠 Customization

### Update your affiliate tag
Search and replace `amazon000de-20` with your own Amazon Associates tag across the file.

### Change a category link
Find the relevant `<a href="https://amzn.to/...">` tag and replace the URL with your new SiteStripe link.

### Add a new product card
Copy any `.mini-card` block inside `<div class="cards-row">` and update the emoji, title, stars, and `href` link.

### Change the countdown duration
In the `<script>` block at the bottom, edit this line:
```js
let t = 10 * 60; // 10 minutes — change to any number of seconds
```

---

## ⚖️ Amazon Associates Compliance

This page includes the required Amazon Associates disclosure:

> *"As an Amazon Associate, this site earns commissions from qualifying purchases through affiliate links. This is at no additional cost to you."*

All links use `rel="noopener sponsored"` as recommended by Amazon's policies.

---

## 🧰 Built With

- Pure **HTML5 / CSS3 / Vanilla JavaScript** — zero dependencies
- [Nunito](https://fonts.google.com/specimen/Nunito) + [Barlow Condensed](https://fonts.google.com/specimen/Barlow+Condensed) via Google Fonts
- CSS animations: gradient shift, blob float, fade-up reveals, CTA pulse glow

---

## 📄 License

This project is open source and free to use, modify, and redistribute for personal and commercial affiliate marketing purposes.

---

*Built for the Amazon Associates Program — affiliate tag `amazon000de-20`*
