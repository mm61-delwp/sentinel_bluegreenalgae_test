# Sentinel Blue-green Algae Test
Determine whether Sentinel satellite data can be used to map extent and severity of Blue-Green Algae outbreaks in the Gippsland Lakes

## Background:
Toxic algal blooms are a frequent occurrence in the Gippsland Lakes and require emergency response & monitoring.
High-resolution satellite imagery & data are available through Sentinel Hub, and user-contributed scripts return some encouraging images indicating potential to adopt existing remote sensing technology for mapping extent and severity of blooms.

#### Ulyssys Water Quality Viewer (UWQV)
A custom script to dynamically visualize the chlorophyll and sediment conditions of water bodies on Sentinel-2 and Sentinel-3 images. Authored by by András Zlinszky and Gergely Padányi-Gulyás. Winner of the 2nd Sentinel Hub Custom Script Contest.
![image](https://user-images.githubusercontent.com/100050237/161180006-81f553b5-a0bd-4820-b6f0-5a6ef336c8d5.png)
* https://custom-scripts.sentinel-hub.com/custom-scripts/sentinel-2/ulyssys_water_quality_viewer/
* More info: https://medium.com/sentinel-hub/water-quality-information-for-everyone-a81faab8ff5e
* Live example: [25th March 2022](https://apps.sentinel-hub.com/sentinel-playground/?source=S2&lat=-37.958816425021716&lng=147.5196075439453&zoom=11&preset=CUSTOM&layers=B01,B02,B03&maxcc=20&gain=1.0&gamma=1.0&time=2021-09-01%7C2022-03-25&atmFilter=&showDates=false&evalscript=Y29uc3QgUEFSQU1TID0gewogIC8vIEluZGljZXMKICBjaGxJbmRleDogJ3JsaCcsCiAgdHNzSW5kZXg6ICdkZWZhdWx0JywKICB3YXRlcm1hc2tJbmRpY2VzOiBbJ25kd2knLCAnaG9sJ10sCiAgLy8gTGltaXRzCiAgY2hsTWluOiAwLjAwNiwKICBjaGxNYXg6IDAuMDQ1LAogIHRzc01pbjogMC4wNzUsCiAgdHNzTWF4OiAwLjE4NSwKICB3YXRlck1heDogMCwKICBjbG91ZE1heDogMC4wMiwKICAvLyBHcmFwaGljcwogIGZvcmVncm91bmQ6ICdkZWZhdWx0JywKICBmb3JlZ3JvdW5kT3BhY2l0eTogMS4wLAogIGJhY2tncm91bmQ6ICdkZWZhdWx0JywKICBiYWNrZ3JvdW5kT3BhY2l0eTogMS4wCn07CmZ1bmN0aW9uIGdldEluZGljZXModCl7cmV0dXJuIHQ%2Fe25hdHVyYWw6IlsxLjAqQjA3KzEuNCpCMDktMC4xKkIxNCwxLjEqQjA1KzEuNCpCMDYtMC4yKkIxNCwyLjYqQjA0LUIxNCowLjZdIixjaGw6e2ZsaDoiQjEwLTEuMDA1KihCMDgrKEIxMS1CMDgpKigoMC42ODEtMC42NjUpLygwLjcwOC0wLjY2NSkpKSIscmxoOiJCMTEtQjEwLShCMTgtQjEwKigoMC43MDg3NS0wLjY4MTI1KSoxMDAwLjApKS8oKDAuODg1LTAuNjgxMjUpKjEwMDAuMCkiLG1jaToiQjExLSgoMC43NTM3NS0wLjcwODc1KS8oMC43NTM3NS0wLjY4MTI1KSkqQjEwLSgxLjAtKDAuNzUzNzUtMC43MDg3NSkvKDAuNzUzNzUtMC42ODEyNSkpKkIxMiJ9LHRzczp7YjA3OiJCMDciLGIxMToiQjExIn0sd2F0ZXJtYXNrOntuZHdpOiIoQjA2LUIxNykvKEIwNitCMTcpIn19OntuYXR1cmFsOiJbMi41KkIwNCwyLjUqQjAzLDIuNSpCMDJdIixjaGw6e3JsaDoiQjA1LUIwNC0oQjA3LUIwNCooKDAuNzA1LTAuNjY1KSoxMDAwLjApKS8oKDAuNzgzLTAuNjY1KSoxMDAwLjApIixtY2k6IkIwNS0oKDAuNzQtMC43MDUpLygwLjc0LTAuNjY1KSkqQjA0LSgxLjAtKDAuNzQtMC43MDUpLygwLjc0LTAuNjY1KSkqQjA2In0sdHNzOntiMDU6IkIwNSJ9LHdhdGVybWFzazp7bmR3aToiKEIwMy1CMDgpLyhCMDMrQjA4KSJ9fX1mdW5jdGlvbiBibGVuZCh0LG4sZSxyKXtyZXR1cm4gdC5tYXAoKGZ1bmN0aW9uKHQsbCl7cmV0dXJuIHQvMTAwKmUrbltsXS8xMDAqcn0pKX1mdW5jdGlvbiBnZXRBbHBoYSh0LG4sZSl7cmV0dXJuIG4rKGUtbikvMjx0PzEwMDp0PD1uPzA6dD49ZT8xOih0LW4vMikvKGUtbikqMTAwfWZ1bmN0aW9uIGdldENvbG9ycyh0LG4sZSxyLGwpe2xldCBhLEI7c3dpdGNoKHQpe2Nhc2UiY2hsIjpCPVtbLjAwMzQsLjAxNDIsLjE2M10sWzAsLjQxNiwuMzA2XSxbLjQ4NiwuOTgsMF0sWy45NDY1LC44NDMxLC4xMDQ4XSxbMSwwLDBdXSxsJiYoQj1CLnJldmVyc2UoKSxlKj0xMCxyLz0xMCksYT1jb2xvckJsZW5kKG4sW2UsZSsoci1lKS8zLChlK3IpLzIsci0oci1lKS8zLHJdLEIpO2JyZWFrO2Nhc2UidHNzIjpCPVtbLjk2MSwuODcxLC43MDJdLFsuMzk2LC4yNjMsLjEyOV1dLGE9Y29sb3JCbGVuZChuLFtlLHJdLEIpfXJldHVybiBhfWZ1bmN0aW9uIGlzUHVyZVdhdGVyKHQpe3JldHVybiB0P0IwNjwuMzE5JiZCMTc8LjE2NiYmQjA2LUIxNj49LjAyNyYmQjIwLUIyMTwuMDIxOkIwMzwuMzE5JiZCOEE8LjE2NiYmQjAzLUIwNz49LjAyNyYmQjA5LUIxMTwuMDIxfWZ1bmN0aW9uIGlzQ2xvdWQodCxuKXtjb25zdCBlPW4%2FKEIwNC0uMTc1KS8oLjM5LS4xNzUpOihCMDItLjE3NSkvKC4zOS0uMTc1KTtyZXR1cm4gZT4xfHxlPjAmJihCMDQtQjA2KS8oQjA0K0IwNik%2BdH1mdW5jdGlvbiBnZXRFdmFsKHMpe3JldHVybiBldmFsKHMpfWZ1bmN0aW9uIGlzV2F0ZXIodCxuLGUscixsKXtpZigwPT09bi5sZW5ndGgpcmV0dXJuITA7e2xldCBhPSEwO2ZvcihsZXQgQj0wO0I8bi5sZW5ndGg7QisrKXtjb25zdCB1PW5bQl07aWYoIm5kd2kiPT11JiZnZXRFdmFsKHQubmR3aSk8ZSl7YT0hMTticmVha31pZigiaG9sIj09dSYmIWlzUHVyZVdhdGVyKGwpKXthPSExO2JyZWFrfWlmKCJiY3kiPT11JiZpc0Nsb3VkKHIsbCkpe2E9ITE7YnJlYWt9fXJldHVybiBhfX1mdW5jdGlvbiBnZXRCYWNrZ3JvdW5kKHQsbixlKXtsZXQgcixsPSExO2NvbnN0IGE9cGFyc2VJbnQoMTAwKmUpO3JldHVybiJkZWZhdWx0Ij09PXR8fCJuYXR1cmFsIj09PXQ%2FKHI9Z2V0RXZhbChuKSxsPSEwKTpyPSJibGFjayI9PT10P1swLDAsMF06IndoaXRlIj09PXQ%2FWzEsMSwxXTpnZXRTdGF0aWNDb2xvcih0KSxsfHwxPT09ZT9yOmJsZW5kKHIsZ2V0RXZhbChuKSxhLDEwMC1hKX1mdW5jdGlvbiBnZXRGb3JlZ3JvdW5kKHQsbixlLHIpe2xldCBsO2NvbnN0IGE9cGFyc2VJbnQoMTAwKnIpO3JldHVybiBsPSJuYXR1cmFsIj09PXQ%2FZ2V0RXZhbChlKTpnZXRTdGF0aWNDb2xvcih0KSwxPT09cj9sOmJsZW5kKGwsbixhLDEwMC1hKX1mdW5jdGlvbiBnZXRTdGF0aWNDb2xvcih0KXtyZXR1cm5bdFswXS8yNTUsdFsxXS8yNTUsdFsyXS8yNTVdfWZ1bmN0aW9uIGdldFZhbHVlKHQpe2xldCBuLGUscixsLGE7Y29uc3QgQj10LmNobEluZGV4LHU9dC50c3NJbmRleCxvPXQuYmFja2dyb3VuZCxzPXQuZm9yZWdyb3VuZCxjPXQuZm9yZWdyb3VuZE9wYWNpdHksaT0idW5kZWZpbmVkIiE9dHlwZW9mIEIxOCxkPWdldEluZGljZXMoaSksZj1nZXRCYWNrZ3JvdW5kKG8sZC5uYXR1cmFsLHQuYmFja2dyb3VuZE9wYWNpdHkpO2lmKCFpc1dhdGVyKGQud2F0ZXJtYXNrLHQud2F0ZXJtYXNrSW5kaWNlcyx0LndhdGVyTWF4LHQuY2xvdWRNYXgsaSkpcmV0dXJuIGY7aWYoImRlZmF1bHQiIT09cylyZXR1cm4gZ2V0Rm9yZWdyb3VuZChzLGYsZC5uYXR1cmFsLGMpO2xldCBnO2lmKG51bGwhPT1CKXtjb25zdCByPSJkZWZhdWx0Ij09PUI%2FaT8iZmxoIjoibWNpIjpCO249Z2V0RXZhbChkLmNobFtyXSksZT1nZXRDb2xvcnMoImNobCIsbix0LmNobE1pbix0LmNobE1heCxpJiYiZmxoIj09PXIpfWlmKG51bGwhPT11KXtjb25zdCBuPSJkZWZhdWx0Ij09PXU%2FaT8iYjExIjoiYjA1Ijp1O3I9Z2V0RXZhbChkLnRzc1tuXSksbD1nZXRDb2xvcnMoInRzcyIscix0LnRzc01pbix0LnRzc01heCksYT1nZXRBbHBoYShyLHQudHNzTWluLHQudHNzTWF4KX1nPW51bGwhPT1CJiZudWxsIT09dT9ibGVuZChsLGUsYSwxMDAtYSk6bnVsbCE9PUImJm51bGw9PT11P2U6bnVsbCE9PXUmJm51bGw9PT1CP2JsZW5kKGwsZixhLDEwMC1hKTpmO2NvbnN0IGg9cGFyc2VJbnQoMTAwKmMpO3JldHVybiAxPT09Yz9nOmJsZW5kKGcsZixoLDEwMC1oKX1yZXR1cm4gZ2V0VmFsdWUoUEFSQU1TKTsK)
* Note: set `chlIndex: 'rlh', chlMin: 0.006, chlMax: 0.045`
#### Sentinel-2 Water Quality (Se2WaQ)
The Se2WaQ - Sentinel-2 Water Quality - script by Nuno Sidónio and Andrade Pereira uses Sentinel-2 products (L1C & L2A) to display the spatial distribution of six relevant indicators of water quality: (i) the concentration of Chlorophyll a (Chl_a), (ii) the density of cyanobacteria (Cya), (iii) turbidity (turb), (iv) colored dissolved organic matter (CDOM), (v) dissolved organic carbon (DOC), and (vi) water color (Color).
![image](https://user-images.githubusercontent.com/100050237/161179412-2dd927ee-02ba-475a-abe7-6fe3a76dace9.png)
* Source: https://custom-scripts.sentinel-hub.com/custom-scripts/sentinel-2/se2waq/
* Live example: [25th March 2022](https://apps.sentinel-hub.com/eo-browser/?zoom=11&lat=-37.96309&lng=147.56432&themeId=DEFAULT-THEME&visualizationUrl=https%3A%2F%2Fservices.sentinel-hub.com%2Fogc%2Fwms%2F42924c6c-257a-4d04-9b8e-36387513a99c&evalscript=dmFyIEZMQUdwYXJhbSA9IDE7CnZhciBGTEFHYmFja0dyb3VuZCA9IDI7Cgp2YXIgQmxhY2sgPSBbMF07ICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgLy8gRkxBR2JhY2tHcm91bmQgPSAwCnZhciBORFZJID0gaW5kZXgoQjA4LCBCMDQpOyAgICAgICAgICAgICAgICAgICAgICAgICAgICAvLyBGTEFHYmFja0dyb3VuZCA9IDEKdmFyIE5EV0kgPSBpbmRleChCMDMsIEIwOCk7CnZhciBUcnVlQ29sb3IgPSBbQjA0KjIuNSwgQjAzKjIuNSwgQjAyKjIuNV07ICAgICAgICAgICAvLyBGTEFHYmFja0dyb3VuZCA9IDIKdmFyIENobF9hID0gNC4yNiAqIE1hdGgucG93KEIwMy9CMDEsIDMuOTQpOyAgICAgICAgICAgIC8vIEZMQUdwYXJhbSA9IDA7IFMyLUwyQTsgWzFdIFVuaXQ6IG1nL20yOyAgICAgICAgCnZhciBDeWEgPSAxMTU1MzAuMzEgKiBNYXRoLnBvdyhCMDMgKiBCMDQgLyBCMDIsIDIuMzgpOyAvLyBGTEFHcGFyYW0gPSAxOyBTMi1MMkE7IFsxXSBVbml0OiAxMF4zIGNlbGwvbWw7IAp2YXIgVHVyYiA9IDguOTMgKiAoQjAzL0IwMSkgLSA2LjM5OyAgICAgICAgICAgICAgICAgICAgLy8gRkxBR3BhcmFtID0gMjsgUzItTDJBOyBbMV0gVW5pdDogTlRVOyAgICAgICAgICAKdmFyIENET00gPSA1MzcgKiBNYXRoLmV4cCgtMi45MypCMDMvQjA0KTsgICAgICAgICAgICAgIC8vIEZMQUdwYXJhbSA9IDM7IFMyLUwxQzsgWzJdIFVuaXQ6IG1nL2w7ICAgICAgICAgCnZhciBET0MgPSA0MzIgKiBNYXRoLmV4cCgtMi4yNCpCMDMvQjA0KTsgICAgICAgICAgICAgICAvLyBGTEFHcGFyYW0gPSA0OyBTMi1MMUM7IFsyXSBVbml0OiBtZy9sOyAgICAgICAgIAp2YXIgQ29sb3IgPSAyNTM2NiAqIE1hdGguZXhwKC00LjUzKkIwMy9CMDQpOyAgICAgICAgICAgLy8gRkxBR3BhcmFtID0gNTsgUzItTDFDOyBbMl0gVW5pdDogbWcuUHQvbDsgICAgICAKCnZhciBzY2FsZUNobF9hID0gWzAsIC40ICwgLjgsIDEuNiwgMy4yLCAxMF07CnZhciBzY2FsZUN5YSAgID0gWzAsIDEwLCAyMCwgNDAsIDUwLCAxMDAwXTsKdmFyIHNjYWxlVHVyYiAgPSBbMCwgNCwgOCwgMTIsIDE2LCAyMF07CnZhciBzY2FsZUNET00gID0gWzAsIDEsIDIsIDMsIDQsIDVdOwp2YXIgc2NhbGVET0MgICA9IFswLCA1LCAxMCwgMjAsIDMwLCA0MF07CnZhciBzY2FsZUNvbG9yID0gWzAsIDEwLCAyMCwgMzAsIDQwLCA1MF07Cgp2YXIgcyA9IDI1NTsKdmFyIGNvbG9yU2NhbGUgPSAKICBbCiAgIFs3My9zLCAxMTEvcywgMjQyL3NdLAogICBbMTMwL3MsIDIxMS9zLCA5NS9zXSwKICAgWzI1NC9zLCAyNTMvcywgNS9zXSwKICAgWzI1My9zLCAwL3MsIDQvc10sCiAgIFsxNDIvcywgMzIvcywgMzgvc10sCiAgIFsyMTcvcywgMTI0L3MsIDI0NS9zXQogIF07CgppZiAoTkRXSTwwKSB7CiAgaWYgKCBGTEFHYmFja0dyb3VuZCA9PSAwICkgewogICAgcmV0dXJuIEJsYWNrOwogIH0gZWxzZSBpZiAoIEZMQUdiYWNrR3JvdW5kID09IDEgKSB7CiAgICByZXR1cm4gWzAsIC41KihORFZJKzEpLCAwXTsKICB9IGVsc2UgaWYgKCBGTEFHYmFja0dyb3VuZCA9PSAyICkgewogICAgcmV0dXJuIFRydWVDb2xvcjsKICB9Cn0gZWxzZSB7CiAgc3dpdGNoICggRkxBR3BhcmFtICkgewogICAgY2FzZSAwOgogICAgIHJldHVybiBjb2xvckJsZW5kKENobF9hLCBzY2FsZUNobF9hLCBjb2xvclNjYWxlKTsKICAgICBicmVhazsKICAgIGNhc2UgMToKICAgICAgcmV0dXJuIGNvbG9yQmxlbmQoQ3lhLCBzY2FsZUN5YSwgY29sb3JTY2FsZSk7CiAgICAgIGJyZWFrOwogICAgY2FzZSAyOgogICAgICByZXR1cm4gY29sb3JCbGVuZChUdXJiLCBzY2FsZVR1cmIsIGNvbG9yU2NhbGUpOwogICAgICBicmVhazsKICAgIGNhc2UgMzoKICAgICAgcmV0dXJuIGNvbG9yQmxlbmQoQ0RPTSwgc2NhbGVDRE9NLCBjb2xvclNjYWxlKTsKICAgICAgYnJlYWs7CiAgICBjYXNlIDQ6CiAgICAgIHJldHVybiBjb2xvckJsZW5kKERPQywgc2NhbGVET0MsIGNvbG9yU2NhbGUpOwogICAgICBicmVhazsKICAgIGNhc2UgNToKICAgICAgcmV0dXJuIGNvbG9yQmxlbmQoQ29sb3IsIHNjYWxlQ29sb3IsIGNvbG9yU2NhbGUpOwogICAgICBicmVhazsKICAgIGRlZmF1bHQ6CiAgICAgIHJldHVybiBUcnVlQ29sb3I7CiAgfQp9Cg%3D%3D&datasetId=S2L1C&fromTime=2022-03-25T00%3A00%3A00.000Z&toTime=2022-03-25T23%3A59%3A59.999Z#custom-script)
* Note: set `var FLAGparam = 1` for Cyanobacteria or `var FLAGparam = 0` for Chlorophyll (also scale down the visuals to something like `var scaleChl_a = [0, .4 , .8, 1.6, 3.2, 10]`)

#### Other related scripts:
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

Licensing:
* Scripts are CC by attribution (check specifics), so give credit and provide source under same license for any modifications.
* Sentinel basic data access is free for non-commercial use, but double-check permissions. 
