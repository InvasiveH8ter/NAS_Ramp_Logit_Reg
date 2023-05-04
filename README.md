## This document is for NAS_Ramp_Logit_Reg

This script is designed to test the correlation between the occurence of a non-indigenous aquatic species and the number of public accesses on a waterbody. This workflow and associated scripts have been designed to be flexible such that the user can easilly replace the example data provided with their own waterbody and public access shapefiles. The example data here can be used to test the correlation between zebra mussel occurence and the number of waterbody access sites per lake in MN (for lakes greater than 0.50 km squared and with at least one public access).

## Dependencies
You will need the following software and packages:

* OSGeo4W
* python 3
* pandas
* geopandas
* numpy
* json-e
* requests
* functools
* matplotlib
* seaborn

## Install required packages

Open OSGeo4W from start menu

Navigate to your user directory by running:

cd C:\Users\YourInfo

Install required packages by running:
	
pip install python pandas geopandas numpy json-e requests functools matplotlib statsmodels seaborn scikit-learn notebook


## Workflow
Create a project folder within your home directory.

Download repository as zipfile and extract to your project folder

Download MN_lakes_shapefiles and Extract into Data Subdirectory (Leave this in the shape folder it comes packed in)

https://prd-tnm.s3.amazonaws.com/StagedProducts/Hydrography/NHD/State/Shape/NHD_H_Minnesota_State_Shape.zip

## Check Yourself:
	
At this point you should have:

* 2 ipynb notebook stored in your project folder
* The MN_accesses.shp stored in the data subfolder
* The NHDWaterbody.shp stored within a folder named shape within the data subfolder

## Open Jupyter notebook from OSGeo4W by runnning:

python -m notebook

Navigate to the directory where you stored your downloaded files

## Run the model

* Open the Access_NAS_logit_regression notebook.
* Note: If you renamed the shapefiles or are using your own, modify the path names in the notebook to match.
* Now run the cells in order to get a regression plot.
* You can now use the fitted model to predict probability of the presence of your invasive based on the number of public access sites for a waterbody. 

***Alternatively***
To download a waterbody shapefile for your area of interest, visit https://apps.nationalmap.gov/downloader/#/. 

You will also need a shapefile containing georeferenced points for public accesses for your region of interest. These can be found online usually by searching for "state name public water access shapefile". Be advised using your own data may require modifying filenames and attribute column names to match your data.

You can also change the species key information to investigate the correlation between public accesses and your most hated non-indigenous aquatic species by getting the species ID at:

https://nas.er.usgs.gov/api/v2/species to get your taxa species key information.
