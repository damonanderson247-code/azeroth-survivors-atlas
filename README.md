# Azeroth Survivors Build Atlas — GitHub Pages site

The complete static Atlas is in this folder: 9 classes, 29 routes, visuals, research evidence, and an assisted 5× Shadow Priest Naxx victory.

## One-time publishing (public GitHub repository)

1. In GitHub, create a **public** repository called `azeroth-survivors-atlas` under your account. Do not initialize it with a README; the upload includes one.
2. Extract the ZIP on your PC. Upload the **contents** of the extracted folder (not the ZIP itself) to the repository root on the `main` branch. GitHub's **Add file → Upload files** supports drag-and-drop. Commit the files.
3. Go to **Settings → Pages**; choose **Deploy from a branch**; select `main` and `/ (root)`; Save.
4. When deployed, your address is `https://damonanderson247-code.github.io/azeroth-survivors-atlas/` (assuming that exact owner and repository name).
5. GitHub may ask you to approve installing the ChatGPT GitHub app on the new repository; allow repository access so subsequent updates can be committed from chat.

## Future updates without downloading anything

After sharing each Run Recorder ZIP in ChatGPT, review the measurements, then update just **`data/updates.json`** in the **same GitHub repo**. The site reloads this file on each visit. New run entries go into `runs`, and changed recommendations/evidence go into `route_overrides` using a key like `"Priest/Shadow"`. The ChatGPT GitHub connection can make those commits once your repository is accessible and writable. The original bulk research data (`data/site.json`) and page (`index.html`) normally do not change.

Do **not** claim the web page updates without an actual successful commit to GitHub. Runs do not automatically upload from the game.

## Repository layout

- `index.html`: Atlas site UI with embedded fallback snapshot.
- `data/site.json`: 29-route baseline and initial Shadow Priest assisted run.
- `data/updates.json`: compact mutable run updates / route evidence overrides.
- `assets/`: reviewed meter screenshots.
- `Talent_Tree_Images/`: original diagrams.

Public repos and Pages are viewable by anyone. Review evidence files before publishing.