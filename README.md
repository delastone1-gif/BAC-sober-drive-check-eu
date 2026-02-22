<p align="center">
  <img src="https://em-content.zobj.net/source/apple/391/wine-glass_1f377.png" width="80" alt="EuroBAC logo">
</p>

<h1 align="center">EuroBAC</h1>

<p align="center">
  <strong>Blood Alcohol Calculator for European drivers</strong><br>
  Estimate your BAC, compare legal limits across countries, and calculate rest time before driving.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="MIT License">
  <img src="https://img.shields.io/badge/languages-FR%20%7C%20EN-orange.svg" alt="FR | EN">
  <img src="https://img.shields.io/badge/zero-dependencies-green.svg" alt="Zero dependencies">
</p>

---

## What is EuroBAC?

EuroBAC is a single-page, client-side blood alcohol concentration (BAC) estimator designed for European drivers. It helps you understand how different drinks affect your BAC and how long you need to wait before legally driving in various European countries.

**Everything runs in your browser. No data is sent anywhere.**

## Features

- **4 drink types** with adjustable quantities: beer (33cl/5%), wine (15cl/13%), champagne (12.5cl/12%), spirits (4cl/40%)
- **6 European countries** with accurate legal limits: Denmark, Sweden, France, Norway, Germany, United Kingdom
- **Novice driver toggle** that applies stricter limits per country (e.g. 0.20 g/L in France, 0.00 g/L in Germany)
- **Rest time calculator** showing exactly how long to wait and the clock time when you can legally drive, per country
- **Detailed breakdown** of pure alcohol consumed per drink type
- **Visual BAC gauge** with color-coded status (safe / warning / danger)
- **Bilingual interface** (French / English) with one-click language switching
- **Profile settings**: sex, weight, stomach status (empty/full), time elapsed
- **Fully responsive** design for mobile and desktop

## Novice / Young Driver Limits

| Country | Standard | Novice |
|---------|----------|--------|
| 🇩🇰 Denmark | 0.50 g/L | 0.20 g/L (first 3 years) |
| 🇸🇪 Sweden | 0.20 g/L | 0.20 g/L (same for all) |
| 🇫🇷 France | 0.50 g/L | 0.20 g/L (probationary, 3 years) |
| 🇳🇴 Norway | 0.20 g/L | 0.20 g/L (same for all) |
| 🇩🇪 Germany | 0.50 g/L | 0.00 g/L (under 21 or first 2 years) |
| 🇬🇧 United Kingdom | 0.80 g/L | 0.80 g/L (no novice limit) |

## How It Works

The calculator uses the **Widmark formula** to estimate BAC:

```
BAC (g/L) = (alcohol_grams x absorption_factor) / (body_weight x distribution_ratio) - (elimination_rate x hours)
```

Key parameters:
- **Distribution ratio (r)**: 0.68 for men, 0.55 for women
- **Absorption factor**: 1.0 (empty stomach), 0.8 (full stomach)
- **Elimination rate**: 0.15 g/L per hour (average)
- **Alcohol density**: 0.789 g/mL

## Getting Started

EuroBAC is a single HTML file with zero dependencies. Just open it in any browser.

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/eurobac.git

# Open in browser
open eurobac.html
```

Or simply download `eurobac.html` and double-click it.

### Deploy to GitHub Pages

1. Push `eurobac.html` as `index.html` to your repo
2. Go to **Settings > Pages**
3. Select the branch and root folder
4. Your calculator is live at `https://YOUR_USERNAME.github.io/eurobac/`

## Tech Stack

- Vanilla HTML / CSS / JavaScript
- No frameworks, no build step, no dependencies
- Google Fonts: [DM Sans](https://fonts.google.com/specimen/DM+Sans) + [Fraunces](https://fonts.google.com/specimen/Fraunces)

## Disclaimer

> This calculator provides an **estimation** based on the Widmark formula. Actual BAC varies based on metabolism, health conditions, medications, fatigue, and many other individual factors. **Never drive if you have any doubt.** When in doubt, use a certified breathalyzer. Legal limits sourced from the European Transport Safety Council (ETSC) and WHO (2025).

## Contributing

Contributions are welcome! Some ideas:
- Add more European countries
- Add more drink types (cocktails, shots, pints)
- Add a dark/light theme toggle
- Improve accessibility (ARIA labels, keyboard navigation)
- Add more languages (Danish, German, Swedish, Norwegian)

## License

[MIT](LICENSE) -- free to use, modify, and distribute.

---

<p align="center">
  Made with 🍷 in Copenhagen
</p>
