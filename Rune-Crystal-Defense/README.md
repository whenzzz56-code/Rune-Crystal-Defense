# Rune Crystal Defense - PWA package (PWABuilder ready)

Contents
- index.html - the game (manifest link, theme-color, icons, service worker registration)
- manifest.webmanifest - name, id, scope, start_url, standalone + landscape, icons (192, 512, 512 maskable), 3 screenshots
- sw.js - service worker: caches the app on first visit and serves it offline
- icons/ - icon-192.png, icon-512.png, icon-maskable-512.png
- screenshots/ - gameplay.png, skill-tree.png, menu.png (1280x720)

Steps
1. Upload this whole folder to any HTTPS static host (GitHub Pages, Netlify, Cloudflare Pages, Vercel).
   Keep the files together. index.html must load at the URL you will give PWABuilder.
2. Open https://www.pwabuilder.com, paste the URL, press Start. Manifest, service worker and icons should all pass.
3. Package for stores > Android. Choose a package ID (for example com.yourname.runecrystal), then Generate.
   Keep the signing key and its passwords that PWABuilder gives you.
4. Test the .apk on a phone. Upload the .aab to Google Play if you publish.
5. For the full-screen Trusted Web Activity, put the assetlinks.json that PWABuilder generates at
   https://YOUR-HOST/.well-known/assetlinks.json

Notes
- Progress and saves use localStorage, which persists inside the installed app.
- The Silkscreen font loads from Google Fonts online; a system monospace font is used if it is unavailable.
- Touch works: tap a hero, then tap the ground to move its post. The on-screen buttons cover pause, skill tree,
  change heroes, start wave and map, so no keyboard is needed.
