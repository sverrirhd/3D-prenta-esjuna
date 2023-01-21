# 3D-print esjan


1. Fetch the elevation model/map from: https://atlas.lmi.is/mapview/?application=DEM
![elevation map](https://github.com/sverrirhd/3D-prenta-esjuna/raw/main/images/lmi-ss.png)

2. Open the .tif file in QGIS
   1. Compute the contour lines for the mountain to better see its outline ![contour](https://github.com/sverrirhd/3D-prenta-esjuna/raw/main/images/qgis-contour.png)
   2. Roughly select the boundary around the moountain in QGIS and draw it's outline ![outline](https://github.com/sverrirhd/3D-prenta-esjuna/raw/main/images/qgis-contour-freehand.png)
   3. Use the "Clip" or "Extract by Mask" tool to create a new layer that only contains the area within the boundary of the mountain.![cropped with hillside visual](https://github.com/sverrirhd/3D-prenta-esjuna/blob/main/images/esjan-cropped.png)
   4. Save the reduced model to another .tif file
3. Open the .tif file in blender using the Blender GIS plugin
   1. Extrude the surface directly downwards 
   2. Cut off the bottom part of the volume with a block using a boolean modifier to subtract the bottom part of the block
   3. You should be left with a 3D volume that looks like this ![3D volume](https://github.com/sverrirhd/3D-prenta-esjuna/raw/main/images/Blender-final.png) 
4. Refine the model in blender as needed. Tips:
   - Scale the mountain in the X-Y plane seperately from the Z-axis and then scale the Z-axis to the desired scale to bring out the shape of the mountain, even if the elevation is exaggerated. 
   - 