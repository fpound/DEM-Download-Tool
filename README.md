# DEMDownload Tool
## A simple tool to download a Digital Elevation Model in the Contiguous United States (CONUS) from an Area of Interest (AOI)

### Inputs
The tool can make an AOI from the extents (bounding box) of a Shapefile (SHP), or of a TIF file.
However, with simple modification, additional file types supported by Geopandas and Rasterio would be possible.


### Fuctionality
With an AOI, the tool uses requests to access *The National Map's* API. It is hardcoded to fetch the **National Elevation Dataset 1/3 Arc Second DEM**. This is approximately 10m resolution. This dataset is available over the entire CONUS. 

Occasionally, DEMs are updated, and newer and older DEMs are hosted and available for a given area. The Download_DEM function's variable Newest defualts to True, meaning, only the newest DEM is downloaded. If older DEMs are desired, set Newest=False.




### Required packages
- geopandas
- os
- requests
- rasterio
- shapely
