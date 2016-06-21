# Instructions to create DDL_census_data.csv


Census Block Group centroids were obtained for the Greater Washington area (attached). 

1) From openstreetmaps.org > export > Metro extracts, connected to https://mapzen.com/data/metro-extracts/ and downloaded shapefile for DC metropolitan area - I think it was the one called "dc-baltimore_maryland.imposm-shapefiles.zip"

2) Downloaded census block group shapefiles for DC, MD, VA for 2014 using the following link: https://www.census.gov/geo/maps-data/data/cbf/cbf_blkgrp.html 
 
3) Extracted the census block groups for MD and VA that intersected the polygons that defined the Metro DC area in the file downloaded from mapzen.com as descibed above in step 1.
 
4) Calculated the centroid latitude and longitude of these polygons in ArcGIS. This is also be done in QGIS, which is a free product.

5) Downloaded income and disability data for DC and surrounding census block groups from the website http://factfinder.census.gov/faces/nav/jsf/pages/index.xhtml, which was a link from the blog post http://conveyal.com/blog/2015/12/11/census-tools that had been recommended to us by Jeffrey Meisel. Used the "guided search" option to extract information, including

⋅⋅* People > Food Stamps > Disability > B22010, RECEIPT OF FOOD STAMPS/SNAP IN THE PAST 12 MONTHS BY DISABILITY STATUS FOR HOUSEHOLDS: Households; 2010-2014 American Community Survey 5-Year Estimates

6) Merged census block group shapefiles from DC and portions of MD and VA (DC metro area) with centroid latitudes and longitudes calculated (from step 4), then joined to census data on income and disability as extracted in step 5, using the census block group ID to perform the join. These steps were performed using ArcGIS.



2) Downloaded census block group shapefiles for DC, MD, VA for 20914 using: (https://www.census.gov/geo/maps-data/data/cbf/cbf_blkgrp.html) and extracted the census block groups for MD and VA that intersected the polygons that defined the Washington, DC metro area 

3) Calculated the centroid latitude and longitudes of these polygons in ArcGIS

4) Downloaded income and disability data for DC, VA, and MD at the block group level from: http://factfinder.census.gov/faces/nav/jsf/pages/index.xhtml
..* 

5) Merged census block group shapefiles with centroid lat longs calculated for DC, MD, VA, then joined to census data on icome and disability

6) File named DDL_census_data.csv, fields described below:

* ACS_14_5YR Estimate; Median household income in the past 12 months (in 2014 Inflation-adjusted dollars)
* ACS_14_5_1 Margin of Error; Median household income in the past 12 months (in 2014 Inflation-adjusted dollars)
* HD01_VD01 Estimate; Total:
* HD02_VD01 Margin of Error; Total:
* HD01_VD02 Estimate; Household received Food Stamps/SNAP in the past 12 months:
* HD02_VD02 Margin of Error; Household received Food Stamps/SNAP in the past 12 months:
* HD01_VD03 Estimate; Household received Food Stamps/SNAP in the past 12 months: - Households with 1 or more persons with a disability
* HD02_VD03 Margin of Error; Household received Food Stamps/SNAP in the past 12 months: - Households with 1 or more persons with a disability
* HD01_VD04 Estimate; Household received Food Stamps/SNAP in the past 12 months: - Households with no persons with a disability
* HD02_VD04 Margin of Error; Household received Food Stamps/SNAP in the past 12 months: - Households with no persons with a disability
* HD01_VD05 Estimate; Household did not receive Food Stamps/SNAP in the past 12 months:
* HD02_VD05 Margin of Error; Household did not receive Food Stamps/SNAP in the past 12 months:
* HD01_VD06 Estimate; Household did not receive Food Stamps/SNAP in the past 12 months: - Households with 1 or more persons with a disability
* HD02_VD06 Margin of Error; Household did not receive Food Stamps/SNAP in the past 12 months: - Households with 1 or more persons with a disability
* HD01_VD07 Estimate; Household did not receive Food Stamps/SNAP in the past 12 months: - Households with no persons with a disability
* HD02_VD07 Margin of Error; Household did not receive Food Stamps/SNAP in the past 12 months: - Households with no persons with a disability
