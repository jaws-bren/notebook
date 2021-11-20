# JAWS | BREN
## Mapping habitat suitability for the identification and conservation of the Guadalupe Mountain necklacepod (Sophora gypsophila)

**Student Authors:**<br>
**J**ulia Parish<br>
**A**lex Vand<br>
**W**ylie Hampson<br>
**S**hale Hunter<br>

## Project Details

This notebook was created to provide an introduction to using satellite data from the USGS Landsat 8 Level 2, Collection 2, Tier 1 sourced from Google Earth Engine for analysis to identify soil composition.

Landsat 8 is a joint effort between USGS and NASA, with data collected from 2013-04-11 to the present. This particular dataset is the atmospherically corrected surface reflectance and land surface temperature from the Landsat 8 OLI/TIRS sensors.

This project used the Google Earth Engine API to download Landsat 8 data in order to explore potential habitat for an endangered plant species. By comparing NDVI and OIF bands, this study was able to determine possible regions of high gypsum concentration in the Guadalupe Mountains.

**Landsat 8 Bands**
* SR_B1: Band 1 (ultra blue, coastal aerosol) surface reflectance
* SR_B2: Band 2 (blue) surface reflectance
* SR_B3: Band 3 (green) surface reflectance
* SR_B4: Band 4 (red) surface reflectance
* SR_B5: Band 5 (near infrared) surface reflectance
* SR_B6: Band 6 (shortwave infrared 1) surface reflectance
* SR_B7: Band 7 (shortwave infrared 2) surface reflectance
* ST_B10: Band 10 surface temperature. 

**Selected Metadata Definitions**

* 'CLOUD_COVER': Percentage cloud cover (0-100), -1 = not calculated.<br>
* 'CLOUD_COVER_LAND': Percentage cloud cover over land (0-100), -1 = not calculated.<br>
* 'DATA_SOURCE_ELEVATION': Elevation data source.<br>
* 'DATA_SOURCE_WATER_VAPOR': Water vapor data source.<br>
* 'EARTH_SUN_DISTANCE': Earth-Sun distance (AU) One astronomical unit (AU) is about 93 million miles (150 million kilometers).<br>
* 'IMAGE_QUALITY_OLI': Image quality of the OLI bands. 1 = worst, 9 = best, 0 = quality not calculated. For Landsat 8, this parameter is adjusted downward for scenes collected using the lower 12 bits from the OLI sensor (TRUNCATION_OLI = "LOWER").<br>
* 'IMAGE_QUALITY_TIRS': Image quality of the TIRS bands. 1 = worst, 9 = best, 0 = quality not calculated. It is also adjusted downward for scenes processed with "SWITCHED" for the TIRS_SSM_POSITION_STATUS value.<br>
* 'SENSOR_ID': Name of the sensor.<br>
* 'SPACECRAFT_ID': Name of the spacecraft.<br>
* 'SUN_ELEVATION': Sun elevation angle in degrees for the image center location at the image center acquisition time. A positive value indicates a daytime scene. A negative value indicates a nighttime scene. Note: For reflectance calculation, the sun zenith angle is needed, which is 90 - sun elevation angle.<br>
* 'SUN_AZIMUTH': Sun azimuth angle in degrees for the image center location at the image center acquisition time. A positive value indicates angles to the east or clockwise from the north. A negative value indicates angles to the west or counterclockwise from the north.<br>
* 'WRS_PATH': The Worldwide Reference System (WRS) is a global notation system for Landsat data. It is used to identify the path and row of each Landsat image. The path is the descending orbit of the satellite. Each path is segmented into 119 rows, from north to south.<br>

## Installation

### Packages
* `ee`
* `geemap`
* `pandas`
* `matplotlib.pyplot`
* `numpy`

### Binder Environment

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/jaws-bren/notebook/main)

## Usage

Identifying Gypsic Soils
Mapping habitat suitability for the identification and conservation of the Guadalupe Mountain necklacepod (Sophora gypsophila)

*Sophora gypsophila* is a G1 Critically Endangered shrub in the pea family endemic to a small area surrounding the Guadalupe mountains in Southeastern New Mexico and Western Texas. Part of what puts *S. gypsophila* at risk is the fact that it is a substrate obligate - in other words, it can only survive in a specific soil type. But this also gives us an advantage: it means that we can identify potentially suitable habitat simply by mapping the gypsic areas in the vicinity of existing populations of *S. gypsophila* and subsetting these areas by the plant's known elevation range. This can be done using Landsat bands 1, 5, and 7, taking advantage of the fact that gypsic soils are highly reflective in band 5 () but particularly nonreflective in band 7 ().

## References

Binte Mostafiz, R.; Noguchi, R.; Ahamed, T. Agricultural Land Suitability Assessment Using Satellite Remote Sensing-Derived Soil-Vegetation Indices. Land 2021, 10, 223. https://doi.org/10.3390/land10020223

Boettinger, J., Ramsey, R., Bodily, J., Cole, N., Kienast-brown, S., Nield, S., Saunders, A., & Stum, A. (2008). Landsat Spectral Data for Digital Soil Mapping. Digital Soil Mapping with Limited Data. https://doi.org/10.1007/978-1-4020-8592-5_16

Browning, D. M., & Duniway, M. C. (2011). Digital Soil Mapping in the Absence of Field Training Data: A Case Study Using Terrain Attributes and Semiautomated Soil Signature Derivation to Distinguish Ecological Potential. Applied and Environmental Soil Science, 2011, e421904. https://doi.org/10.1155/2011/421904

Landsat 8 data courtesy of the U.S. Geological Survey. https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C02_T1_L2#image-properties

Nield, S. J., Boettinger, J. L., & Ramsey, R. D. (2007). Digitally Mapping Gypsic and Natric Soil Areas Using Landsat ETM Data. Soil Science Society of America Journal, 71(1), 245–252. https://doi.org/10.2136/sssaj2006-0049

Ridwan, M. A., Radzi, N., Ahmad, W., Mustafa, I., Din, N., Jalil, Y., Isa, A., Othman A., Zaki, W. Applications of Landsat-8 Data: Survey. Internation Journal of Engineering & Techonology 2018, 11, 436-441. DOI:10.14419/ijet.v7i4.35.22858

Sophora gypsophila | NatureServe Explorer. (n.d.). Retrieved November 16, 2021, from https://explorer.natureserve.org/Taxon/ELEMENT_GLOBAL.2.155365/Sophora_gypsophila

Soil Survey Manual - Ch. 5. Digital Soil Mapping | NRCS Soils. (n.d.). Retrieved November 16, 2021, from https://www.nrcs.usda.gov/wps/portal/nrcs/detail/soils/ref/?cid=nrcs142p2_054255

Stafford, K., Rosales Lagarde, L., & Boston, P. (2008). Castile evaporite karst potential map of the Gypsum Plain, Eddy County New Mexico and Culberson County, Texas: A GIS methodological comparison. J Cave Karst Stud, 70.

Texas Native Plants Database. (n.d.). Retrieved November 16, 2021, from https://aggie-horticulture.tamu.edu/ornamentals/nativeshrubs/sophoragypsophila.htm

Vermote, E., Justice, C., Claverie, M., & Franch, B. (2016). Preliminary analysis of the performance of the Landsat 8/OLI land surface reflectance product. Remote Sensing of Environment, 185, 46-56.
