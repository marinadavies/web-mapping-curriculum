## California Wildland Fires: Identifying Wildland Urban Interface Zones, Management Status, and Bay Area Fire Threats
  Leala Lingo and Marina Davies,
  Web Mapping,
  Spring 2020,
  Univeristy of San Francisco GSAL Lab 
  
 
  
  
  ### Project description
   The intensity and size of wildfires in California have significantly increased since the 1980s (CDFW, 2020). In recent years, wildfires have been the deadliest, most destructive, costliest, and largest in state history (Forest Climate Action Team, 2018). Therefore, a map including current wildfire threat and management status will provide citizens of California and local agencies valuable information. The objective of our map is to illustrate Wildland Urban Interface (WUI) zones and land management agencies across the state. In addition, our map will identify fire threat status for the Bay Area region of California. 
  
   WUI zones are areas where structures are built near or among forests, shrublands, and grasslands (Mutch et al., 2011). These zones are subject to a higher risk of wildland fires and can have socially disastrous consequences if such fires occur (Mutch et al., 2011). It is important that citizens and agencies know where WUI zones are located throughout the state to implement management plans and help citizens be aware and prepared if a wildland fire is to occur. Land management agencies are shown on the map to inform users of the agencies that manage land of interest to them. This is important so users can look up agency management plans and strategies to reduce fire events. In addition to WUI zones and management agencies, our map will highlight the fire threat status for the Bay Area. The fire threat status shows areas that are considered at low, moderate, high, and very high risk of wildland fires. Our intention with this map is to show users who are interested in wildland fire threat and management the overall status of WUI zones in California and the agencies in charge of managing those zones. Additionally, our intention with the wildland fire threat status of the Bay Area is to inform local citizens of areas that are at risk to wildland fires so that they can prepare accordingly. 

#### Datasets and sources
WUI zones in California layer by CalFire - https://frap.fire.ca.gov/mapping/gis-data/ 

Fire Threat layer by CalFire- https://frap.fire.ca.gov/mapping/gis-data/

County Boundaries by California Department of Technology- https://data.ca.gov/dataset/ca-geographic-boundaries

California Wildland Fire Direct Protection Areas 2019 layer by U.S. Forest Service - https://www.arcgis.com/home/item.html?id=ce2d26d06f4245afb1297734a5a018e9



### Dataset meaning, purpose, barriers, additional datasets

##### WUI Zones 
The purpose of the WUI Zones dataset is to illustrate transitional areas from wildland to urban landscape. This is important for both citizens and local agencies in identifying areas that are within close proximity to lands prone to wildland fires. For citizens, this may be critical information when looking to purchase a home. For local agencies, this information may influence building code for homes within WUI areas and may aid in developing wildfire management goals or plans. WUI zones are represented as hollow polygons within the county view so users can easily identify WUI zones within their county. 

##### Bay Area Fire Threat
The fire threat layer is a product of the California Department of Forestry and Fire Protection’s Fire and Resource Assessment Program (FRAP). It is a final product of data sets combining expected fire frequency and history predicting fire behavior. The layer shows four threat classes, ranking the areas most to least vulnerable to forest fires. The purpose behind including this layer is to provide the user with a visual representation of the areas which have been deemed by fire specialists as potentially high wildland fire sites. This data is provided in raster format and will have little interaction other than to show what CA FRAP has assessed for different areas.

##### County Boundaries
County Boundaries are necessary for the user’s situational awareness while panning around the map while zoomed in. Normally, these boundaries also correspond to responsible management agencies (discussed below) and will supplement the user’s geographic understanding of the fire data being displayed.

##### California Wildland Fire Direct Protection Areas (2019)
The California Wildland Fire Direct Protection Area layer provides the user with information on what agency (federal, state, local) is responsible for managing and suppressing wildland fire throughout the state. Since each agency likely has different methods of land management, this provides the user with the ability to understand who is responsible for managing land in the area of interest. The user can then research agencies in their area and learn current/proposed fire management strategies, such as prescribed burning, removal of invasive species, and planting of fire-resilient species.

##### Additional Datasets
Other layers considered but rejected included information like historic fire boundaries of varying sizes (i.e. 5,000+ or 100,000+ acres), causes and duration of each fire, and associated vegetation types. While there were barriers to including these layers, for example integration concerns within the map, it was ultimately deemed that the raw fire data was of less use to an end user (general public, politicians), and that providing instead refined data provided by CA FRAP’s fire scientists was more useful and required less knowledge on the part of the user. The final set of layers to be used in the map were carefully selected to convey the most useful information to the end user, require the least amount of knowledge before using the map, and ultimately capture the need-to-know facts for someone interested in a particular area.


### Methodology 
The data layers selected were transformed as they were vector and raster datasets. Each dataset was simplified to remove excess information (i.e. coding internal to the department providing the data), and to make labels uniform for similar data across data sets. To simplify, we deleted unnecessary attribute fields from the attribute table of each dataset. We then used the mapshaper.org website to further simplify and smooth out polygon lines to reduce the size of the dataset. This was important because most of the data included in our map covered the state of California and were initially large file sizes. After shapefiles were simplified, we uploaded them to Mapbox and created tilesets of each dataset. Once the datasets were uploaded as tilesets, we styled our map using Mapbox Studio. From there we created a code to encompass all parts of our interactive map. Listed below is our methodology for each layer. 

##### WUI zones 
WUI zones are displayed as polygons. These zones are visible as the user zooms to county level. Along with all other data discussed below, the webpage containing the web map has a sidebar to the right of the map describing what WUI zones represent, along with citing the source for the information. The sidebar will also identify what county the user clicks on.

##### Bay Area Fire Threat Status
Originally, this dataset was a raster and needed to be converted to a shapefile. The dataset covered the entire state of California and was clipped in ArcGIS to the San Francisco Bay Area. The dataset was too large to upload as a tileset so for the scope of our project we only display fire threat status for the Bay Area. The Bay Area Fire Threat Status layer is displayed as a polygon with a fill color corresponding to the threat status (Low to Very High). The sidebar on the right will indicate what wildfire threat class the user clicks on when in the Bay Area region. Additionally, a legend will be located on the map to show users the various threat levels and corresponding color. 

##### County Boundaries 
County Boundaries are displayed as dark grey lines with the stylistic emphasis of showing the user the name of the counties being viewed and where boundaries are between counties for situational awareness. On the map, the user can click on an area within California and the sidebar will display what county the user clicked on. This is to help simplify the information generated on the map so the user doesn’t have to always zoom out to see what county they are in. 

##### Management Agency 
Management Agency will is not visually represented on the map. Instead it is a callable layer that provides the user with the information of which agency controls the clicked portion of the map. Inclusion of the visual representation of management agencies would likely clutter the map and take away from the most important geographic information of WUI and current threat status, and would confuse our situational awareness county boundaries layer. 

##### Web Map Coding 

In order to display the data prepared above, we created a web page containing a webmap coded using mapbox script and styling. To manage the overall layout of the website, we used CSS Flexboxes, coding a header box which fills the top 10% of the page while spanning the entire width and a container box filling the remaining 90% of the screen. Within the container there are two additional side-by-side boxes, the map box using 75% of the container and the data taking up the remaining 25%. Using these flexboxes allows these proportions to take up all of the available space on any computer screen accessing the data, creating a neat and functional webpage for all users regardless of computer screen size.

Next, the webmap was coded into the map flexbox. Controls were added to allow the user to zoom in and out using navigation control and to locate themselves using a geolocate feature. Then, an event listener was coded, listening for the user’s click within the map area. At the time of the click, the function pulls label data from the county, wildfire threat class, and wildfire management agency and stores it to be displayed with coding in a different flexbox.

The final flexbox displays data and has clickable links to enhance the user’s understanding of the webmap. A button was coded to allow the user to quickly zoom in on the Bay Area in order to show the functionality of the threat class layer. In future iterations of this map where state-wide data would be available, this button may not be necessary. Next, we created a space to display the data queried during the click event described above. This shows the user the county, management agency, and, currently in the bay area only, the threat class at the location of the click. Below the output of the click function, we included a legend showing the cartographic symbology for the WUI and threat classes, followed by an explanation of the layer and a link to additional information from the respective sources of the data. Finally, we provided a link to this document to further assist the user in understanding the purpose and intended use of the map.

### Challenges and Suggestions
The initial challenge for this project was to identify the most important and useful information. Because of the significant threat and recent wildfire history in California, there is an abundance of data available online, including the types of vegetation used for groundcover, the geographic extent and ignition source of wildfires dating back to the 1800s, and more. While these other datasets were interesting, they were ultimately cut from the final map as the WUI zones and threat classes were generated using wildfire history, vegetation types, and other factors as inputs. 

The next challenge was dealing with large data sets. WUI and fire threat class layers contained hundreds of thousands of points each, and were too large to load on free webmapping hosts. While WUI data was easily simplified and uploaded as a tileset, fire class data for the entire State of California remained too large to be hosted on mapbox as a single layer. For the scope and timeline of our project, we used ArcGIS to clip the data to a more manageable size. In the future, we suggest to split the state into approximately 10 equal parts, and create individual tilesets for each part so that the entirety of the fire class data could be uploaded into mapbox and eventually rendered and displayed for the user.




### References
CDFW, 2020. Science: Wildlife Impacts.  https://wildlife.ca.gov/Science-Institute/Wildfire-Impacts

Forest Climate Action Team. 2018. California Forest Carbon Plan: Managing Our
Forest Landscapes in a Changing Climate. Sacramento, CA.

Mutch, R. W., Rogers, M. J., Stephens, S. L., and Gill, A.M. 2011. Protecting lives and property in the wildland-urban interface: Communities in montana and southern california adopt australian paradigm. Fire technology 47:357-377.


