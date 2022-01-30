# GeoLiAS

Geologic lineament analysis using imagery leveraged through Python, Heroku, and Google Earth Engine, try it out: <https://mongo-lin-gee.herokuapp.com>

## Introduction
**GeoLiAs** is an app that utilizes [Google Earth Engine](https://developers.google.com/earth-engine/) and the Python package [geemap](https://github.com/giswqs/geemap) to analyze imagery for lineaments.

Current data sources include [SRTM](https://developers.google.com/earth-engine/datasets/catalog/NASA_NASADEM_HGT_001?hl=en) and [Landsat 7](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C01_T1?hl=en).

## Edge Detection
Edges were detected using [Canny Edge Detector](https://developers.google.com/earth-engine/apidocs/ee-algorithms-cannyedgedetector?hl=en) and further analyzed using [Hough Transform](https://developers.google.com/earth-engine/apidocs/ee-algorithms-houghtransform?hl=en).

### Threshold
The "Threshold" parameter designates the pixel for edge detection only if the gradient magnitude is higher than this value.
### Sigma
The "Sigma" parameter applies gaussian filter before edge detection. A value of "0" applies no filtering.

## Roadmap of the Future
* Ability import any shapefile
* Add other data sources (additional Landsat, DEM sources, etc.)
* Ability to import own imagery for edge detection

## Credits
Thank you to Qiusheng Wu for creating [geemap](https://github.com/giswqs/geemap) and additional documentation and tutorials [here](https://github.com/giswqs).

Instructions on how to deploy Earth Engine Apps on heroku are [here](https://github.com/giswqs/geemap-heroku)