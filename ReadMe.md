# VT Men's Basketball — Sideline Analytics

A single-page, in-browser analytics console for VT MBB play-calls. It reads live and historical possessions from **Firebase Realtime Database** and renders in-game and post-game views (top plays, outcome distributions, PPP/FG% comparisons, heatmaps, scatter, and radar profiles). Built with **React (UMD + Babel in-browser)**, **TailwindCSS**, and **Chart.js**—no build step required.

---

## Quick Start

1. **Clone** the repository, then open `analytics.html` in any modern browser.
2. To avoid CORS/local file issues, serve it with a lightweight server:
   ```bash
   # pick one
   python -m http.server 8080
   npx http-server -p 8080


###
 Firebase Structure
```
playcalls/
├── 2024/
├── 2025/
│   ├── games/
│   │   ├── 2025-11-08
│   │   │   └── possessions
│   ├── schedule/
│   ├── stats/
│   │   ├── series
├── 2026/
│   ├── games/
│   │   ├── 2025-11-08
│   │   │   └── possessions
│   ├── schedule/
│   ├── stats/
│   │   ├── series
```
All of the previous data that was provided was put under the 2024 season. Any new data will be logged under the 2025 stats. Once data gets entered for a game, it will appear the games section in firebase. 

### 
The Manage Game Schedule file is how I maintained the schedule in firebase. It writes directly to the schedule tab, and has the ability to add games and remove them as needed. 