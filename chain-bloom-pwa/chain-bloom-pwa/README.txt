CHAIN BLOOM - installable web app (PWA)

FILES
  index.html             the game
  manifest.webmanifest   app name, colors and icons
  sw.js                  service worker: makes the game work offline
  icon-*.png             app icons

HOST IT (free, must be served over HTTPS)
  Netlify Drop     app.netlify.com/drop: drag this unzipped folder onto the page.
  GitHub Pages     new repository, upload these files, then Settings > Pages >
                   deploy from the main branch (root).
  Cloudflare Pages similar to the above.
  Note: itch.io runs games inside a frame, so the game plays there but cannot be
  installed to the home screen. Use one of the hosts above for the installable version.

INSTALL
  Android (Chrome)  open the link, then tap "Install app" in the game menu
                    (or Chrome menu > Install app / Add to Home screen).
  iPhone/iPad       open the link in Safari, tap Share > Add to Home Screen.
  After the first load the game works with no connection.

TEST ON YOUR COMPUTER
  python3 -m http.server 8000   then open http://localhost:8000

UPDATING
  Change the files, then bump CACHE ('chain-bloom-v1' -> 'v2') in sw.js so
  installed copies pick up the new version.
