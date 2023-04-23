This document is for NAS_Ramp_Logit_Reg

This script is designed to test the correlation between the occurence of a non-indigenous aquatic species and the number of public accesses on a waterbody. This workflow and associated scripts have been designed to be flexible such that the user can easilly replace the example data provided with their own waterbody and public access shapefiles. The example data here can be used to test the correlation between zebra mussel occurence and the number of waterbody access site per lake in MN.

## Dependencies
You will need the following software and packages:

* anaconda (https://conda.io/projects/conda/en/stable/user-guide/install/download.html)
* python 3
* pandas
* geopandas
* numpy
* json-e
* requests
* functools
---

  
## Conda Setup

Open the Anaconda Powershell via your start menu

It is recommended that you set up a conda environment prior to using this package.

% conda create -n <NAME> python=3 
	
% conda activate <NAME>
---

## Install required packages
% conda install -c anaconda python
% conda install -c anaconda pandas
% conda install -c anaconda geopandas
% conda install -c anaconda numpy
% conda install-c conda-forge json-e
% conda install-c requests
% conda install-c functools
% pip install notebook
---


## Workflow
Download Notebooks and store in your project folder.

*NAS_data_pull.ipynb
*Access_NAS_logit_regression.ipynb

Download Shapefiles from repository and store in a subfolder called data within folder containing the notebooks you downloaded.

*MN_accesses.shp 
*MN_Lakes.shp (https://prd-tnm.s3.amazonaws.com/StagedProducts/Hydrography/NHD/State/Shape/NHD_H_Minnesota_State_Shape.zip)

***Alternatively***
Visit https://apps.nationalmap.gov/downloader/#/ to download a waterbody shapefile for your area of interest
Note: You will also need a shapefile containing georeferenced points for publis accesses for your region of interest. These can be found online usually by searching for "<state name> public water access shapefile". Be advised using your own data may require modifying filenames and attribute column names to match your data.
---

Open model script notebook from Conda by runnning:

% python -m notebook

Navigate to the directory with the model script and open the NAS_data_pull notebook.

Run the NAS_data_pull notebook and export the final shapefile to your local directory.

***Alternatively***
Visit https://nas.er.usgs.gov/api/v2/species to get your taxa species key information

---
Check Yourself:
* At this point you should have:
	a conda environment with all packages installed
  	2 ipynb notebooks stored in a unique folder
	3 shapefiles stored in a data subfolder within your unique project directory.
---

Run the model

*Open the Access_NAS_logit_regression notebook
*If you renamed the shapefiles or are using your own, modify the path names in the notbook to match.
*Now run the cells in order to get a regression plot.
*You can now us the fitted model to predict probability of the presence of your invasive based on the number of public access sites for a waterbody. 
