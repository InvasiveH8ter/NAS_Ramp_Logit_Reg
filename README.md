## This document is for NAS_Ramp_Logit_Reg

This script is designed to test the correlation between the occurence of a non-indigenous aquatic species and the number of public accesses on a waterbody. This workflow and associated scripts have been designed to be flexible such that the user can easilly replace the example data provided with their own waterbody and public access shapefiles. The example data here can be used to test the correlation between zebra mussel occurence and the number of waterbody access site per lake in MN.

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
	
pip install python
	
pip install pandas
	
pip install geopandas
	
pip install numpy
	
pip install json-e
	
pip install requests
	
pip install functools

pip install matplotlib

pip install statsmodels

pip install seaborn

pip install scikit-learn
	
pip install notebook


## Workflow
Create a project folder.

Download NAS_Access_Reg.zip and extract to your project folder

## Check Yourself:
	
At this point you should have:
	

* 2 ipynb notebook stored in a unique folder
* The MN_accesses.shp stored in a data subfolder 

## Open Jupyter notebook from OSGeo4W by runnning:

python -m notebook

## Run the model

* Open the Access_NAS_logit_regression notebook.
* Note: If you renamed the shapefiles or are using your own, modify the path names in the notebook to match.
* Now run the cells in order to get a regression plot.
* You can now us the fitted model to predict probability of the presence of your invasive based on the number of public access sites for a waterbody. 

***Alternatively***
To download a waterbody shapefile for your area of interest, visit https://apps.nationalmap.gov/downloader/#/. 

You will also need a shapefile containing georeferenced points for public accesses for your region of interest. These can be found online usually by searching for "state name public water access shapefile". Be advised using your own data may require modifying filenames and attribute column names to match your data.

You can also change the species key information to investigate the correlation between public accesses and your most hated non-indigenous aquatic species.

Visit https://nas.er.usgs.gov/api/v2/species to get your taxa species key information.
