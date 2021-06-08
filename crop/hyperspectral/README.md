# Hyperspectral Pipeline/Claibration for season 9 VNIR

### Introduction

- [hs_crop.py](https://github.com/GWUvision/OPEN/blob/master/crop/hyperspectral/hs_crop.py) file provides the necessary functions 
to process raw hyperspectral data from Terra Sorgum season 9 
- For each hyperspectral scan the code will output:
  - a h5 file that is the PCA representation of the 15 most important components
  - a calibrated reduced dimensionality (by 10 in both x and y direction) nc file 
  - a rgb representation of the plot capture (full resolution)
  - a json that has field coordinates of the capture

### Required Python libraries

- Base libraries: `os`,`numpy`, `math`, `json`, `h5py`, `PIL` 
- Special libraries:
  - `netCDF4`: for reading the uncalibrated hyperspectral files
  - `terra_common`: TERRA project library used for obtaining the plot level coordinates used for cropping the scan files with multiple plots
  - `sklearn.utils.extmath`: used for PCA reduction of the most important 15 features
  
