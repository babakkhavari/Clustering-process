[![DOI](https://zenodo.org/badge/197186462.svg)](https://zenodo.org/badge/latestdoi/197186462)

# PopCluster

PopCluster is a QGIS plugin that uses raster population layers to generate vector based (polygon) population settlements or else "population clustes". The result clusters are attributed with the following information:

1. **id** - a unique identifier for each cluster
2. **Country** - the name of the country/study area 
3. **Population** - population in defined year (based on HRSL published date)
4. **Area** - the area of each cluster (in sq.km)
5. **Nightlights** - the maximum value of nighttime light detected in each cluster (0-64)
6. **ElecPop** - the number of people living in areas with detected nighttime light

### How-to-use Instructions 

#### Versions
As of July 2019 there are three different versions of the plugin available. 

 * **Version 1.** Plugin developed for QGIS 3.2 and works with the [High Resolution Settlement Layer](https://data.humdata.org/organization/facebook?sort=metadata_modifieddesc&page=1&q=&ext_page_size=25#dataset-filter-start)
 * **Version 2.** Plugin developed for QGIS 3.4 (the latest stable version) and works with the [High Resolution Settlement Layer](https://data.humdata.org/organization/facebook?sort=metadata_modifieddesc&page=1&q=&ext_page_size=25#dataset-filter-start)
 * **Version 3.** Plugin developed for QGIS 3.2 and works with the [Global Human Settlement Layer](https://ghsl.jrc.ec.europa.eu/))

Please select one of the above to proceed.  

#### How to install

**Note:** Istallation instructions are also available as a downloadable document [here](Instructions/Installation%20of%20plugin.docx)

1.	Download the zipped plugin folder onto your computer.
2.	Open QGIS Desktop make sure that you use version 3.2 or 3.4 (this depends on which version of the plugin that you have downloaded). 
3.	On top of the window you have a number of menus, click on the one that reads Plugins.

	![image1](assets/installation/img/image1.jpg)

4.	Next, go to Manage and Install Plugins…

	![image2](assets/installation/img/image2.jpg)


5.	This will open a new window with a number of different options on the left-hand side. Choose Install from ZIP
 	
	![image3](assets/installation/img/image3.jpg)


6.	In the window that opens click on the three dots next to the empty field to navigate to where you saved the zipped plugin folder.
	
	![image4](assets/installation/img/image4.jpg)

7.	When you have found it, select it and click **Install plugin**
 	
	![image5](assets/installation/img/image5.jpg)

8.	After the plugin has been installed will appear under the Plugins menu on top of the screen. You are now ready to run the plugin.
	
	![image6](assets/installation/img/image6.jpg)

9.	When the plugin is installed it appear under the Plugin menu with the name HRSL Clustering.
	
	![image7](assets/installation/img/image7.jpg)
	
#### Additional resources needed in order to run the plugins
In order to run the clustering plugins three datasets are needed. 

**1**.  A population dataset. The population dataset has to be in the form of a raster. This raster will set the base of 	the clusters. It is recommended that you use the High Resolution Settlement Layer (available [here](https://data.humdata.org/organization/facebook)). If you area of interest is not available in High Resolution Settlement Layer database use the Global Human Settlement Layer instead (available [here](https://ghsl.jrc.ec.europa.eu/))

**2.**  Administrative boundaries. To run the plugin administrative boundaries are needed. These administrative boundaries will be used to clip your other datasets to the area of interest. They will also be used in order to limit the maximum area of the clusters and therefore it is highly recommended that you choose administrative boundaries that are disaggregated beyond the national borders. Administrative boundaries can be found e.g. [here](https://gadm.org/).

**3.** Nighttime lights. The nighttime lights map show anthropogenic light sources and will be used in order to determine the population living in areas with light emitting infrastructures present. The nighttime lights used are avialable [here](https://eogdata.mines.edu/download_dnb_composites.html). It is recommended that you use the cleaned data with outliers removed. These data are only available on a yearly basis and as of July 2019 the latest version is from 2016.
 
#### How to run the plugins

Detailed instructions for how to run the plugin is available [here](Instructions/How%20to%20run%20the%20clustering%20plugin.docx)


### Cautions

* Make sure that the QGIS version available for your needs is installed on your machine. If you are using the High Resolution Settlement Layer use QGIS 3.4 or QGIS 3.2. If you are using the Global Human Settlement Layer use QGIS 3.2. QGIS 3.4 can be downloaded [here](https://qgis.org/en/site/forusers/download.html) and QGIS 3.2 can be dowloaded [here](http://download.osgeo.org/qgis/)

* As of July 2019 the nighttime light map is mandatory to run the plugin. This will be updated in future versions of the plugin in which the use of nighttime lights will be optional.

### Supplementary material

* An academic publication supporting the methodology is available [here](https://www.mdpi.com/1996-1073/12/7/1395)

* An example is available [here](Equatorial%20Guinea%20example%20case).

* Any questions or bug reports can be submitted here or on in the [OnSSET forum](https://groups.google.com/forum/m/#!forum/onsset)

* For any additional information please contact the KTH team [here](http://www.onsset.org/contact--forum.html)
