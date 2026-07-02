# Blackjack PWA

A mobile-first blackjack game with a basic strategy coach. Single-file HTML app that works offline as a Progressive Web App.

## Features

- Configurable shoe size (1, 2, 4, or 6 decks)
- Full blackjack rules: Hit, Stand, Double Down, Split, Late Surrender
- Dealer hits soft 17, blackjack pays 3:2
- Basic strategy coach with single-deck and multi-deck tables
- Persistent balance and statistics via localStorage
- Works fully offline after first load

## Deploy to Cloudflare Pages

1. Push this repo to the `streeter-lab/blackjack` GitHub repository
2. Go to [Cloudflare Dashboard](https://dash.cloudflare.com) > **Pages**
3. Click **Create a project** > **Connect to Git**
4. Select the `streeter-lab/blackjack` repository
5. Configure build settings:
   - **Framework preset**: None
   - **Build command**: *(leave empty)*
   - **Build output directory**: `/`
6. Click **Save and Deploy**

The site will be live at `https://blackjack.pages.dev` (or your custom domain).

## Install on iPhone

1. Open the deployed site in Safari
2. Tap the **Share** button (square with arrow)
3. Scroll down and tap **Add to Home Screen**
4. Tap **Add**

The app will launch in full-screen mode and work offline.

## Local Development

Open `index.html` directly in a browser, or serve it locally:

```
npx serve .
```

Note: The service worker requires HTTPS or localhost to register.

## Files

| File | Description |
|------|-------------|
| `index.html` | Complete game (HTML + CSS + JS inline) |
| `manifest.json` | PWA manifest for home screen install |
| `sw.js` | Service worker for offline caching |
