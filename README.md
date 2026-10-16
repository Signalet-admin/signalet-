# Signalet — free EUR/USD signal PWA

## Included
- Installable dark-mode PWA.
- Calculates BUY/SELL/WAIT from uploaded OHLC CSV candles.
- Strategy: EMA20/50/200 trend + EMA20 pullback + RSI(14) confirmation.
- SL = 2 × ATR(14); TP = 2R.
- Local signal journal and CSV export.
- Simulated sample candles for testing the interface only.

## Important limitations
This version has **no live market feed**, does not continuously monitor prices, and does not execute trades. Sample data is simulated, not real market data. The strategy is unvalidated and not evidence of profitability. Verify every signal against current broker prices and use demo/manual execution only.

## Install on Android for free
PWA installation/service workers require HTTPS or localhost. Free GitHub Pages setup:
1. Create a public GitHub repository named `signalet`.
2. Upload `index.html`, `manifest.webmanifest`, `sw.js`, and `icon.svg` to its root.
3. Open **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
4. Open the published `https://YOUR-USERNAME.github.io/signalet/` URL in Chrome on Android.
5. Chrome menu ⋮ → **Add to Home screen** or **Install app**.

GitHub Pages terms may change. Do not put passwords, broker credentials, or API keys in a public repository.

## CSV format
Use columns like `time,open,high,low,close` and at least 205 chronological candles, preferably H1. Example:
```csv
time,open,high,low,close
2026-01-05 09:00,1.08300,1.08400,1.08250,1.08370
2026-01-05 10:00,1.08370,1.08420,1.08320,1.08390
```
