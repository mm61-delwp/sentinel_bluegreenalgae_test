# Sentinel Blue-green Algae Test
Determine whether Sentinel satellite data can be used to map extent and severity of Blue-Green Algae outbreaks in the Gippsland Lakes

## Background:
Toxic algal blooms are a frequent occurrence in the Gippsland Lakes and require emergency response & monitoring.
High-resolution satellite imagery & data are available through Sentinel Hub, and a quick look returned some encouraging images using custom scripts provided by other users: 
* https://custom-scripts.sentinel-hub.com/custom-scripts/sentinel-2/se2waq/
* https://custom-scripts.sentinel-hub.com/custom-scripts/sentinel-2/ulyssys_water_quality_viewer/


Others are available but have issues with these:
* https://custom-scripts.sentinel-hub.com/sentinel-2/cyanobacteria_chla_ndci_l1c
* https://custom-scripts.sentinel-hub.com/sentinel-2/maximum_peak_height_bloom_index
* https://custom-scripts.sentinel-hub.com/sentinel-2/apa_script

More information
* https://medium.com/sentinel-hub/water-quality-information-for-everyone-a81faab8ff5e

## Method:
1. Capture satellite data (requires relatively clear conditions at time of satellite fly-over).
2. Collect water samples to match.
3. Test whether usable relationships exist between satellite data and lab results from water testing.

### Random Notes:
How to extract Sentinel satellite data to GeoTIFF:
https://www.copernicus-user-uptake.eu/fileadmin/FPCUP/dateien/resources/2018-1-06/Guide_basics_satellite_data_english.pdf
