TRAINING TRACKER — install as an app on your Android phone
===========================================================

This folder is a complete Progressive Web App (PWA). It works offline,
opens fullscreen, and keeps all your data on your phone.

Files (keep them together, don't rename):
  index.html               your tracker
  manifest.json            app name, icon, fullscreen setting
  sw.js                    offline caching
  icon-192.png             app icon (small)
  icon-512.png             app icon (large)
  icon-maskable-512.png    app icon (adaptive/circular crop)


DEPLOY (about 5 minutes, free)
------------------------------
Easiest route — Netlify Drop:
  1. Go to  https://app.netlify.com/drop
  2. Drag this whole folder onto the page.
  3. You get a URL like  https://something-random.netlify.app
     (unlisted — only someone with the exact link can reach it).

Alternative — GitHub Pages:
  1. Create a repository, upload these files.
  2. Settings > Pages > deploy from the main branch, root folder.
  3. You get a  https://yourname.github.io/repo  URL.

Both serve over HTTPS, which is required for offline mode to work.


INSTALL ON YOUR PHONE
---------------------
  1. Open the URL in Chrome on your Android.
  2. Tap the ⋮ menu > "Add to Home screen" / "Install app".
  3. It appears on your home screen with the blue icon and opens
     fullscreen, no browser bar.

After the first visit it works with no internet.


YOUR DATA
---------
Data is stored on your phone, in the app — it never goes to the host.
Use the "Export backup" button every few weeks to save a copy, and to
move your history to a new phone (then "Import backup" there).


UPDATING LATER
--------------
If you change the app, re-deploy the folder. To force phones to pick up
the new version, open sw.js and bump the version line:
    const CACHE = "tracker-v1";   ->   "tracker-v2"
