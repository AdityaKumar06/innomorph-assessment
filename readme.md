# 360° Interactive Car Viewer & Panorama Demo

**Single-file vanilla JavaScript project** demonstrating multiple interaction patterns for a 360° product viewer (car rotation) + immersive 360° panorama.

Built as a lightweight, framework-free showcase to demonstrate front-end skills: DOM manipulation, event handling (mouse, touch, keyboard, wheel), modular code structure, responsive design, theme switching, and third-party library integration (Pannellum).

**Live demo goal**: One HTML file → open in browser → everything works (assuming image assets are present).

## Features

### 360° Car Spin Viewer (51-frame image sequence)
- Same 51 high-quality PNG frames used across all modes (`img/1.png` → `img/51.png`)
- Tabbed interface — switch control methods without page reload or layout shift
- All viewers appear in the **same fixed position** (no vertical scrolling when changing tabs)

Supported interaction modes:

| Mode              | Input Method                  | Mobile Support | Accessibility Notes                  |
|-------------------|-------------------------------|----------------|--------------------------------------|
| Drag              | Mouse drag / touch swipe      | Full           | Most intuitive & widely used         |
| Mouse Move        | Mouse movement over image     | Partial        | Quick preview style                  |
| Wheel / Trackpad  | Mouse wheel or two-finger scroll | Full        | Natural for desktop & laptops        |
| Arrow Keys        | ← → (or ↑ ↓) after focus      | N/A            | Keyboard accessible (tabindex + keydown) |

### Immersive 360° Panorama
- Full equirectangular panorama using **Pannellum** (loaded via CDN)
- Auto-rotation, zoom, fullscreen, controls
- Shown as fifth tab ("Panorama")

### Additional Polish
- Dark / Light mode toggle (persists via localStorage + system preference detection)
- Smooth fade transitions between tabs
- Responsive layout (mobile-friendly tabs & viewer sizing)
- Glassmorphism + neumorphic card styling
- Consistent loading spinner across all viewers
- Clean separation of concerns (constants, helper functions, per-mode logic)

## Technologies Used

- **HTML5** + **CSS3** (modern features: clamp(), backdrop-filter, custom properties)
- **Vanilla JavaScript** only — no frameworks, no build tools
- **Pannellum** (CDN) — lightweight 360° panorama viewer
- Google Fonts (Inter) via link preconnect
- Local image assets (51 PNG frames + 1 panorama JPG)

