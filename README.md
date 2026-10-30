<div align="center">

# 🧹 Bulk Delete Chats for Google™ AI Mode

<p align="center">
  <strong>The history management tools Google™ AI Mode should have had.</strong><br>
  Bulk delete, pin, filter, and beautify your Google AI Mode chats with ease.
</p>

[![Version](https://img.shields.io/badge/version-1.2.2-blue.svg?style=flat-square)](https://github.com/rajeshc-git/aimode-extension)
[![Manifest](https://img.shields.io/badge/manifest-v3-green.svg?style=flat-square)](manifest.json)
[![Chrome](https://img.shields.io/badge/browser-Chrome%20137%2B-orange.svg?style=flat-square)](https://google.com/chrome)
[![Languages](https://img.shields.io/badge/languages-16%20supported-purple.svg?style=flat-square)](#-internationalization)
[![License](https://img.shields.io/badge/license-MIT-lightgrey.svg?style=flat-square)](LICENSE)

---

</div>

## 📖 Overview

Google's **AI Mode** (`?udm=50`) provides rich conversational search experiences, but managing large volumes of past chat history one-by-one is tedious.

**Bulk Delete Chats for Google™ AI Mode** transforms the chat history interface into a full-featured management dashboard. Select specific chats, filter by age, pin critical discussions to prevent accidental deletion, revoke public sharing links in bulk, and personalize your workspace with over 20 tailored themes.

---

## ✨ Features

### 🚀 Chat Management
- **Bulk Selection & Deletion:** Select multiple chats with checkboxes or choose "Select all" to delete in batches.
- **Pin Important Chats:** Pin key discussions to stay permanently pinned at the top and excluded from bulk deletion.
- **Age-Based Filtering:** Quick-select chats older than **7 days**, **30 days**, or **90 days**.
- **Automated Cleanup:** Set background auto-cleanup rules for past chats older than a specified duration.
- **Revoke Public Shared Links:** Find and delete all publicly shared chat links in a single click without losing local history.

### 🎨 20+ Aesthetic Page Themes
Personalize Google AI Mode with curated palettes, custom typography, and procedural SVG backdrops:

| Theme | Style | Description |
|---|---|---|
| **Paper** | Warm Editorial | Cream background, serif type (`Literata`), subtle paper grain texture |
| **Synthwave** | Neon Retro | Cyberpunk magenta/cyan glow, 80s gridlines, retro aesthetics |
| **Blueprint** | Technical | Deep architectural cyan with drafting grid lines and monospace fonts |
| **Fjord** | Clean Minimal | Crisp Nordic cool whites, subtle slate lines, and modern sans-serif |
| **Sakura** | Floral Soft | Gentle cherry-blossom pink with floating petal illustrations |
| **Vampire** | Dark High-Contrast | Deep purple-charcoal dark theme with vivid emerald highlights |
| **OLED Black** | True Black | Pure `#000000` dark mode optimized for OLED screens |
| *And 15+ more...* | | *Matcha, Amber CRT, Zen, Gazette, Netrunner, Moon Run, etc.* |

### 🔒 Privacy & Security First
- **Zero Data Collection:** Does not collect, transmit, or monitor chat contents or search queries.
- **Minimal Permissions:** Requires only the `storage` permission to store your local preferences and theme settings.
- **Secure Sandbox:** Operates using Manifest V3 isolated world scripts with CSP compliance.

---

## 🌍 Internationalization

Built with full multi-language support (16 languages) including native plural rules:

| | | | |
|:---:|:---:|:---:|:---:|
| 🇺🇸 English (`en`) | 🇷🇺 Русский (`ru`) | 🇺🇦 Українська (`uk`) | 🇩🇪 Deutsch (`de`) |
| 🇫🇷 Français (`fr`) | 🇪🇸 Español (`es`) | 🇮🇹 Italiano (`it`) | 🇧🇷 Português (`pt_BR`) |
| 🇳🇱 Nederlands (`nl`) | 🇵🇱 Polski (`pl`) | 🇹🇷 Türkçe (`tr`) | 🇻🇳 Tiếng Việt (`vi`) |
| 🇯🇵 日本語 (`ja`) | 🇰🇷 한국어 (`ko`) | 🇨🇳 简体中文 (`zh_CN`) | 🇹🇼 繁體中文 (`zh_TW`) |

---

## 🛠️ Installation

### Manual / Developer Mode (Chrome, Edge, Brave, Opera)

1. **Clone or download this repository:**
   ```bash
   git clone https://github.com/rajeshc-git/aimode-extension.git
   ```
2. Open your Chromium-based browser and navigate to the Extensions management page:
   * **Chrome / Brave:** `chrome://extensions`
   * **Edge:** `edge://extensions`
3. Toggle on **"Developer mode"** in the top-right corner.
4. Click **"Load unpacked"** in the top-left corner.
5. Select the `aimode-extension` project folder.
6. Navigate to [Google](https://www.google.com) and enter **AI Mode** (`?udm=50`) — the bulk management interface will appear automatically!

---

## 📂 Architecture

```
├── manifest.json            # Manifest V3 extension configuration
├── background.js            # Service worker (lifecycle & theme font distributor)
├── popup.html               # Extension popup UI
├── assets/                  # Popup CSS and bundled stylesheets
├── chunks/                  # Bundled popup logic (Vite chunk)
├── content-scripts/
│   ├── content.js           # Core chat list injector, selection UI, CRUD RPC
│   ├── content.css          # Chat interface styles, checkmarks, badges
│   ├── page-theme.js        # Theme injection engine & procedural SVG backgrounds
│   ├── xsrf.js              # Token bridge (MAIN world)
│   └── welcome.js           # Onboarding listener
├── fonts/                   # Bundled fonts (Geist & Theme Typography WOFF2)
├── icon/                    # Extension action icons (16, 32, 48, 96, 128px)
└── _locales/                # Localization catalogs (16 languages)
```

---

## ⌨️ How It Works

1. **Direct RPC Integration:** Communicates with Google's native internal `AimThreadsService` protocol to list, update, and delete chat threads reliably.
2. **XSRF Safety:** Extracts session tokens in page context to execute authorized batch actions securely on your behalf.
3. **Optimistic UI Updates:** Deleted or pinned items update instantaneously in the DOM with automatic fallback retry mechanisms on network hiccups.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## ⚠️ Disclaimer

*Google™ and Google AI Mode™ are trademarks of Google LLC. This extension is an independent open-source project and is not affiliated with, sponsored by, or endorsed by Google LLC.*

---

## 📄 License

Distributed under the MIT License. See [`LICENSE`](LICENSE) for more information.

