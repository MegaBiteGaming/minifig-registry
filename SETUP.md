# MegaBites Minifig Collection — Setup

A fully offline minifigure catalog. Once installed on your iPhone, it needs **no server and no internet connection** — all your data (including photos) lives in the phone's local storage.

## 1. Get it online (one-time, ~5 minutes)

iOS needs to load the app from a URL once before it can be "installed." The easiest free option is GitHub Pages:

1. Create a free GitHub account if you don't have one: https://github.com/join
2. Create a new **public** repository, e.g. `minifig-registry`
3. Upload these files, keeping the folder structure:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icons/icon-192.png`
   - `icons/icon-512.png`
   - `icons/apple-touch-icon.png`
   - `icons/logo-header.png`
4. Go to the repo's **Settings → Pages**, set Source to the `main` branch, root folder, and save
5. GitHub gives you a URL like `https://yourname.github.io/minifig-registry/`

(No coding or command line needed — GitHub lets you drag-and-drop files to upload via the web interface, under "Add file → Upload files.")

## 2. Install on your iPhone

1. Open the GitHub Pages URL in **Safari** (must be Safari, not Chrome — only Safari supports "Add to Home Screen" as a real app on iOS)
2. Tap the **Share** button (square with an arrow)
3. Tap **Add to Home Screen**
4. Open it from your home screen icon — it now runs full-screen, like any other app

## 3. Go offline

Open the app once while connected (this lets the service worker cache everything). After that, turn on Airplane Mode and open it again — it'll work exactly the same. Add a figure, close the app, restart your phone — the data stays, all stored locally in the browser's IndexedDB.

## Online lookup (optional)

Tap the gear icon (bottom left) to add a free **Rebrickable** API key. Once set, a search icon next to the Item Number field lets you look up a figure by its item number (e.g. `sw1211`) or name while you're online — it auto-fills the name, item number, and photo.

To get a key: create a free account at [rebrickable.com](https://rebrickable.com), then go to **Account → Settings → API** to generate one, and paste it into the app.

This only runs when you have a connection — everything else in the app keeps working fully offline as before.

## Backing up your data

Tap the up-arrow icon (bottom left) to export a JSON file of your whole collection — useful before you clear Safari data, switch phones, or just want a backup. The down-arrow icon re-imports it.

## Updating the app later

If you ever want to tweak the code, just re-upload the changed file(s) to the same GitHub repo. Safari will pick up the update next time you're online.
