FISHEYED PANCHANG - INSTALL AS AN APP (no store, no signing)
=============================================================

Upload ALL files in this folder to your domain, in the same folder
(index.html, manifest.json, sw.js, appcache.manifest and the three icon PNG files).
If your host only accepts some file types, upload at least index.html and the icon PNG files; the app still works.
The site must open with https:// (W3Schools Spaces does this).

ANDROID (Chrome)
 1. Open your page in Chrome.
 2. Menu (three dots) > "Install app" (or "Add to Home screen").
 3. Chrome builds a real installed app (a WebAPK) with its own icon. It works offline after the first visit.
 TO GET A REAL .APK FILE WITHOUT ANY EDITOR: open pwabuilder.com, paste your page address, press Start, then Package for Stores > Android > Generate. Download the zip, open the .apk inside it on your phone and install it (allow 'install unknown apps' when asked).

iPHONE / iPAD, INCLUDING iOS 10.3.3 (Safari)
 1. Open your page in Safari.
 2. Tap the Share button > "Add to Home Screen" > Add.
 3. Open it from the Home Screen: it runs full screen like an app.
 Offline use on iOS 10 relies on appcache.manifest. If your host does not serve that file as
 "text/cache-manifest" the app still works but needs an internet connection.
 After every update, change the "version" number in appcache.manifest so phones refresh.

A real APK file or IPA file needs Android Studio / Xcode (see the two project kits that came with this package).

OFFLINE USE (no internet) - READ THIS ONCE
 1. Upload every file in this folder, including the one named _headers (Netlify and Cloudflare Pages use it
    to serve appcache.manifest correctly, which iOS 10 needs). Keep .htaccess too if your host runs Apache.
 2. On the iPad (iOS 10.3.3): connect to Wi-Fi, open your page in Safari and wait until the green
    "Offline ready" badge shows at the top (about 5-20 seconds). Then Share > Add to Home Screen.
 3. Open the app from the Home Screen once while online. After that you can switch on Airplane mode: it opens
    and works with no internet. Notes and settings are saved on the device.
 4. On Android Chrome the same badge appears after the first visit (it uses a service worker).
 5. After you upload a new version, open the page once online and then close and reopen it. For iOS 10 also
    change the "version" number in appcache.manifest so the iPad downloads the update.
 Notes: iOS can clear offline copies if the iPad is very low on storage or the app is unused for a long time;
 just open it once online again to save it again.
