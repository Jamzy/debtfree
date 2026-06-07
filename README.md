# DebtFree PWA

A Progressive Web App debt payoff tracker — installable on iPhone via Safari, works fully offline.

---

## Files

```
debt-pwa/
├── index.html       ← The entire app
├── manifest.json    ← PWA config (name, icon, display mode)
├── sw.js            ← Service worker (offline caching)
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

---

## Deploy to GitHub Pages (free, ~5 minutes)

1. Go to https://github.com/new and create a **public** repo named `debtfree` (or anything)
2. Upload all files: drag and drop the entire `debt-pwa` folder contents into the repo root
3. Go to **Settings → Pages**
4. Under "Source" select **Deploy from a branch** → branch: `main`, folder: `/ (root)`
5. Click Save — GitHub gives you a URL like `https://yourusername.github.io/debtfree`

Wait ~60 seconds, then open that URL on your iPhone in Safari.

---

## Install on iPhone

1. Open your GitHub Pages URL in **Safari** (must be Safari, not Chrome)
2. Tap the **Share** button (box with arrow)
3. Scroll down and tap **"Add to Home Screen"**
4. Tap **Add**

The app now lives on your home screen, runs fullscreen, and works **completely offline** after first load.

---

## Data storage

All your debt data is saved in the browser's `localStorage` — it persists between sessions automatically.
Data stays on your device only — nothing is sent anywhere.

---

## Update the app

Edit `index.html`, commit and push to GitHub. The service worker will pick up the new version on next reload.
To force an immediate cache bust, increment the cache name in `sw.js`: change `debtfree-v1` to `debtfree-v2`.
