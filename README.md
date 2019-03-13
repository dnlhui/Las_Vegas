# Las_Vegas
Final Metis Project on Las Vegas

This project combined my architecture background with my data science tools. I analyzed Las Vegas’ urban zoning with an interest in residential neighborhoods. I first became interested in Las Vegas housing while researching the 2008 housing crisis. I wondered why houses in Las Vegas were so densely packed? 

Las Vegas was one of the hardest-hit cities in the sub-prime mortgage bubble. Vast amounts of desert transformed into housing tracts in the years leading up the financial crisis of 2008. I trained a Convolutional Neural Network to analyze housing patterns to identify anomalies in residential neighborhoods.

I started with Microsoft’s Github repository of every building in the United States - all 125 million. I first became aware of this dataset from a New York Times story that considered the social, cultural, and political artifacts of our built environment. 

GitHub - Microsoft Dataset of every building in the United States
https://github.com/Microsoft/USBuildingFootprints

New York Times - "A Map of Every Building in the United States"
https://www.nytimes.com/interactive/2018/10/12/us/map-of-every-building-in-the-united-states.html

I processed the data through a variety of tools. The Microsoft data came in the form of GeoJSON, with GPS coordinates for every vertex of each building. I processed the data first through QGIS, an open-source GIS program. Once I extracted a DXF vector file, I could process it using CAD software to generate PNG image files of the figure-ground relationship. 

I created 200 meter x 200 meter images of every neighborhood in Las Vegas using automated batch processing in Adobe Photoshop. However, this neighborhood data was not labelled. I turned to zoning maps from Las Vegas municipalities to programmatically assign labels to each image based on zoning type.

Las Vegas - https://www.lasvegasnevada.gov/Business/Planning-Zoning/Master-Plan/Land-Use-Environment
Henderson - http://www.cityofhenderson.com/community-development/land-use-plans/comprehensive-plan
North Las Vegas - http://www.cityofnorthlasvegas.com/departments/city_manager/about_our_city/city_maps.php
Paradise - https://www.clarkcountynv.gov/comprehensive-planning/land-use/Pages/WinchesterParadiseLandUsePlan.aspx 
Spring Valley -  https://www.clarkcountynv.gov/comprehensive-planning/land-use/Pages/SpringValleyLandUsePlan.aspx

I trained a Convolutional Neural Network to predict zoning classifications based on the images. The image to the left shows examples of where the model correctly classified images as low density residential, and where it misclassified as medium or high density residential. In each case, it is identifying housing that was built in excess compared to typical low density residential housing. Either houses were physically larger, or houses were more closely spaced together.

When analyzing the map of Las Vegas, many of these areas of overbuilding occurred in areas that grew the most during the financial crisis. View the complete project here: https://www.dnlhui.com/vegas
