# Predicting Foreclosures in Los Angeles
A datascience project to predict housing foreclosure in Los Angeles.  To get started
simply clone the repository.  

Each folder contains Python Notebook files or CSV that were used in our project.  Descriptions of each folder and its function is described below.  Funcitonality of each folder was seperated so that source CSV files are only read from the /source directory and after normalization is performed the resulting files are stored in the /dataset directory.  This organization was used to allow a modular approach while retaining separation of functions.

## Explanation of Filetree:
The workflow can be understood as follows:
### source -> util -> dataset -> application -> plots
 - /source : Original CSV files are stored here
 - /util : Notebook files to normalize data 
 - /dataset : all normalized datastore here
 - /application : reads data form /dataset and preforms predictions
 - /plots : Any images generated are held in /plots

### /application
This folder contains all the final prediction models, imported CSV files are read from the /dataset directory.  File names describe which algorithms are used and any features that were created in that Notebook.
  - Linear Regression
  - Decision Tree Regresion
  - Random Forest Regresion

### /dataset
The dataset directory contains all normalized feature and label data in the form of CSV files.  The file names are same as their counter parts in the source directory for continuity. With the exception of FORECLOSURES.CSV and 1-CombinedDataset.csv.

### /plots
The Notebook files in our application folder generate images using MatPlotLib. Files in this folder follow the naming of the Notebook file that generated them.
![Linear Regression using Periodic time](https://github.com/Shramster/CS4661-Project/blob/main/plots/LinearRegression_Multiple_runs_with_isJan_periodic.png?raw=true)

### /source
This directory contains unaltered CSV files that we gathered during our research. The README.md file contains a listing of the filename, description of the data and where it was found.

### /util
The util folder contains Notebook files used to normalize CSV files from the source folder, including both feature and label data.  File naming is based on the file CSV file in source that it is normalizing and the output file is saved to the dataset directory.
  - LA Foreclosures 2014 - 2022:
  - 30 Year Mortgage Rates
  - Zillow Home Value Index
  - Consumer Pricing Index
  - etc


