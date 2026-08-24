# bookmark-app

A personal bookmark dashboard built using Claude Code. Save, search, filter, and organize your bookmarks — all in the browser, no account or server required.

## Features

- **Add bookmarks** with a title, URL, category, and optional notes, via a collapsible "Add a Bookmark" form
- **Browse** bookmarks as cards in a responsive grid
- **Search** in real time by title or category
- **Filter** by category using clickable chips
- **Delete** bookmarks with a confirmation prompt
- **Persistence** via the browser's `localStorage` — your data survives page reloads
- **Sample data** is seeded automatically on first load so the dashboard isn't empty

## Tech Stack

- Plain **HTML, CSS, and JavaScript** — no frameworks, no build tools
- Single self-contained file (`index.html`) — everything (markup, styles, and logic) lives in one place
- Browser `localStorage` for client-side persistence
- No backend, no dependencies, nothing to install

## Usage

Open `index.html` directly in any modern browser (double-click it, or drag it into a browser window). No server or build step needed.
