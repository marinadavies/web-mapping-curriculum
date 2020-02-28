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
Why might you want to create the 'centroids-selected' layer after you've created the 'centroids' layer?
Should you set the marker's lngLat and add it to the map? Why or why not?
How did you know which arguments to pass to the pip() function?
