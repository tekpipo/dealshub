# 🛒 DealsHub — Amazon Associates Splash Page

A high-impact, fully responsive **affiliate marketing splash page** built for Amazon Associates. Designed for traffic exchange networks like [EasyHits4U](https://www.easyhits4u.com), featuring a live visitor counter, real-time stats panel, geo-detected visitor notifications, and animated category links — all in a **single HTML file with zero dependencies**.

---

## 🔥 Live Preview

> Deploy to [Netlify Drop](https://app.netlify.com/drop) by dragging `index.html` — get a public URL in under 60 seconds.

---

## ✨ Features

### 🎨 Design & UX
- Animated gradient background that shifts continuously (orange → blue → purple)
- Floating ambient blob effects for depth (pink, yellow, green)
- Staggered fade-up reveal animations on page load
- Pulsing CTA button with glow ring animation
- Fully responsive — desktop, tablet, and mobile

### 📊 Live Visitor Tracking *(New)*
- **Fixed top bar** — always visible, shows online users, today's count, total visits, and average time on page
- **Visitor ticker** — bottom-left notification that pops up every 8–18 seconds showing a visitor joining from a real city/country (e.g. `🇺🇸 New York, US just visited`)
- **Stats panel** — collapsible bottom-right panel with online count, daily/total visits, avg session duration, click count, and top 4 countries with progress bars
- **Geo detection** — detects the real visitor's country and city via IP on arrival and shows a personalized welcome notification
- **Click tracking** — counts every affiliate link click during the session
- **Session duration** — records how long each visitor stays; updates every 10 seconds and on tab close
- **All data persists** via `localStorage` across visits in the same browser

### 🔗 Affiliate Links
- Top badge linking to Amazon Prime Deals
- 6 category chip pills (Headphones, Smartphones, Home & Kitchen, Sneakers, Beauty, Tech & Gadgets)
- 6 product mini-cards with individual SiteStripe links
- Main CTA button + secondary text link
- 10-minute urgency countdown timer (loops)
- Trust badges (Prime Shipping, Secure Checkout, Reviews, Easy Returns)
- Amazon Associates FTC-compliant disclosure footer

---

## 📁 File Structure

```
dealshub/
├── index.html    # Complete splash page — single self-contained file
└── README.md     # This file
```

> No frameworks. No npm. No build step. Just open `index.html` in any browser.

---

## 🔗 Affiliate Links Reference

All links use Amazon Associates tag **`amazon000de-20`**.

| Element | Link |
|---|---|
| ⚡ Top badge | Amazon Prime Deals — `amzn.to/3N9inEw` |
| 🛒 Main CTA button | `amazon.com/?tag=amazon000de-20` |
| 🔗 Secondary link | `amazon.com/?tag=amazon000de-20` |
| 🎧 Headphones | `amzn.to/4dukgGm` |
| 📱 Smartphones | `amzn.to/40EQcQU` |
| 🏠 Home & Kitchen | `amzn.to/4sjHUdl` |
| 👟 Sneakers | `amzn.to/4uS8M5Y` |
| ✨ Beauty | `amzn.to/3PhdtWy` |
| 💡 Tech & Gadgets | `amzn.to/4rBuHLB` |

---

## 📊 Visitor Tracking — How It Works

Since this is a static HTML file (no server), all tracking is client-side using `localStorage`. Here's what gets tracked per browser:

| Data Point | How it's collected |
|---|---|
| Total visits | Incremented on every page load |
| Visits today | Resets daily using `Date.toDateString()` |
| Online users now | Calculated from total visits with a natural fluctuation algorithm |
| Session duration | Saved every 10s and on `beforeunload` |
| Average time | Mean of all recorded session durations |
| Clicks | Tracked on every `[data-track]` affiliate link click |
| Country / City | Detected via `ipapi.co` free API (no key required) |
| Top countries | Ranked and stored as a frequency map |

> **Note:** Because `localStorage` is per-browser, each unique device/browser maintains its own stats. For cross-device analytics, integrate with a free service like [Plausible](https://plausible.io), [Umami](https://umami.is), or Google Analytics 4.

---

## 🚀 Deployment

### Option 1 — Netlify Drop *(Recommended, Free)*
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag and drop `index.html`
3. Copy your public URL (e.g. `https://amazing-name-123.netlify.app`)

### Option 2 — GitHub Pages *(Free, from this repo)*
1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Live at `https://yourusername.github.io/repo-name`

### Option 3 — Tiiny.host *(Instant, no account)*
1. Go to [tiiny.host](https://tiiny.host)
2. Upload `index.html`
3. Get instant public URL

---

## 📋 Using with EasyHits4U

1. Deploy using one of the options above and copy your public URL
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
Find the `<a href="https://amzn.to/...">` for that chip or card and replace the URL with your new SiteStripe link.

### Add a new product card
Copy any `.mini-card` block inside `<div class="cards-row">` and update the emoji, title, stars, and `href`. Add `data-track="card"` to the button to track clicks.

### Change the countdown duration
```js
let t = 10 * 60; // change 10 to any number of minutes
```

### Upgrade to real cross-device analytics
Add this snippet inside `<head>` to connect [Umami](https://umami.is) (free, open source, GDPR-friendly):
```html
<script async src="https://analytics.umami.is/script.js"
  data-website-id="YOUR-WEBSITE-ID"></script>
```
Or use the standard [Google Analytics 4](https://analytics.google.com) gtag snippet.

### Reset all stored stats
Open browser DevTools → Console and run:
```js
localStorage.removeItem('dh_stats');
localStorage.removeItem('dh_today');
location.reload();
```

---

## ⚖️ Amazon Associates Compliance

This page includes the required Amazon Associates disclosure in the footer:

> *"As an Amazon Associate (amazon000de-20), this site earns commissions from qualifying purchases through affiliate links. This is at no additional cost to you."*

All affiliate links use `rel="noopener sponsored"` per Amazon's link attribution guidelines.

---

## 🧰 Built With

- Pure **HTML5 / CSS3 / Vanilla JavaScript** — zero dependencies, zero frameworks
- [Nunito](https://fonts.google.com/specimen/Nunito) + [Barlow Condensed](https://fonts.google.com/specimen/Barlow+Condensed) via Google Fonts
- [ipapi.co](https://ipapi.co) — free IP geolocation API (no key required, 1k req/day)
- `localStorage` — client-side persistent stats storage
- CSS animations: gradient shift, blob float, fade-up reveals, CTA pulse glow, ticker slide-in/out

---

## 📄 License

Open source and free to use, modify, and redistribute for personal and commercial affiliate marketing purposes.

---

*Built for the Amazon Associates Program — affiliate tag `amazon000de-20`*
