# Sentinel Blue-green Algae Test
Determine whether Sentinel satellite data can be used to map extent and severity of Blue-Green Algae outbreaks in the Gippsland Lakes

## Background:
Toxic algal blooms are a frequent occurrence in the Gippsland Lakes and require emergency response & monitoring.
High-resolution satellite imagery & data are available through Sentinel Hub, and a quick look returned some encouraging images using custom scripts provided by other users: 

#### Ulyssys Water Quality Viewer (UWQV)
A custom script to dynamically visualize the chlorophyll and sediment conditions of water bodies on Sentinel-2 and Sentinel-3 images. Authored by by András Zlinszky and Gergely Padányi-Gulyás. Winner of the 2nd Sentinel Hub Custom Script Contest.
![image](https://user-images.githubusercontent.com/100050237/161180006-81f553b5-a0bd-4820-b6f0-5a6ef336c8d5.png)
* https://custom-scripts.sentinel-hub.com/custom-scripts/sentinel-2/ulyssys_water_quality_viewer/
* More info: https://medium.com/sentinel-hub/water-quality-information-for-everyone-a81faab8ff5e

#### Sentinel-2 Water Quality (Se2WaQ)
The Se2WaQ - Sentinel-2 Water Quality - script by Nuno Sidónio and Andrade Pereira uses Sentinel-2 products (L1C & L2A) to display the spatial distribution of six relevant indicators of water quality: (i) the concentration of Chlorophyll a (Chl_a), (ii) the density of cyanobacteria (Cya), (iii) turbidity (turb), (iv) colored dissolved organic matter (CDOM), (v) dissolved organic carbon (DOC), and (vi) water color (Color).
![image](https://user-images.githubusercontent.com/100050237/161179412-2dd927ee-02ba-475a-abe7-6fe3a76dace9.png)
* https://custom-scripts.sentinel-hub.com/custom-scripts/sentinel-2/se2waq/

#### Other available scripts:
* https://custom-scripts.sentinel-hub.com/sentinel-2/cyanobacteria_chla_ndci_l1c
* https://custom-scripts.sentinel-hub.com/sentinel-2/maximum_peak_height_bloom_index
* https://custom-scripts.sentinel-hub.com/sentinel-2/apa_script

## Method:
1. Capture satellite data (requires relatively clear conditions at time of satellite fly-over).
2. Collect water samples to match.
3. Test whether usable relationships exist between satellite data and lab results from water testing.

### Random Notes:
How to extract Sentinel satellite data to GeoTIFF for further analysis in ArcGIS:
* https://www.copernicus-user-uptake.eu/fileadmin/FPCUP/dateien/resources/2018-1-06/Guide_basics_satellite_data_english.pdf
