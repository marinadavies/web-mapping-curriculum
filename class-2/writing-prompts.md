## What is the difference between raster and vector data?
* Raster tiles are images and plain HTML elements that can be manipulated and rendered on the fly. Vector data can be stored in vector tiles. With vector tiles, you only store data and code rules for how you want the map to look like. Rendering vector tiles happens at the end. 

## Why do "slippy maps" exist?
* Slippy maps exist because it makes it easier for the user to see adjacent areas or tiles near their point of interest. Previously, if an address bordered the edge of one tile, it would be hard for the user to find it on any other tile. Slippy maps have multiple zoom levels so it makes it easier for users to find places in the world. 

## Why would you want to install a dedicated text editor?
* A dedicated text editor is essential for writing code. These programs make it easy to write and edit codes in various formats, such as HTML or CSS. 

## What is Leaflet?
* Leaflet is an open source JavaScript library that is used to build web maps. Leaflet is open to the public and allows users to create and customize tiled web maps. 

## How has web map rendering changed over the years?
* Previously, web maps were loaded with a pre-created image that was static. Now we have tile web maps, which allow users to set their own extent to customize the way they want their map to look. Beyond tiles, current web mapping allows users to style maps using defined styles such as CartoCSS which specified how maps will look at various zoom levels. 

## What is the basemap-overlay paradigm and how are GL maps different?
* The basemap-overlay paradigm is when a map is made up of two types of layers, a basemap and the overlay. The basemap is a complete map made up of map tiles. The overlay is often any interactive data such as feature or data layers. GL maps are different because they don't have basemaps. The GL maps have sources, layers and styles. 

## Head to the Mapbox GL JS examples page and pick two examples under the user interactions section. What kind of interactions do you see? Why might you use each of those interactions?
* The first example I chose was the measure distance tool. A user might use this interaction to measure distances along a point of interest. For example, if someone was curious about how long a stretch of a river may be they could use this tool to get an approxiamte distance. The second example I chose was the update a choropleth layer by zoom level. A user might use this to examine data on a smaller scale, such as by county, rather than the state scale. 
