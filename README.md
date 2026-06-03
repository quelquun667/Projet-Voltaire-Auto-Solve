<div align="center">

# 🎓 Projet Voltaire Solver

**Automatically solve Projet Voltaire grammar exercises using React Fiber extraction — no AI, no API key.**

[![Latest Release](https://img.shields.io/github/v/release/quelquun667/Projet-Voltaire-Solver?style=for-the-badge&label=version&color=4A90D9)](https://github.com/quelquun667/Projet-Voltaire-Solver/releases/latest)
[![Releases](https://img.shields.io/github/release-date/quelquun667/Projet-Voltaire-Solver?style=for-the-badge&color=27AE60&label=released)](https://github.com/quelquun667/Projet-Voltaire-Solver/releases)
[![Stars](https://img.shields.io/github/stars/quelquun667/Projet-Voltaire-Solver?style=for-the-badge&color=F1C40F&label=stars)](https://github.com/quelquun667/Projet-Voltaire-Solver/stargazers)
[![Last Commit](https://img.shields.io/github/last-commit/quelquun667/Projet-Voltaire-Solver?style=for-the-badge&color=9B59B6&label=updated)](https://github.com/quelquun667/Projet-Voltaire-Solver/commits/main)

[![Manifest V3](https://img.shields.io/badge/Chrome-Manifest_V3-4285F4?style=flat-square&logo=google-chrome&logoColor=white)](https://developer.chrome.com/docs/extensions/mv3/)
[![License MIT](https://img.shields.io/badge/license-MIT-orange?style=flat-square)](LICENSE)

[🇫🇷 Version française](README.fr.md)

<img src="images/interface.png" alt="Extension interface" width="340"/>

</div>

---

## ✨ Features

| | Feature | Description |
|---|---|---|
| 🔍 | **React Fiber Extraction** | Reads answers directly from the app's internal React state — no guessing |
| ✅ | **Click-the-mistake** | Detects and clicks the wrong word, or "Il n'y a pas de faute" |
| 📝 | **Click-the-word** | Identifies and clicks the correct word (COD, past participle, etc.) |
| 📋 | **Drag & Drop** | Automatically places phrases in the correct columns (Tableau) |
| 📊 | **Per-session stats** | Correct / wrong / total counter, reset at each new session |
| ⏱️ | **Random delay** | Configurable min/max delay to mimic human behaviour |
| 🎲 | **Error rate** | Intentionally make mistakes at a configurable rate (0–50%) |
| 🕵️ | **Inspector mode** | Click any element to see its selector (debug) |
| 🌗 | **Dark / Light mode** | Adapts to your preference |
| 🔔 | **Auto update check** | Notified automatically when a new version is available |

---

## 🚀 Installation

1. Download the latest **[Release](https://github.com/quelquun667/Projet-Voltaire-Solver/releases/latest)** (`.zip` file) and extract it.
2. Open Chrome and go to `chrome://extensions/`.
3. Enable **Developer mode** (top-right toggle).
4. Click **Load unpacked**.
5. Select the `ProjetVoltaireExtension` folder (the one containing `manifest.json`).

> **Updating:** Download the new release, replace the folder, then click **Refresh** (↺) on `chrome://extensions/`.

---

## ⚙️ Usage

1. Open the extension popup (Chrome toolbar icon).
2. Toggle **Auto Solve** on.
3. Adjust the min/max delay if needed (default: 1 s – 2 s).
4. Navigate to a Projet Voltaire exercise — the extension takes care of the rest.

---

## 🛠️ How it works

Projet Voltaire is a React Native Web application. The extension injects two scripts:

- **`extractor.js`** runs in the page's MAIN world and traverses the React Fiber tree to extract exercise data (correct answer, type, sentence). It exposes this data via a hidden DOM element.
- **`content.js`** runs in the isolated extension world, reads that data, matches the displayed words to the right exercise, and simulates native pointer events to click the answer.

This approach requires no external API and works regardless of what the page looks like visually.

---

## 📈 Star History

<div align="center">
  <a href="https://star-history.com/#quelquun667/Projet-Voltaire-Solver&Date">
    <img src="https://api.star-history.com/svg?repos=quelquun667/Projet-Voltaire-Solver&type=Date" alt="Star History Chart" width="600"/>
  </a>
</div>

---

## ⚠️ Disclaimer

This tool is intended for educational and testing purposes only.
