# Workout Log — your own app

Everything runs on your phone. No account, no server, no AI can read your data.

## Files
- `index.html` — the whole app
- `sw.js` — service worker (makes it work offline)
- `manifest.webmanifest` — makes it installable
- `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` — app icons
- `workout-backup-2026-11-17.json` — your zones, races and run templates

## Put it online (GitHub Pages, free, permanent)

1. Create a free account at github.com
2. Click **+** (top right) → **New repository**
3. Name it `workout`, choose **Public**, click **Create repository**
4. Click **uploading an existing file**
5. Drag in every file from this folder EXCEPT README.md (the backup .json is optional)
6. Click **Commit changes**
7. Go to **Settings** → **Pages** (left sidebar)
8. Under *Source* choose **Deploy from a branch**, branch **main**, folder **/ (root)**, click **Save**
9. Wait about a minute, then reload the page — it shows your URL:
   `https://YOUR-USERNAME.github.io/workout/`

## Faster alternative (no account)

Go to **app.netlify.com/drop** and drag this whole folder onto the page.
You get a URL instantly. Make a free account afterwards if you want to keep it.

## Install on iPhone

1. Open your URL in **Safari** (it must be Safari, not Chrome)
2. Tap the **Share** button (square with an arrow)
3. Scroll down, tap **Add to Home Screen**
4. Tap **Add**

It now opens full screen with no browser bars, and works with no signal.
Wait for the first load to finish before going offline — that's when it caches itself.

## Restore your settings

Open the app → **Settings** (gear, top right) → **Restore** → paste the contents of
`workout-backup-2026-11-17.json` → **Restore**.

That puts back your heart-rate zones (195 / 59), both races and your five run templates.
The 193-exercise library rebuilds itself automatically.

## Back up

**Settings → Backup** copies all your data as text. Do it now and then — clearing
Safari's website data would erase everything.

## Updating later

Replace `index.html` on GitHub (Add file → Upload files → same name → Commit).
Then bump `CACHE` in `sw.js` from `workout-v1` to `workout-v2` so phones fetch the new copy.
