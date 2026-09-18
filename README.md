<div align="center">

# 🌾 Agrain: "Alamin Ang Tamang Presyo"
**Top 10 Finalist | UPLB ACSS The Innovation Lab Hackathon**

[![Live Web](https://img.shields.io/badge/Live_Web-Visit_Vercel-orange?style=for-the-badge&logo=vercel)](https://agrain.vercel.app/)
[![Hackathon](https://img.shields.io/badge/Hackathon-The_Innovation_Lab-blue?style=for-the-badge&logo=eventbrite)](https://luma.com/a3hzf077)
[![Tests](https://img.shields.io/badge/tests-108_passing-brightgreen?style=for-the-badge&logo=vitest)](#-testing)
[![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)](LICENSE)

---

### 🚀 Financial Empowerment for the Modern Filipino Farmer
*Breaking the cycle of negotiation disadvantage through visual, offline-first technology.*

</div>

## 📖 Executive Summary
**Agrain** is an innovative, **offline-first** financial empowerment tool designed to address the lack of transparent pricing information and the negotiation disadvantage faced by smallholder farmers. 

By replacing mental arithmetic with visual and tactile feedback, Agrain enables farmers to make informed decisions confidently, even under pressure. The application strengthens negotiation leverage and provides verifiable proof of true production costs.

---

## ✨ Key Features

* **📸 Offline Expense Logging:** Snap photos of fertilizer sacks, receipts, seeds, and labor costs. No internet required.
* **🪣 The "Expense Bucket":** A visual representation of total seasonal investment, providing an intuitive overview of production costs.
* **📊 Automatic Break-Even Calculation:** Instantly know the minimum price per kilo needed to recover your investment.
* **⚖️ Dynamic Negotiation Slider:**
    * 🔴 **Red Screen:** Offer is below break-even (Potential Loss).
    * 🟢 **Green Screen:** Offer exceeds threshold (Profit).
* **🌐 PWA Technology:** Operates entirely offline using **IndexedDB** for local storage.

---

## 🛠️ Tech Stack

<p align="left">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=react,vite,tailwind,js,npm" />
  </a>
</p>

| Category | Technology |
| :--- | :--- |
| **Language** | JavaScript (JSX) |
| **Frontend Framework** | **React 19** |
| **Build Tool** | Vite 6 |
| **Styling** | Tailwind CSS v4 + Custom CSS Variables |
| **Routing** | React Router DOM v7 |
| **State Management** | React Context API |
| **Database / Storage** | **IndexedDB** via LocalForage (Offline-first) |
| **PWA** | `vite-plugin-pwa` (Installable & Offline-capable) |
| **Testing** | Vitest 4, React Testing Library, jsdom |
| **Package Manager** | npm |
| **Fonts** | Google Fonts (*Righteous, Bebas Neue, Playfair Display*) |

---

## 👥 Team CIH314
We are a dedicated team of student innovators that joined the **UPLB ACSS Innovation Lab** Hackathon in February 2026.

* **Alvarado, Silver Aldren A.**
* **Billones, John Rey F.**
* **Capistrano, Gem Erien A.**
* **Cuchado, Rosh Evander B.**
* **Lagajino, Justine Nicol D.**

---

## ⚙️ Installation & Usage (Local Development)

**Prerequisites:** Node.js 18+ and npm

```bash
# 1. Clone the repo
git clone https://github.com/gecapistrano/Agrain.git
cd Agrain

# 2. Install dependencies
npm install

# 3. Start the dev server (http://localhost:5173)
npm run dev
```

**Other commands**

| Command | What it does |
| :--- | :--- |
| `npm run dev` | Start the Vite dev server with hot reload |
| `npm run build` | Production build to `dist/` |
| `npm run preview` | Serve the production build locally |
| `npm test` | Run the full Vitest suite once |
| `npm run test:watch` | Run tests in watch mode |

> **Note:** Agrain is a PWA and needs no backend, API keys, or environment variables. All data is stored locally in the browser via IndexedDB, so the app is fully functional offline from first load.

---

## 🧪 Testing

The app ships with **108 tests across 20 suites**, covering UI components, business logic, and page-level integration.

```bash
npm test
```

| Layer | Covered |
| :--- | :--- |
| **Negotiation** | Break-even math, bucket visual, harvest input, price slider |
| **Expenses** | Expense cards, list rendering, logging modal, tier picker |
| **Camera** | Capture flow and photo preview |
| **Layout / UI** | App shell, bottom nav, header, buttons, confirmations |
| **Pages** | Home, Expenses, and Negotiation integration |
| **Utilities** | Design tokens and shared constants |

The break-even calculation in `src/utils/breakeven.js` is the core of the product, so it is unit-tested independently of the UI.

---

## 🧠 How the Break-Even Logic Works

Agrain's central idea is that a farmer should never have to do arithmetic under negotiating pressure.

1. Every expense logged during the season is summed into a **total investment**.
2. The farmer enters their **harvest weight** in kilos.
3. The app computes the **break-even price per kilo** — total investment divided by harvest weight.
4. The negotiation slider compares any offered price against that threshold and turns **red below it** and **green above it**.

The result is a single, glanceable answer to the only question that matters at the farm gate: *is this offer a loss or a profit?*

---

## Keywords

`offline-first` • `financial empowerment` • `farm-gate` • `smallholder farmers` • `break-even price` • `PWA` • `negotiation leverage` • `expense tracking` • `zero-math interface`
