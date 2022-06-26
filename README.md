# USGS_LIDAR_AgriTech

**Contents**

- [USGS-Lidar-custom-package](#USGS-Lidar-custom-package)
  - [Introduction](#introduction)
  - [Discription](#discription)
  - [Approach](#approach)
  - [Project Structure](#project-structure)
    - [assets](#assets)
    - [notebooks](#notebooks)
    - [scripts](#scripts)
    - [tests](#tests)
    - [logs](#log)
    - [root folder](#root-folder)
  - [Dependancies](#Dependancies)

## Introduction

Agricultural technology or agrotechnology (abbreviated agtech, agritech, AgriTech, or agrotech) is the use of technology in agriculture, horticulture, and aquaculture with the aim of improving yield, efficiency, and profitability. Agricultural technologies are developed to increase production, resolve chemo-physical, biological, and socioeconomic constraints related to crop production systems. Today’s agriculture routinely uses sophisticated technologies such as robots, temperature and moisture sensors, aerial images, and GPS technology. These advanced devices and precision agriculture and robotic systems allow businesses to be more profitable, efficient, safer, and more environmentally friendly. Thus, Agritech is demanded by many counties to boost the economy gained from agriculture.

## Discription
In this study fetching, visualizing and transforming has been performed on USGS data. Open source python packages is used to design python module that domain experts and data scientists can use to fetch, visualise, and transform publicly available satellite and LIDAR data. The developed python module interface with USGS 3DEP and fetch data using their API. 

## Approach
The project is divided and implemented by the following phases
- Fetching point cloud data of all available year of given a boundary polygon in any coordinate reference system (CRS)
- Graphically displaingy returned elevation files as a 3D render plot.
- Sub-sampling point cloud data based on given resolution.

## Project Structure
The repository has a number of files including python scripts, jupyter notebooks, and text files. Here is their structure with a brief explanation.

### assets:
- `get_data.json`: a json template used for fetching data using pdal
- `usgs_3dep_metadata.csv`: a csv file scrapped from [usgs.entwine.io](https://usgs.entwine.io/) containing data about regions and their boundary points along with the year it is collected

### notebooks:
- `example.ipynb`: a jupyter notebook showing how to fetch data
- 

### scripts:
- `app_logger.py`: a python script for logging
- `file_handler.py`: a python script for handling reading and writing of csv, pickle and other files
- `lidar_processor.py`: the main python script of this project that does the fetching, displaying and sub-sampling

### tests:
- the folder containing unit tests for components in the scripts

### logs:
- the folder containing log files (if it doesn't exist it will be created once logging starts)

### root folder
- `requirements.txt`: a text file lsiting the projet's dependancies
- `setup.py`: a configuration file for installing the scripts as a package
- `README.md`: Markdown text with a brief explanation of the project and the repository structure.

## Dependancies
This package is dependent on the following python packages.
* PDAL
* Shapely
* Geopandas
* Matplotlib
