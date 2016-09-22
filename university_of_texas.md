# The University of Texas at Austin in QGIS: Creating New Vector Data from Historical Maps (Campus Maps)
[Originally used Monday April 4, 2016]
[Modified September 9, 2016]
### This tutorial is designed to reinforce the skills learned in [Programming Historian QGIS Tutorial\#3](http://programminghistorian.org/lessons/vector-layers-qgis "Links to Programming Historian")

1. Using your preferred web browser, visit the **Natural Earth** website: http://www.naturalearthdata.com/, and download all 10m Cultural Themes.  The Cultural large scale data file will be a rather large zip.file (about 200MB).  To download the data, click on "Get Data" on the home page and then "Cultural" under *Large scale data, 1:10m* and then "Download all 10m cultural themes".  (See images 0001.png thru 0004.png.)

2. Save and Extract the downloaded zip.file (10m_cultural.zip) to you computer's hard drive.

3. Having extracted the 10m_cultural folder, open QGIS and start a new project.  Set the CRS to 3081 - NAD83 / Texas State Mapping System. (See image 0005.png.)
 
4. When you click on the vector icon, and browsing the 10m_cultural folder, review how many and what different kinds of shp.files there are in the folder.  (See image 0006.png.)

5. Add the following vector files.  (See image 0007.png.) Go in this order and look at each file as the files render in QGIS. Use the zoom tools as needed to change the render image.  Drag the vector up and down in the Layers Panel to change the order as needed or that makes the most sense to you.  Turn the label on for the ne_10m_roads.shp layer so you can see how the names of roads are rendered.
 
   - QGIS\10m_cultural\10m_cultural\ne_10m_admin_1_states_provinces_shp.shp
   - QGIS\10m_cultural\10m_cultural\ne_10m_admin_1_states_provinces_lines_shp.shp
   - QGIS\10m_cultural\10m_cultural\ne_10m_urban_areas.shp
   - QGIS\10m_cultural\10m_cultural\ne_10m_roads.shp
   - QGIS\10m_cultural\10m_cultural\ne_10m_railroads_north_america.shp
  
6. Try zooming in on the continental United States of America.  Try zooming in Texas.  Try zooming in on what appears to be Austin, Tx.  (See images 0008.png thru 0010.png.)  Notice that the 10m_cultural shp.files do not give you city level information.

7. For city level information pertaining to Austin, Tx., visit the **City of Austin's GIS Data Sources** website at: https://austintexas.gov/page/gis-data-sources.  Click on the link: City of Austin GIS Data Sets. (See image 0011.png.)    
 
8. Notice how much and what kind of information the City of Austin has available.  For the purposes of our tutorial, you will need to download the following data sets.  To download the data sets, click on the Description name.  When the webpage refreshes to take you a visual representation of that particular data, use the *Export* button in the upper right-hand corner to download the corresponding zip.file.  (See image 0012.png.) Be sure to select the "*Shapefile*" option when exporting.

    * Lakes and Ponds [*downloads as Hydrogaphy Polygons*]
    * Street Centerlines (Streets/Roads) [*downloads as Street Segment*]
    * Urban Roadways [*downloads as Urban Roadways*]
 
9. Once the City of Austin GIS zip.files have been downloaded and extracted, upload each shp.file into QGIS.  There should be a total of 3 shp.files being added.  (See image 0013.png.)  Your QGIS rendered view should look something like image 0014.png.

10. Now you will need to add Raster files; two historical maps for the purpose of this tutorial.  To show change over time within the City of Austin, and specifically looking at The University of Texas at Austin campus since its formation, visit the **University of Texas Libraries**' *Perry-Castaneda Library Map Collection* at: http://www.lib.utexas.edu/maps/ut_austin_historical_maps.html.  For this tutorial, we will be using the *University of Texas Campus Map 1933* and *University of Texas Campus Map 1944*.  (Note: You will need to geo-reference any of the maps you wish to download from the UTAustin Library web site.

11. Add Raster: *University of Texas Campus Map 1933*. Note: Again, if downloading directly from the UT Library website, you will have to geo-reference the map.
 
12. Add Raster: *University of Texas Campus Map 1944*. Note: See note in Step 11 if you have not already geo-referenced this file.

13. Create a Point shp.file called “points\_interest’. In that file you will use points to locate buildings from the 1944 map and compared agains the 1933.  The objective is to see how much, in an 11 year span, the UT Austin campus had changed.  [HINT: For viewing convenience, open the 1933 and 1944 campus maps in a separate image viewer] 
   
   Build an attribute table for these points, with these attributes:
    * Name
    * Year [will be the same as the map]
   
    Note: See image 0015.png.  When done and prompted to save as shp.file, save the new point shp.file as *Landmarks*.  (See image 0016.png.)

 Edit the new Point shp.file
    * Add 4 points from the 1944 Campus Map
    * Add 2 points from the 1933 Campus Map
    * Change “properties” to display the new name and date info

14. Create a Line shp.file for roads and an attribute table with these fields
    * Name
    * Year
   
    Trace 4 roads from the 1944 map and them to compare to modern roads
   
    Note: See image 0015.png, but select *Line*.  When done and prompted to save as shp.file, save the new point shp.file as *roads* as previously done in Step 13 with image 0016.png.
    

15. Create a new Polygon shp.file with "building_name" and "year" attributes
    * Trace 2 buildings as polygons, assisted by the 'snapping' function

16. Save the whole project as a “UT Austin Campus.qgs” file so you can load it later.

17. Zoom in on the UT Austin Campus to a view rendering that shows the new vector files, but NOT the historical maps.  (See image 0017.png.)

18. Open Print Composer; then Layout, then Add Map to show this downtown area. Leave enough space at the top or bottom of the page for your title

19. Go back to the main screen of QGIS, Zoom out to show the full extent of Louisiana. Turn off the buildings and roads areas [to speed up loading]

20. Then back in Print Composer, add an insert map [Layout/Add Map] that shows the whole state.
    * Put frames around both Map0 and Map1
    * Add a scalebar in Map0, with units in feet [Layout/Add Scalebar]
    * Add a Title to the map [Layout/AddLabel] and add another smaller label identifying the sources of the data.

21. Save the printer composer file and then export a PDF[Composer/Export as PDF]. Put your last name in the PDF filename and upload it to Blackboard.  (See PDF: AustinTX_and_UTAustin Campus - Sebastian Fuentes.pdf.)

### Data sources for this tutorial:
1. Cultural data used to obtain Texas map information was obtained from Natural Earth: http://www.naturalearthdata.com/.

2. City of Arlington data from the GIS Data Sources website: https://austintexas.gov/page/gis-data-sources. 

3. *University of Texas Campus Map 1933* map from *Sanborn Fire Insurance Maps*. 2MB. Obtained from University of Texas Libraries' Perry-Castaneda Library Map Collection: http://www.lib.utexas.edu/maps/ut_austin_historical_maps.html. September 21, 2016.

4. *University of Texas Campus Map 1944* map from *UT Buildings Collection, Alexander Architectural Archive, University of Texas*. 682KB. Obtained from University of Texas Libraries' Perry-Castaneda Library Map Collection: http://www.lib.utexas.edu/maps/ut_austin_historical_maps.html. September 21, 2016.
