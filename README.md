# Produce LULC-Maps through satellite image classififcation
Built an Artificial Neural Network which uses the Landsat-5 data along with it's classified image as training data and the model classifies into four classes of  built-up, vegetation, barren lands and water bodies. 

We're using this classifier to generate Land-Use/Land-Cover (LULC) for the same season but different years, In this instance, I have used,
1997 multispectral image of Bangalore data to generate a LULC map for 1998. 
Another alterate method was tried where only a few training samples were taken from 1997 instead of the entire classified image and was used to predict the classified image of the city in 1997 and 1998. Code uploaded here talks into consideration of the latter, although minor changes are needed to be done to use the former method to generate LULC maps 


# Results 
-As the spectral reflectance of the sun changes every year, we need to measure the devaitions before using it to predict the LULC maps (plot and check the bands on ploty-chart studio)

-This approach of prediction works only when the season is same, when we build the classifier for summer season and try to predict for winter season,
the margin of error increases.

-Taking care of the above factors the exported classified image for 1998, gave a statistics of area-wise accuracy ~90% (Checked in Q-GIS)

-Classified Image of 1997 gave a statistics of area-wise accuracy of ~95% (Checked in Q-GIS)


# Reqirements

1) gdal

2) tensorflow

3) Most of the related data can be found in usgs explorer website

# Future work
Feel free to use the code, and any future collaborations/suggestions to work on the project are always welcome.

