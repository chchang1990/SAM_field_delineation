# Delineating Crop Field Boundaries from Sentinel-2 (S2) imagery using the Segment-Anything Model (SAM)

**GPU runtime is suggested to run this script.**

This script delineates the crop field boundaries on S2 imagery by using the <i>segment-geospatial</i> Python package developed by Prof. Qiusheng Wu at the University of Tennessee, Knoxville. The <i>segment-geospatial</i> package utilizes Meta's Segment-Anything Model (SAM) to generate segmented masks of different features on a remote sensing imagery as separated polygons. Hence, theoretically, if SAM is applied over the croplands, the boundaries of the segmented polygons can be considered as the crop field boundaries.


This script attempts to answer two questions:    
1. If SAM can really be used to delineate the crop field boundaries?

2. Since false-color image enhance the contrast between crops that have different health conditions, can SAM reveal the boundaries between crops that have different health conditions if it is applied to false-color image?

To answer these two question, I retrieved both S2 true-color and false-color images from the Google Earth Engine, then delineated the crop field boundaries using SAM. The results were compared with the USDA Cropland Data Layer, as well as the coincident S2 NDVI image. 

The results showed that the boundaries delineated from both types of imagery generally agree with the boundaries shown on the USDA Cropland Data Layer. This indicates that SAM can be used as a tool that quickly delineate the field boundaries.

In addition, the field boundaries delineated from the false-color image seem to better reveal some details shown on the NDVI image, indicating that applying SAM on the false-color image may be used to show the boundaries between crops that have different health conditions. However, more examination on the delineated results should be inspected to reach a solid conclusion.



