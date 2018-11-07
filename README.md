# Atmoshack2018
Join EUMETSAT, ECMWF, FMI and University of Helsinki scientists for a weekend hackathon working with atmospheric data at the Finnish Meteorological Service in Helsinki on 16-18 November 2018. 

This Github repository contains the resources for Copernicus Hackathon 2018 in Helsinki, it can be used to share code. More info at

https://ultrahack.org/atmoshack2018 

https://www.eumetsat.int/website/home/News/ConferencesandEvents/DAT_4070861.html?lang=EN

![EventBanner](https://github.com/WEkEO/AtmosHack2018/blob/master/01-images/Atmoshack2018-banner.jpg)

 # Table of contents
1. [Challenge](#challenge)
2. [Dataset offering](#datasets)  
3. [Platform offering](#platform)
4. [Solution Domains](#solution)
5. [Background](#bg)
6. [Data Access](#data)
7. [Useful Links](#useful)

# Challenge: Hack the Atmosphere! <a name="challenge"></a>
Urban air pollution poses a significant threat to human health and the quality of life of millions of people worldwide. Nine out of ten people are estimated to breathe air containing high levels of pollutants, causing around 7 million deaths every year. More than 90% of air pollution-related deaths occur in the developing world. Many of these areas have no surface air-quality monitoring networks and rely mainly on modelling and satellite information. Besides air pollution, there are other aspects of atmospheric composition that can affect health: UV radiation, which strongly depends on the stratospheric ozone layer, is another example.
Urban air pollution poses a significant threat to human health and the quality of life of millions of people worldwide. Nine out of ten people are estimated to breathe air containing high levels of pollutants, causing around 7 million deaths every year. More than 90% of air pollution-related deaths occur in the developing world. Many of these areas have no surface air-quality monitoring networks and rely mainly on modelling and satellite information. 

Your challenge is to create solutions that help people in their daily lives to reduce their exposure to pollutants and UV radiation. To solve this challenge, you are encouraged to use Copernicus atmospheric monitoring data.

Various approaches are welcome: Create new solutions or add atmosphere-smart features to existing solutions. Propose innovative data visualisations for academic purposes or for raising awareness around the atmospheric environment. Mobile, web apps, platforms or hardware - it’s your call how to improve the quality of life for many!

### Dataset offering <a name="datasets"></a>
An overview of the complete set of datasets available for this event is listed below

|  Product | Source | Used for   | Geo Coverage  | Time Coverage   |  Resolution |  Format | HTTP Access  |
| ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ |
|PMAP Aerosol Optical Depth - particles in the atmosphere | Metop | Air pollution (basis for PM10, PM2.5 etc) | Global | April 2016 - onwards.  Aim 2017 onwards. (14 per day). January 2017 until December 2017 | 5x40km and 10x40km | NetCDF | [GOME-PMAP](http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=01-GOME_PMAP)|
|NO2, Aerosols Index | Metop GOME-2 and IASI | Air pollution monitoring, volcanic eruptions, forest fires | Global | 2016 onwards | 40x80km | NetCDF/ HDF5 | [Aerosols-Index](http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=07-Aerosols_Index/) |
| NO2, CO, O3 |	Sentinel-5p Tropomi	| Air pollution monitoring | Global	| July 2018 onwards | 5x5km and 7x5km | NetCDF |  [Sentinel-5P](http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=03-Sentinel_5p-Tropomi/) |
|UV index (corrected for clouds with ECMWF data) | Metop (AC SAF) | UV - risk of harm | Global | June 2007 until May 2017 | 250 x 250 | PNG/HDF5 | [UV-Index](http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=02-UV_Index-AC_SAF/)|
|Dust RGB |	Meteosat Second Generation (geo orbit) | Dust storms - health and transport problems |Atlantic and Indian Ocean	| Available from 28th September 2018 | 4km | GeoTiff/ PNG | [Dust-RGB](http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=04-Meteosat-Dust_RGB) |
|Ash RGB | Meteosat Second Generation (geo orbit) |	Volcanic ash - aviation, health etc. | Atlantic and Indian Ocean | Available from 28th September 2018 | 4km | GeoTiff/ PNG | [Ash-RGB](http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=05-Meteosat-Ash_RGB)|
| SmartSMEAR Aerosols, gases, meteo, fluxes, soil,... | SMEAR |	Research | Finland |	1996 onwards depending on station and measured parameter | Point observations, no geospatial data | txt/csv, hdf5 | <a href="https://avaa.tdata.fi/web/smart/smear/api" target="_blank">SmartSMEAR</a>|
|Regional forecasts/ analyses of PM, O3, NO2, SO2 | CAMS | European air pollution | Europe | 2018 | Point data (as used in Euronews air quality forecasts), gridded data @ ~10km	| CSV , NetCDF (gridded data) | [Air-Pollution](http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=06-CAMS-AirPollution)|
|Global total ozone column | CAMS |	Total ozone columns | Global | 2003-present. Reanalysis from 2003 until 2016 | ~40km | NetCDF, GRIB |[CAMS Reanalysis data](https://confluence.ecmwf.int/display/CKB/How+to+download+the+CAMS+Reanalysis+data+via+the+ECMWF+Web+API)|
|Global ozone (Metop GOME-2 instrument)| EUMETSAT/DLR |	ozone (O3), nitrogen dioxide (NO2), sulphur dioxide (SO2) | Global | Daily | - | WMS |[Latest](https://geoservice.dlr.de/web/maps/metop:gome2.tc.latest), [Daily](https://geoservice.dlr.de/web/maps/metop:gome2.tc.daily)|
|Global UV forecasts | CAMS | UV index | Global | 2003-present. NRT from 2016 June onwards, Reanalysis from 2003 to 2016 |~40km	| NetCDF | [CAMS](https://atmosphere.copernicus.eu/) |
|Global fire emissions | CAMS |	Wildland fire emission estimates | Global |	2003-present | ~10km | NetCDF | [CAMS](https://atmosphere.copernicus.eu/) |

### Platform offering <a name="platform"></a>
WEkEO platform [wekeo.eu](https://www.wekeo.eu/) provides access to Copernicus datasets and cloud based processing resources. Get to know the capabilities of WEkEO from [here](https://www.wekeo.eu)

You will be offered VM access by participating on the AtmosHack2018 [here](https://www.wekeo.eu/advanced_user)

### Solution domains <a name="solution"></a>
* Air-quality apps
* Traffic and navigation
* Geological: volcanic eruptions, dust and smoke in the atmosphere
* Cleantech for industries, factories and agriculture
* Smart city solutions

### Background <a name="bg"></a>
Copernicus AtmosHack is funded by the EU’s [Copernicus Programme](http://www.copernicus.eu/) and has been organised through a partnership of [EUMETSAT](https://www.eumetsat.int/website/home/index.html), the [Copernicus Atmosphere Monitoring Service (CAMS)](https://atmosphere.copernicus.eu/), the [Finnish Meteorological Service (FMI)](https://en.ilmatieteenlaitos.fi/), and the [University of Helsinki](https://www.inar.helsinki.fi/).

### Data Access <a name="data"></a>

**Object Storage**
End Point http://atmoshack.obs.eu-de.otc.t-systems.com/ 

**list** all product, for example, of CAMS Air Pollution

```sh 
curl http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=06-CAMS-AirPollution
```

**download** a file

```sh 
curl -O atmoshack.obs.eu-de.otc.t-systems.com/01-GOME_PMAP/M01-GOME/2017/01/M01-GOME-GOMPMA02-NA-2.0-201701003859.000000000Z-20170101022528-1293482-1.nc
```

Alternatively the data can be accessed with commonly used Object Storage tools, using the access keys below (AK/SK):

S3cmd https://s3tools.org/s3cmd  
S3FS https://linux.die.net/man/1/s3fs
  
|  User Name | Access Key Id | Secret Access Key   | 
| ------------ | ------------ | ------------ |
| AtmosHack2018 | IXUCNIYQK5IXQ80TGTSA | SurkPQ2Z2xrBWxe9nye2Wfbyd3UVZ2ebVntT8ViN | 

**CAMS Data Access** 

Access CAMS data via the ECMWF MARS archive - Web-API

Retrieve ECMWF key

• Self-register at http://apps.ecmwf.int/registration

• Login at https://apps.ecmwf.int/auth/login

• Retrieve your API key at https://api.ecmwf.int/v1/key/

• Specify the ECMWFDataServer with your url, key and email information

Install the ecmwfapi python library
```sh 
pip install https://software.ecmwf.int/wiki/download/attachments/56664858/ecmwf-api-client-python.tgz
```
If you cannot run the pip commands, just download the ecmwf-api-client-python.tgz library. Extract its content and copy the module ecmwfapi to a directory pointed by the environment variable PYTHONPATH

Execute a MARS request and download data either as GRIB or netCDF

NOTE: per default, ECMWF data are on a gaussian grid with longitudes going from 0 to 360 degrees. It can be reprojected to a regular geographic latitude-longitude grid. If a reprojection is wished, the key 'grid' with the respective latitude and longitude resolution has to be specified. The same applies for specifying a longitude range of -180 to 180. The key area can be set.


```sh 
#!/usr/bin/env python 

from ecmwfapi import ECMWFDataServer

server = ECMWFDataServer(url="https://api.ecmwf.int/v1", key="...", email="...@...")

server.retrieve({
       'stream': "oper",
       'levtype': "sfc",
       'param': "167",
       'dataset': "interim",
       'step': "0",
       'grid': "0.5/0.5",
       'area': "90/-180/-90/179.5",
       'time': "00/06/12/18",
       'date': "2014-07-01/to/2014-07-31",
       'type': "an",
       'class': "ei",
       'format': "netcdf",
       'target': "test.nc"
        })
   ```

### Useful Links <a name="useful"></a>

[How to Visualize NetCDF data - YouTube Video](https://www.youtube.com/watch?v=XqoetylQAIY)

CAMS: https://atmosphere.copernicus.eu/

Example notebook: https://gist.github.com/erget/467dba7082d31d73b20f3b5e90e740af

GDAL: http://www.gdal.org/

Jupyter: https://jupyter.org/

Scipy stack, including matplotlib and numpy: https://www.scipy.org/

Info on netCDF tool: https://www.unidata.ucar.edu/software/netcdf/

QGIS: https://www.qgis.org/en/site/

Xarray: http://xarray.pydata.org/en/stable/

Scitools: https://scitools.org.uk/
