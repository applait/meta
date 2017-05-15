## Backend (Server)

The backend of the app will be a web service which will provide a RESTful API for the frontends to communicate with it. This server will be formed of three main modules - scraper, processor and output. The primary benefit of separating the server into modules is that these components can modified independently and one change required in the one of the module will not impact the rest.

The modules in detail:

### 1. Data scraper/receiver

This module will scrape data from multiple sources and collate them together in a database in a specific format. Current sources include:

 - eRail API - automatically scraped at intervals.
 - Individual sources for metro railways, manually fed.

### 2. Data processor

This module will read data from the database where the data scraper has written the data and perform operations on that data to make it more meaningful for the features we are trying to provide.

At the moment for MVP, it will process data into:

 - Geographical location of each train at a given time.
 - Point to point trains, mapping train routes.
 - Given any two arbitrary towns or cities, show train routes available, with multiple breaks. Something like what we have for flight data, but for trains.

### 3. Data output (REST interface)

This module will be the public facing side of the server. It will expose API endpoints to request data. Depending on the request, it will scan through the crunched data and produce output as JSON.

## Frontend (app)

The app will be built as a hybrid HTML5 app, on Ionic and Cordova. We will primarily use client side data storage (localForage) and GeoLocation, both of which work well with Cordova.

Current target platforms for MVP are Firefox OS and Android.

### MVP features:

 - Find trains by stations
 - Find trains by date
 - Check reservation status
 - Find metro stations near user location.
 - Get metro route from point to point in selected city.
 - Get metro availability at a given time.