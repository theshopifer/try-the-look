# Try the Look — Runway

An interactive Nike-branded streetwear outfit carousel and styling experience. Six full-body curated looks stand on a turning 3D ring stage with depth-of-field blur, smooth spring dynamics, interactive product pins, a responsive "In this look" panel with size selectors, bundle discounting, and a client-side styling bag shortlist.

Built with **pure vanilla HTML, CSS, and JavaScript** encapsulated in a custom `<runway-section>` web component, bundled with Vite.

---

## ✨ Features

- **🔄 3D Ring Carousel & Depth Physics**:
  - **Desktop (Ring Mode)**: 12 bodies arranged along a 3D cylindrical ring with depth scaling, horizon convergence, and optical depth-of-field blur.
  - **Mobile (Classic Mode)**: Diagonal staggered perspective procession with velocity-based swipe gesture handling.
  - Seamless hero-to-body handoff at rest, light sweep reflections, and automatic canvas-based alpha probe scanning for perfect sole-to-floor alignment (`findFeet`).

- **🎯 Interactive Product Pins & "View Look" Lightbox**:
  - Click on the hero figure or "View" prompt to expand the look via a 950ms FLIP zoom animation.
  - Glass-morphism numbered pins with double-ripple halos highlighting head-to-toe pieces.
  - Bi-directional hover/focus linking between model pins and the sidebar product list.

- **🛍️ "In This Look" Sidebar & Bundle Flow**:
  - Live product breakdown with thumbnail zooms, badges, vendor tags, and prices.
  - Size selectors (pill radio buttons) with real variant mapping and mobile bottom-sheet docking.
  - **Complete the Look**: Automatic bundle price calculation ($547.00 → $492.30, save 10%) with batch addition, validation prompts, and animated loading/success states.

- **🎒 Local Styling Bag**:
  - Persistent shortlist stored in `localStorage` (`runway-styling-bag-v3`).
  - Slide-out modal with quantity controls, live reference subtotal, and original product links.
  - One-click export to download a plaintext outfit shortlist (`runway-outfit-shortlist.txt`).

- **🎛️ Fluid Controls & Custom Cursor**:
  - Custom inertia cursor with "Drag", "View", and link dot states.
  - 5-second autoplay timer with 01–06 segmented progress fill bars and play/pause toggle.
  - Full keyboard accessibility (Arrow keys to navigate, Escape to dismiss dialogs).
  - Velocity-preserving drag and fling with horizontal trackpad support.

---

## 🛠️ Tech Stack & Implementation

- **Framework**: None (Vanilla JavaScript, Native Web Components: `<runway-section>`).
- **Styling**: Native CSS custom properties, cubic-bezier transition curves, and CSS Grid/Flexbox.
- **Typography**: Inter 600 (embedded as a base64 WOFF2 data URI for header navigation), system Helvetica / Arial stack for runway elements.
- **Build Tool**: [Vite](https://vite.dev/) 8.

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- `npm`

### Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/theshopifer/try-the-look.git
cd try-the-look
npm install --legacy-peer-deps
```

### Running Locally

Start the local development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Building for Production

Compile production-ready static assets:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

---

## 📁 Project Structure

```text
├── index.html          # Main HTML document with header, <runway-section>, dialog, and toast
├── package.json        # Project metadata and scripts
├── tsconfig.json       # TypeScript and bundler configuration
├── vite.config.ts      # Vite configuration
└── src/
    ├── main.ts         # <runway-section> component, physics engine, and styling bag logic
    └── style.css       # Complete design tokens, keyframes, transitions, and responsive layout
```

---

## ⌨️ Controls & Shortcuts

| Action | Control |
|---|---|
| **Next Look** | Drag Left / ArrowRight / Next Button |
| **Previous Look** | Drag Right / ArrowLeft / Prev Button |
| **Direct Jump** | Click any segmented tick (01–06) or background model |
| **View Look Details** | Click the active model or press Enter when focused |
| **Close Lightbox / Picker** | Press `Escape` or click backdrop |
| **Toggle Autoplay** | Click Pause/Play button (auto-pauses on interaction) |

---

## 📄 License

This project is licensed under the Apache-2.0 License.
