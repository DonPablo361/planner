# Planner

Personal planner web app: Today, Tasks, Training, Health & Wellbeing, Finance, Life admin, Future, Insights.

## Files

All 6 files must sit in the same folder:

- `index.html`: the whole app
- `manifest.webmanifest`: lets the phone install it as an app
- `sw.js`: makes it work offline
- `icon-180.png`, `icon-192.png`, `icon-512.png`: app icons

## Put it online with GitHub Pages (free)

1. Create an account at github.com.
2. Create a new repository, e.g. `planner`. Set it to Public (free accounts can only publish public repositories).
3. In the repository choose "Add file" → "Upload files", upload all 6 files, and commit.
4. Go to Settings → Pages. Under "Branch" choose `main` and `/ (root)`, then Save.
5. After a minute or two the page shows your address: `https://YOUR-NAME.github.io/planner/`

The code is public, your data is not. Everything you enter is stored only on the device you use.

## Install on iPhone or iPad

1. Open the address in Safari.
2. Tap Share → "Add to Home Screen".
3. Always open it from the home-screen icon. The icon and a Safari tab keep separate data.

On the laptop, open the address in Chrome or Edge and use the install icon in the address bar, or bookmark it.

## Updating the app

1. Upload the new files to the repository, replacing the old ones.
2. In `sw.js`, raise the version on the line `const CACHE = 'planner-v4';` (v5, v6, ...).
3. Open the app twice. The first open fetches the update, the second shows it.

Updating never touches your data. Data from the first version (Tasks only) is carried over automatically, and its time values are converted from minutes to hours.

## Your data

- Stored on the device, separately per device and per browser.
- Deleting the home-screen app or clearing Safari website data erases it.
- More → Settings → Export backup saves everything to a file. Import that file on another device to copy your data across.

## Automatic prices (Finance)

Prices are looked up by ISIN from EODHD (eodhd.com). Create a free account there, copy the API token, and paste it under More → Finance → Setup. Prices then update once a day when you open Finance. Without a token, or for positions the service does not know, enter the price by hand on the position.
