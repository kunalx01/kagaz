# कागदपत्रे (Document App)

Same UI as before, now an installable phone app. Static site, no build step.

## Deploy (same way as the Rank Tracker)
1. Upload every file in this folder to a GitHub repository (branch `main`).
2. Settings -> Pages -> Source: GitHub Actions (the included workflow deploys it).
3. Open the Pages link on your phone once (needs internet only this first time).
4. Chrome: menu -> Install app / Add to Home Screen. (Or tap the 💾 button -> ॲप इन्स्टॉल करा.)
   iPhone Safari: Share -> Add to Home Screen.

After that it opens from the home screen icon with the name "कागदपत्रे" and works fully offline (PDF creation too).

## Your data
- Everything you type is saved automatically on the phone (localStorage). Filled rows, ticked boxes and the last tab are remembered.
- A safety copy and daily snapshots (last 7 days) are kept; if the main copy is damaged, the app recovers from them.
- Always open the same installed icon / same link. Clearing browser "site data" erases it, so keep a backup.
- 💾 button -> **बॅकअप जतन करा (.txt)** saves all your entries as a text file on the phone. **बॅकअप परत आणा** restores from that file. Do this about once a week.

## Updating the app
After changing any file, change `VERSION` in `sw.js` (e.g. `kagadpatre-v2`) so phones pick up the new files.

## Files
- `index.html` - the whole app (UI + autosave + backup)
- `sw.js` - offline cache
- `manifest.webmanifest`, `icon*.png`, `icon.svg`, `apple-touch-icon.png` - install + logo
- `html2pdf.bundle.min.js` - PDF maker, bundled locally so it works offline
