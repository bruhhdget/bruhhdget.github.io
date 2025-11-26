---
title: "UMBC Portfolio"
excerpt: "Short description of portfolio item number 1<br/><img src='/images/IMG_9167.png'>"
collection: portfolio
---

# **Describing the Relationship Between Suburban Land Use on Mountain Lion Sightings in California**

**Overview**  
In this assignment for a GIS course at UMBC, I created a dashboard and analyzed point-level data on Mountain Lion Sightings from iNaturalist. The end goal of this assignment was to discover the challenges of coexistence with humans in California and mountain lions, caused by increased suburban developments and migration. 

**Data**

* Mountain Lion Sightings- Point shapefile of Mountain Lion Sightings containing verified, research-grade photographs of the animal or its tracks and other markings in the state of California. This data was downloaded from iNaturalist and provided by my professor in a .zip file.

**Workflow**  
On ArcGIS Online, I began by uploading the mountain lion observation zip file and creating a web map illustrating the spatial location of the mountain lion reports. I symbolized the points according to whether the mountain lion sightings were near human activity and added a pie chart to visualize this data. Then, I created an indicator counter and an interactive sidebar that filters sightings based on land use category and updates the map automatically. 

**Dashboard URL:**  
[**https://umbc-ges.maps.arcgis.com/apps/dashboards/0fe14eadbaa54f2084be3e4eeaefd724**](https://umbc-ges.maps.arcgis.com/apps/dashboards/0fe14eadbaa54f2084be3e4eeaefd724)

# **Top 5 Trees in Poor or Dead Health**

**Overview**  
This project was an assignment for a GIS course I took at UMBC and it maps the distribution of city trees in Baltimore that are in poor health or dead. The data used was provided by my professor and it was a points shapefile representing the locations of street and other trees maintained by Baltimore City and a polygon shapefile representing the boundary of Baltimore City.

**Workflow**  
In ArcGIS Pro, I began by loading in the data (tree points and Baltimore City polygon) and used a summary command to aggregate my data based on tree type (genus) and opted to only visualize the top 5 most common trees. Then, using a selection query I selected the trees which were either dead or in poor health and visualized them on two maps. Finally, I created charts showing the counts for each genus, and pie charts separated by genus, comparing whether it was dead or in poor condition.  

![Baltimore tree health map](https://raw.githubusercontent.com/bruhhdget/bruhhdget.github.io/master/images/balt_tree_health_portfolio.png)


# **Maryland’s Forestation Land Cover Patterns For Carbon Sequestration**

**Overview**  
This final project for a remote sensing course at UMBC, my peers and I aimed to answer the question: “How do the changes in tree forestation land cover and carbon sequestration capacity over the past two decades differ among three distinct geographic regions in Maryland, and how have these changes been influenced by urbanization and reforestation efforts in each area?” By mapping forested and non-forested areas we were able to visualize shifts in carbon sequestration potential and evaluated Maryland’s reforestation project effectiveness. 

**Methods and Data**  
We began by separating Maryland into four physically distinct sample areas (Western Maryland Garrett County, Piedmont Plateau slightly west of Baltimore, Baltimore and Washington metropolitan areas, and the Eastern Shore). Then using images downloaded from Landsat 7 and Landsat 8 satellites, created classification maps to highlight forested and non-forested areas over a 20-year period (2001 and 2021\) on GEE Code Editor. Bodies of water were masked out to clean the data. We incorporated carbon sequestration projections (2019) from a 2019 NASA DAAC and used the raster calculator in ArcGIS Pro to calculate carbon sequestration potential:  
	Classification Map ✕ Carbon Sequestration Potential Map

**Findings**  
Overall Growth in Forested Land and Carbon Sequestration:

* Significant increase over the past 20 years across Maryland.  
* Particularly notable in the Baltimore-Washington metropolitan area and the Eastern Shore.


Baltimore-Washington Metropolitan Area:

* Expansion of green spaces despite urban development.  
* Suggests the success of urban forestry programs in enhancing carbon capture.


Eastern Shore:

* Increase in forestation, likely due to a shift from agricultural to forest land.  
* Development of young forests with high carbon uptake.

Challenges:

* Persistent issues with invasive species and development pressures.

![Map of Forest regrowth](https://raw.githubusercontent.com/bruhhdget/bruhhdget.github.io/master/images/forest_map.png)

# **Creating Spatial Data \+ Coordinate Reference System Work**

**Overview**  
This was an assignment for a GIS course at UMBC. In this assignment the goal was to learn more about the significance of projections, how to georeference an image, and create a new feature class in ArcGIS Pro.

**Part 1: Georeferencing Baltimore’s Historical Redlining**

**Workflow**  
Starting with the point shapefiles provided within the assignment, I used the Project tool in ArcGIS Pro to map these points in the NAD 1983 projection to use as reference points. Next, using the georeferencing tool, I aligned a .tif image of Baltimore’s historical redlining map to the reference points. Finally, with the clip raster tool, I constrained the image’s extent to fit Baltimore City’s Boundaries.  

![Map of georeferenced points](https://raw.githubusercontent.com/bruhhdget/bruhhdget.github.io/master/images/portfolio_map4.png)

**Part 2: Editing and Digitizing HOLC Classifications**

**Workflow**  
In this assignment I was given a digitized version of HOLC classifications of Baltimore neighborhoods with 4 polygons missing; my task was to recreate these missing polygons. I began by uploading the polygon shapefile and my previously referenced .tif image of Baltimore HOLC classifications on ArcGISPro. I made sure snapping was turned on to prevent overlap in the polygons and my layers were ordered such that the .tif was underneath the polygon layer. Then with the polygon tool, I retraced the missing polygons using the .tif underneath as reference. Finally, I updated the attribute to assign the appropriate classifications of the newly created polygons based on the reference image.   

![Map of Reconstructed Polygons](https://raw.githubusercontent.com/bruhhdget/bruhhdget.github.io/master/images/portfolio_map5.png)

# **Querying Baltimore – Data Tables, Joins, and Selection**

**Overview**  
This map was part of an assignment for a GIS course I took at UMBC. The objective was to explore table joins with large datasets and applying SQL-based selection queries to derive meaningful information from feature classes.

**Data**

* Balt\_tracts.shp: polygon shapefile of Baltimore City Tracts from the Census Bureau  
* Rec\_Centers.shp: point shapefile representing all recreation centers in Baltimore   
* Groceries.shp: points shapefile representing the locations of grocery stores in Baltimore as of 2023\. At Open Baltimore ([http://data.baltimorecity.gov/](https://data.baltimorecity.gov/)), there is a disclaimer that says this file may not be complete.

**Workflow**  
I began by adding the data on a map in ArcGISPro. Then, I performed a table join, linking the attribute tables of the grocery stores and recreation centers to the attribute table of Baltimore City’s tracts. To filter the data, I performed a selection query selecting all tracts containing recreation centers and grocery stores. Finally,I created a new field called “area”, and used the Calculate Geometry tool to find the area of each tract.   

![Map of Areas of Interest](https://raw.githubusercontent.com/bruhhdget/bruhhdget.github.io/master/images/portfolio_map6.png)







