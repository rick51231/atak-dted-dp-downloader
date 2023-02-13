# ATAK DTED2 DataPackage generator
This tool used for downloading DTED2 elevation models data from USGS and creating ATAK DataPackages from it.
In releases section, you can find datapackages for several regions.

### Requirements
- USGS account
- Geoapify api key (create free-tier account. For single-use you can find key in the source code of [this](https://www.geoapify.com/boundaries-api) page)
- Geoapify regions ids (see below)

### Get region ids
- Go to https://apidocs.geoapify.com/playground/place-details/
- Select `From address autocomplete`
- Enter the name of the country (or etc) in the text field
- When result loading finished, scroll to the bottom and copy the region id from `place_id: xxxx` (xxx - region id)

### Usage
- Install requirements `npm install`
- Fill variable `usgsLogin` in [index.js](index.js) with you USGS login
- Fill variable `usgsPassword` in [index.js](index.js) with you USGS password
- Fill variable `geoapifyKey` in [index.js](index.js) with you Geoapify api key
- Fill variable `regions` in [index.js](index.js) with required regions list
- Run script via `node index.js`
- When it's finished, the datapackages will be in the `release` folder

