## Data prep and analysis

Find at least two web mapping examples that allow for user analysis. For each example provide: 1) a link to the web map and 2) a description of the user analysis
  * https://docs.mapbox.com/help/how-mapbox-works/geospatial-analysis/
  This analysis allows you to measure a distance from point to point. 
  
  * https://docs.mapbox.com/help/tutorials/analysis-with-turf-mapbox-js/
  This analysis allows users to find the nearest hospital from a library, in case you need a doctor after visiting a library... 
  
Give an example of static data you might include on a web map. How is your example different from dynamic data?
 * An example of static data is wildland urban interface locations. These are locations that are shown as polygons and don't change. This data is analyzed before being displayed on a map. Dynamic data is analyzed right before being displayed, such as looking at a map that shows where airplanes are flying in the sky as a tracking tool. 
 
Under what circumstances might you want to do some data prep in desktop GIS before incorporating data into your web map? Give an example of the type of data that might apply here.
 * You might want to do some data prep in desktop GIS if your data is complex and needs simplifying (ie. deleting columns in attribute tables or clipping data). If your data is in esoteric or proprietary format you should use GIS to convert it. 

What are some data characteristics that can impact rendering speed? How might you address these issues?
 * If the geojson/tileset is too large it may have a slow loading time to display the map. If data has a lot of columns or unnecessary data that should be clipped, this will also slow your map loading time. To address this, you can simplify data, use mapshaper, or delete columns in desktop GIS. 

What is turf.js? Give an example of how you could apply a turf operation to a web map.
 * Turf.js is a browser that allows user to perform analysis online. Some analysis you can do is point-in-polygon, distance analysis, buffer, unit conversion, random sample, and a lot more. 

## Inline writing prompts

Describe where the centroids variable comes from. How is it possible for you to reference this variable when you didn't declare it?
 * For my map, the centroids variable was downloaded and saved onto my computer as a javascript file. I used script source to call on this file without actually referencing the variable in the code. 
 
Why might you want to create the 'centroids-selected' layer after you've created the 'centroids' layer?
 * You would want to create the centroids selected layer after the centroids layer because it would reference its data source from the centroids layer. 
 
Should you set the marker's lngLat and add it to the map? Why or why not?
 * I set the markers lngLat to the clickedLngLat so that when the user clicks on a location the lngLat will be set to that location. If you actually set a location I don't think this would work because this function is suppose to work for clicked locations. 
 
How did you know which arguments to pass to the pip() function?
 * I used the centroid and search-radius arguments so that it would select centroids within a 200 meter radius that the user clicked. 
 
