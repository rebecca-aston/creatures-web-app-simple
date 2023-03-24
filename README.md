# creatures-web-app-simple
 
An example of a simple Progressive Web App, so that you can display your application as a standalone app, force it into full screen mode, or pin it as an app on a mobile device. 

__Managing the scope of github pages urls__

Leave the sw.js file at the top level / root folder (i.e. on the same level as your index.html)

You should replace "creatures-web-app-simple" with the name of your github repo in index.html, sw.js and manifest.webmanifest.  Make sure your changes match what you see in my template, otherwise your paths will be messed up. Watch out the forward slashes / 

__Editing sw.js__

This is where your service worker does its thing. In addition to making sure that `GHPATH` matches the name of your repo:

1. Change the `APP_PREFIX` to something unique to this application. Your cached files for this app will be stored under this name, so make sure it doesn't clash with other names of your apps.
2. If your app is one that can work offline you can make sure that all files and assets you want to use offline are included in the `URLS` array. Again make sure your paths match your folder structure and watch out for the forward slashes /

__Editing your webmanifest__

In addition to making sure that the "scope" property and "start_url" property matches the name of your repo:

1. Names: Set the name and the short name to something unique to your experience.
2. App Icons: you can quickly get up an running with the right format and resolution for your app icons using [this tool](https://tools.crawlink.com/tools/pwa-icon-generator/) and others like it. Upload an image for your icon and then replace the ones in the assets folder of this template (make sure the webmanifest paths to the icons match). More on understanding icons [here](https://dev.to/progressier/why-a-pwa-app-icon-shouldnt-have-a-purpose-set-to-any-maskable-4c78 ).
3. Display: You can control how the app behaves when opened set the "display" property to:
   - "fullscreen"
   - "standalone"
   - "minimal-ui"
   - "browser"
4. The "theme_color" will set the color of the app bar in standalone and mimimal-ui mode.
5. Read more about webmanifests [here](https://web.dev/add-manifest/?utm_source=devtools).

