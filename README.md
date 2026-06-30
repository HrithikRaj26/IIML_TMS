# 🎯 CampusQuest — Daily Task Command Center

A **gamified daily task management system** for colleges. Tasks become *Quests*, departments become factions, and completing work earns **XP and levels**. Built as a pure frontend (no backend) so it deploys to GitHub + Vercel in minutes.

![status](https://img.shields.io/badge/build-static-A855F7) ![backend](https://img.shields.io/badge/backend-none-FF2D95) ![deploy](https://img.shields.io/badge/deploy-vercel-22D3EE)

## ✨ Features

- **Dashboard** — animated completion core, live stat cards, department load bars, today's priority quests
- **Quests** — search + filter by status, department, and priority; create / complete / reopen / delete
- **Board** — Kanban (To Do → In Progress → Done) with one-click stage moves
- **Leaderboard** — staff & students ranked by XP earned from completed quests
- **Gamification** — XP per quest, levels, and an XP-burst confetti animation on completion
- **Motion** — particle field, aurora glow, synthwave grid, count-up stats (all respect `prefers-reduced-motion`)
- **Persistence** — your changes are saved in the browser via `localStorage`
- **Responsive** — works down to mobile with a slide-in sidebar

## 🗂 Structure

```
campusquest/
├── index.html      # the entire app (HTML + CSS + JS, self-contained)
├── vercel.json     # static deploy config
├── .gitignore
└── README.md
```

No build step, no dependencies. Fonts load from Google Fonts via CDN.

## 🚀 Deploy

### Option A — Vercel (recommended)
1. Push this folder to a GitHub repo.
2. Go to [vercel.com](https://vercel.com) → **Add New → Project** → import the repo.
3. Framework preset: **Other**. Leave build command empty, output dir `./`. Click **Deploy**.

### Option B — Vercel CLI
```bash
npm i -g vercel
cd campusquest
vercel
```

### Run locally
Just open `index.html` in a browser, or:
```bash
npx serve .
```

## 🎨 Customize

- **College name** — edit the `Riverstone College` text in the sidebar footer (`index.html`).
- **Dummy data** — edit the `seed()` function near the top of the `<script>` block. Each row is
  `[title, department, priority, status, dueOffsetDays, assignee, role]`.
- **Departments / colors** — the `CATEGORIES` object.
- **XP weights** — the `PRIORITIES` object.

> Tip: to reset to the original dummy data, clear the `campusquest` key in your browser's
> localStorage (DevTools → Application → Local Storage).

## 📝 License

MIT — use it freely.
