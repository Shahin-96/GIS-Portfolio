# Valmeyer City Relocation


## Project Overview
​In 1993, Valmeyer, Illinois, faced catastrophic flooding from the Mississippi River, leading to the inundation of the entire town and the flood water reached up to 16 feet. In response, the community made the unprecedented decision to relocate the entire town to higher ground, approximately two miles east and 400 feet above the original site. This monumental effort involved purchasing a 500-acre farm and reconstructing homes, businesses, and public facilities. In the end, roughly 700 of the 900 people who had lived in the old town relocated to the new one. The process took about four years to complete, less than half of what federal officials had forecast. The successful relocation has since been regarded as a model for communities confronting similar climate-related challenges.

| Old Valmeyer | New Valmeyer |
|-------------|-------------|
| ![Old Valmeyer](https://github.com/user-attachments/assets/042a1c29-06cd-48b8-a270-a9540ad7999c) | ![New Valmeyer](https://github.com/user-attachments/assets/46b2774c-7bfe-48ba-b404-0642ec056b3f) |



## Objectives
- Update the new city parcel layer with current data to reflect the relocation of Valmeyer.
- Attach relevant attributes (mean, minimum, and maximum elevation and slope and mean distance of each parel from original town location) to each parcel.
- Create a new road layer for Valmeyer’s relocated site to assist in transportation planning.
- Generate a publicly available web map using ArcGIS Online to visualize key spatial data. (Click <a href ="https://ucd-cpe.maps.arcgis.com/home/item.html?id=6f5bab2ff165458c98a77a761573bcdb"> Here </a> to view the map online)

### Skills Learned
- Applying zonal statistics
- Performing distance calculations
- Working with raster and vector datasets
- Utilizing spatial joins and attribute calculations
- Digitizing a new layer
- Symbolizing and labeling map features
- Creating an interactive web map with layers

### Tools Used
- ArcGIS Pro

## Steps

### 1. Data Preparation
- Obtain the provided geodatabase containing old and new parcel layers and a raster Digital Elevation Model (DEM).
- Load all datasets into ArcGIS Pro for processing.

### 2. Updating Parcel Attributes
- Use Zonal Statistics to calculate mean, minimum, and maximum elevation for each parcel in the new location.
- Apply Zonal Statistics again to compute mean, minimum, and maximum slope (in degrees).
- Generate a distance raster to compute the mean distance from the old town and attach it to the new parcels.
- Rename the fields as min_elev, max_elev, mean_elev, min_slope, max_slope, mean_slope, and move_dist for consistency.
  
### 3. Digitizing the Road Network
- Identify gaps between parcels in the new town where roads should be located.
- Allocate a new layer to road network and use the digitizing tool in ArcGIS Pro to manually draw road segments between parcels.

### 4. Creating the Web Map
- Upload the following layers to ArcGIS Online.
- Add labels for "Old Valmeyer" and "New Valmeyer" using annotations.
- Configure map settings to make it publicly accessible.

![image](https://github.com/user-attachments/assets/9e6a3c6d-4582-4154-b89e-eb383dabafe9)
