# V_Tab

> A lightweight, pure-frontend personal homepage & browser start page.
> Custom bookmarks, grouped tabs, fun cards — dark mode, light mode, your rules.

## Vision

V_Tab is your **daily launchpad** — the first thing you see when you open a browser tab. Clean, fast, and yours to shape.

- **Pure frontend** — no backend, no database, no server setup. Static-first, deploy anywhere (GitHub Pages, Netlify, Vercel, or a local folder).
- **Lightweight** — no bloat. Built on Vue 3 + Varlet UI, ships lean.
- **Dark & Light modes** — system-aware, manual toggle.
- **Multi-language** — i18n built in from day one.
- **Theme switching** — multiple accent palettes, swap freely.
- **Custom bookmarks** — add, edit, drag & drop, group into categories.
- **Grouped tabs** — organise links like a real dashboard.
- **Fun cards** — widgets, greetings, weather, quote of the day — make it feel alive.
- **Personal homepage** — replace the boring default new tab with something that actually belongs to you.

## Tech Stack

| Layer | Library |
|-------|---------|
| **Framework** | [Vue 3](https://vuejs.org/) (Composition API + `<script setup>`) |
| **Language** | TypeScript |
| **Build Tool** | [Vite](https://vitejs.dev/) |
| **UI Library** | [Varlet UI](https://varlet.gitee.io/varlet-ui/) |
| **State Management** | [Pinia](https://pinia.vuejs.org/) |
| **Routing** | [Vue Router 4](https://router.vuejs.org/) |
| **Type Check** | vue-tsc |

## Getting Started

```bash
npm install
npm run dev      # hot reload at http://localhost:5173
npm run build    # production build
npm run preview  # preview production build
```

## Project Structure

```
V_Tab/
|-- src/
|   |-- components/   # Reusable components
|   |-- views/        # Page-level views
|   |-- router/       # Vue Router setup
|   |-- stores/       # Pinia stores
|   |-- composables/  # Composable utilities (useTheme, useI18n, etc.)
|   |-- utils/        # Helper functions
|   |-- types/        # TypeScript type definitions
|   |-- api/          # API modules
|   |-- assets/       # Static assets
|   |-- App.vue       # Root component
|   |-- main.ts       # Application entry
|-- public/           # Public static files
|-- index.html
|-- vite.config.ts
|-- tsconfig.json
|-- package.json
|-- ...
```

## Roadmap

- [x] Project scaffold (Vue 3 + TS + Varlet UI + Pinia + Router)
- [ ] Dark / Light mode toggle
- [ ] i18n multi-language support
- [ ] Custom bookmark manager (add / edit / delete / drag-drop)
- [ ] Bookmark groups / categories
- [ ] Fun cards widget system
- [ ] Theme accent colour picker
- [ ] Import / export bookmarks
- [ ] Browser start page mode

## Contributors

- [**LordGalaxy**](https://github.com/YDYm233) — 银河领主, project owner
- **Vex@Babata** — 巴巴塔, developer

---

Built with ❤ on 陨墨星号
