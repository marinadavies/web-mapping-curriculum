### Objects recap

An object is a series of key’s : value’s
  
What kinds of things can be included in an object?
 * Objects are key value pairs. The values can be arrays, variables, strings, or other objects. 

### Intro to “client-side”

What does client-side rendering mean in the context of web maps?
  * Client side rendering means the client has the opportunity to change the map style on the fly with minimum resources (usually this happens in the browser rather than on the server). Vector tiles can be rendered with a style, such as smaller text or specific colors for roads. This allows the map to change to a style that works best for the client. 

Why is it possible for Mapbox GL JS to place labels dynamically as you interact with the map?
  * Mapbox GL JS places labels dynamically as you interact with the map because it has a style rule for collision boxes. This rule allows the map to display labels at various zoom levels without them overlapping different labels. This makes the web application easier for the client to use. 

### Jurisdiction finder recap For the following 3 prompts, reference the working file and README.md in the jurisdiction finder explanation folder in the main class repo.

Describe how feature gets to the makeFeatureLabel() function.
  * The makeFeatureLabel function is a code that gets queried data to be displayed in a more user appropriate way. For example, given a feature, this function translates the feature's corresponding map layer (such as us-congress) to a readable name (such as US Congressional district). 
  
  * The user clicks on a feature, which kickstarts the loop for features, which calls on the featureHTML, which calls on the makefeaturelabel function, and spits out a label string (in-class explanation)

What does the getDistrictNumber() function do?
  * The getDistrictNumber function is similar to the makeFeatureLabel function. Given a feature, this code translates between the feature's corresponding map layer (sf-supervisor) and the appropriate district ID attribute name (supdist, which is district value) and then returns to the client the district ID number for whichever district they clicked on. 

Looking at the callback to map.on('click',...), what is e and why do we need it?
  * e is the event object parameter. The event object may contain information, such as lat long coordinates of a clicked location, which is important for determining where/ how interactivity (such as popups) should occur or what information to pull. The e indicates an event that occured (someone clicked) to kickstart the code that dictates what happens in the event of a "click" for example. 
