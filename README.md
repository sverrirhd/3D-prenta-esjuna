# 3D-print esjan


1. Fetch the elevation model/map from: https://atlas.lmi.is/mapview/?application=DEM
![elevation map](https://github.com/sverrirhd/3D-prenta-esjuna/raw/main/images/lmi-ss.png)

2. Open the .tif file in QGIS
   1. Roughly select the boundary around the moountain in QGIS using (...)
   2. Use the "Clip" or "Extract by Mask" tool to create a new layer that only contains the area within the boundary of the mountain.
   3. Save the reduced model to another .tif file
3. Open the reduced .tif file in a jupyer notebook (link here...) using the gdal package
   1. Assuming the mountain is surrounded by a relatively flat area, further refine the clipping of the mountain by filtering all parts of the elevation map using the minimum height
   2. You should end up with something like this: (image here)
   3. Save this to file
4. Open the refined model in Blender using (...)
5. Refine the model in blender as needed. Tips:
   - Scale the mountain in the X-Y plane seperately from the Z-axis and then scale the Z-axis to the desired scale to bring out the shape of the mountain, even if the elevation is exaggerated. 
   - 