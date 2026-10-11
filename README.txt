MAJOR TRIAD FLASH DRILL: home-screen web app

Files
  index.html              the whole app (fonts are embedded, no internet needed to run)
  manifest.webmanifest    name, colors and icons for the home screen
  sw.js                   makes it work offline
  icon-192.png, icon-512.png, apple-touch-icon.png

Put it online (any static host works; keep all files together in one folder)
  GitHub Pages:  new repository, upload these files, then Settings > Pages > deploy from the main branch.
                 Free accounts need a public repository. The app holds no personal data.
  Netlify:       sign in, then drag the unzipped folder onto the Deploy area of a new site.
  Cloudflare Pages: Workers & Pages > Create > Pages > Upload assets.
  The address must start with https:// for offline mode to work.

Install on the iPhone
  1. Open the address in Safari (not an in-app browser).
  2. Tap Share, then Add to Home Screen, then Add.
  3. Open it once from the home-screen icon while online. After that it works offline.

Notes
  Practice history is stored on that phone, inside the home-screen app. It does not sync to other
  devices and it is separate from the copy in Safari. Deleting the app deletes the history.
  To publish an update, replace the files on your host. The phone picks up the new version the
  second time you open the app. To force it sooner, change CACHE in sw.js (for example to triad-drill-v2).
