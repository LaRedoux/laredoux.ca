# LaRedoux Official Digital Hub (laredoux.ca)

A production-ready artist website and digital hub serving as LaRedoux's central online presence as an independent musician. 

🔗 **Live Site:** [laredoux.ca](https://laredoux.ca)

---

## ✨ Key Features

* **Unified Digital Hub:** Anchors music releases, a CD and vinyl merchandise store, live-stream channels, voice/music coaching booking, and press assets.
* **Automated CI/CD Store Sync:** Utilizes a GitHub Actions automated workflow to fetch live product data via the Fourthwall API and keep inventory synchronized.
* **Custom 2006 MySpace Mode:** A nostalgic retro alternate theme toggle built with vanilla JavaScript and CSS class manipulation, with preference saved to `localStorage`.
* **Responsive Glassmorphism UI:** Modern, clean aesthetic built with CSS custom properties, flexbox/grid layouts, and robust mobile responsiveness.

---

## 🛠️ Tech Stack & Architecture

* **Frontend:** HTML5, CSS3, Vanilla JavaScript
* **Automation & CI/CD:** GitHub Actions (`sync-forthwall.yml`)
* **Integrations:** Fourthwall Storefront API, YouTube, Twitch, Discord, StreamElements
* **Hosting & Deployment:** GitHub Pages with custom CNAME and `.nojekyll` configuration

---

## ⚙️ Automated Store Synchronization

The repository features an automated GitHub Action that runs every 6 hours (and supports manual triggers via `workflow_dispatch`). It queries the Fourthwall API, updates the local JSON store in `assets/data/fourthwall-products.json`, and commits changes back to the repository only when products change.
