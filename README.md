# LBD Daily Report Tool

Living by Design Nation daily Bethel attendance reports, packaged as an installable Android app (PWA) and hosted on GitHub Pages.

## 1. Put it on GitHub (one time)
1. On github.com create a new repository (for example `lbd-report-tool`).
2. Upload everything in this folder to it, keeping the structure (`index.html`, `manifest.webmanifest`, `sw.js`, `icons/`, `.github/`). Make sure the hidden `.github` folder is included.
3. In the repository go to **Settings → Pages → Build and deployment → Source** and choose **GitHub Actions**.
4. Open the **Actions** tab; the "Deploy to GitHub Pages" run finishes in about a minute.
5. Your app is live at `https://YOUR-USERNAME.github.io/lbd-report-tool/`.

## 2. Install on Android
Open that link in **Chrome**, tap the menu (⋮) and choose **Install app** (or **Add to Home screen**). It appears in the app drawer with the LBD icon, opens full screen and works offline once opened one time.

## 3. Optional: a real APK
If you want an `.apk`/`.aab` file (to share directly or publish to Google Play):
1. Go to https://www.pwabuilder.com, paste your GitHub Pages link and press **Start**.
2. Choose **Package for stores → Android**, download the package and follow the signing steps.
This wraps the same hosted app, so every update you publish to GitHub shows up in the Android app automatically.

## Publishing an update
Replace `index.html` in the repository with the new version and change `CACHE_VERSION` in `sw.js` (for example `lbd-v2`). Phones pick up the new version the next time the app opens online.

## Things to know
- GitHub Pages on a free account needs a **public** repository, so anyone with the link can open the tool and see its code. The attendance data and your database link/key are not in the repository: they are typed into **Settings** on each phone and stay on that phone.
- **Save PDF** uses Chrome's print dialog: choose **Save as PDF** as the destination.
- CSV downloads go to the phone's Downloads folder.
