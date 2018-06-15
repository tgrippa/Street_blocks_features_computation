# Street blocks features computation

Please cite this code using the following DOI: [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1290642.svg)](https://doi.org/10.5281/zenodo.1290642)
 
This repository contain the python script (in a jupyter notebook) used for computing landscapes metrics in street blocks or any other landscape unit defined as a shapefile to be provided by the user.

It rely on GRASS GIS and mainly on the [r.li suite](https://grass.osgeo.org/grass74/manuals/r.li.html). 
It enable for automated creation of the r.li configuration files which otherwise should be created in the graphical user interface [more info](https://grass.osgeo.org/grass75/manuals/g.gui.rlisetup.html).

The script is supposed to work with provided land cover map, NDVI, NDWI, nDSM. If any of them is missing, the user would need to adapt the code. 

**The script will compute the following landscape metrics**
Level of computation: Landscape level:
- Dominance
- Pielou
- Renyi
- Richness
- Shannon
- Simpson

Level of computation: Class level:
- *"patchnum"* : Patch number
- *"patchdensity"* : Patch density
- *"mps"* : Mean patch size
- *"padsd"* : Stand. dev. of patch size
- *"padcv"* : Patch size coef. of variation
- *"padrange"* : Range of patch size
- *"shape"* : Shape index
- *"prop_xx"* :  Proportion of the class

Street blocks morphology metrics:
- *"area"* : Area
- *"perimeter"* : Perimeter
- *"compact_circle"* : Compactness relative to a circle
- *"compact_square"* : Compactness relative to a square
- *"fd"* : Fractal dimention

Spectral metrics:
- *"ndvi_stddev"* and *"ndvi_median"* : Std. dev. and median of NDVI
- *"ndwi_stddev"* and *"ndwi_median"* : Std. dev. and median of NDWI
 
Other metrics:
- *"mean_build_height"* : Mean nDSM value of built pixels 
- *"count_buildpixels"* : Number of built pixels in the block
