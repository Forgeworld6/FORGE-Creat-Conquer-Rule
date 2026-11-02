# FORGE — Personal Android app

This is a personal, offline-first web app. Projects, profile, likes, bookmarks and theme are saved in this browser on your device using local storage. It does not use a public account, backend, or cloud sync.

## Install on Android
1. Put the contents of this folder on an HTTPS static host (for example, a private GitHub Pages site) or serve it from a local HTTPS development server.
2. Open the site in Chrome on your Android phone.
3. Open Chrome menu ⋮ → **Install app** (or **Add to Home screen**).
4. Launch FORGE from your home screen.

A PWA must be served from HTTPS (or localhost) for reliable installation and offline caching. Opening `index.html` directly from a file manager lets you try the app, but does not provide full PWA installation/offline behavior.

## Features
- Add, edit, and delete projects (delete by editing? use browser data reset; current build supports create/edit; no server-side sync)
- Draft/published status, categories, technology tags, demo/GitHub links
- Image covers (up to 1.2 MB each)
- Search, category filtering, sorting
- Local bookmarks and favourites
- Editable creator profile
- Dark/light theme
- Export personal data as JSON
- Responsive mobile UI and offline shell cache

## Privacy
Everything stays in this browser's local storage. Clearing browser site data will erase your workspace. Use **Export my data** for backups. No uploaded project code is executed.


Branding: the official FORGE logo is used as `icon.png` for the app icon, browser icon, and in-app header.


Logo update: the official FORGE logo is provided as icon-forge-192.png and icon-forge-512.png. The app references these new filenames and uses cache version v3 so older cached logo assets can be replaced.
