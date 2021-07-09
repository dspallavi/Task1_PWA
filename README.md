Demonitrate the Progressive Web Application by using @angular/pwa.


Steps to convert the normal web application into PWA by using Angular CLI

Step 1: 
ng add @angular/pwa --project pwa

Step 2 : ClI will generate files and do nessary changes in angular.json, package.json, app.module.ts and index.html as below

CREATE ngsw-config.json (624 bytes)

CREATE src/manifest.webmanifest (1330 bytes)

CREATE src/assets/icons/icon-128x128.png (1253 bytes)

CREATE src/assets/icons/icon-144x144.png (1394 bytes)

CREATE src/assets/icons/icon-152x152.png (1427 bytes)

CREATE src/assets/icons/icon-192x192.png (1790 bytes)

CREATE src/assets/icons/icon-384x384.png (3557 bytes)

CREATE src/assets/icons/icon-512x512.png (5008 bytes)

CREATE src/assets/icons/icon-72x72.png (792 bytes)

CREATE src/assets/icons/icon-96x96.png (958 bytes)

UPDATE angular.json (3430 bytes)  it will add serviceWorker: true

UPDATE package.json (1107 bytes)

UPDATE src/app/app.module.ts (789 bytes)

UPDATE src/index.html (471 bytes)

√ Packages installed successfully.


Step 3 : Check Angular application as PWA 

    Step A : After adding Sucessfull installation  run ng build --prod
    
    Step B : do npm install of http-server
    
    Step C : http-server -p 8080 -c-1 dist/pwa
    
    Step D : open http://127.0.0.1:8080 in browser 
    
    Step E : Now open the developer console and navigate to Application => Service Workers. there is a service worker file ngsw-worker.js installed for http://127.0.0.1:8080
    
    Step F : The next time that you reload the browser, all the assets should be loaded from the service worker offline cache verify in Network tab Size column
    
    Step G : It means that for the first time we are loading all resources, but afterwards all resources will come from cache storage.
    
    Step H : Cache Storage API helps to keep the application accessible in offline mode. Let’s make application offline from Developer Console “Network => Offline (checkbox)”
    
    Step I : Reload the page and check for content is loaded  ?








