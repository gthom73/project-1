# project-1 Team 3

# Team Members: 
Jon Thomas, Dawn Reyes, Mica Zier

# Background: 
Team 3 selected the topic of Healthcare and Technology, specifically looking at how Telehealth is helping to close the Healthcare Divide 

# Approach: 
Healthcare industry is undergoing a digital transformation, which will result in increased use of technology in patient care. Knowing Internet Access is a factor in Telehealth Adoption, team reviewed Internet Access rates versus current Telehealth usage in order to determine if patients were ready for the shift in care 

# Analysis: 
https://docs.google.com/presentation/d/1gKNeTSREXB53T6KMV5lfzUwxPE1AU3Yc41IM7w-VgB0/edit?usp=sharing

# Data Documentation: 

-Raw Data Sources:

-Medicare Telehealth Trends. "The Medicare Telehealth Trends dataset provides information about people with Medicare who used telehealth services between January 1, 2020 and March 31, 2023. The data were used to generate the Medicare Telehealth Trends Report." https://catalog.data.gov/dataset/medicare-telemedicine-snapshot

-FCC's Connect2Health Map, Broadband Data by state. "The Connect2HealthFCC Task Force’s platform Mapping Broadband Health in America 2023 allows users to visualize, intersect, and analyze broadband and health data at the national, state and county levels – informing policy and program prescriptions, future innovations, and investment decisions. This data visualization tool is especially timely given the recent COVID-19 national public health emergency, when telehealth became increasingly critical to meeting the needs of Americans, especially those residing in rural areas. This experience shifted the way in which many Americans access healthcare.". File name Connect2Health_2023_state.csv. Availalbe for download here: https://www.fcc.gov/reports-research/maps/connect2health/map.html#ll=31.5,-96.4&z=4&t=broadband&hmt=opioid&bbm=fixed_access&dmf=none&ino=none&zlt=county

# To generate clean data file for Analysis: 
Run file github.com/gthom73/project-1/Mica/Data for Analysis.ipynb

# To generate data for "Telehealth" analsysis
Run file:  github.com/gthom73/project-1/dawn1/Dawn's file.ipynb

# To generate data for "Internet Access" analysis:
Run file: "project1Group3.ipynb"
  To successfully load the project1Group3.ipynb file you will need to import into your jupyter project the following dependencies.
  
        import pandas as pd
        from pathlib import Path
        import matplotlib.pyplot as plt
        import numpy as np
        #import contextily as ctx
        import geopandas as gpd
        import os
        import seaborn as sns
        
  It is also suggested to mute warnings due to head file issues.
  
        import warnings
        warnings.filterwarnings('ignore')

Data source files are located at the following addresses and provide the necessary information for all graphs and tables.

-File to Load (Remember to Change These as Necessary)
hospital_data_to_load = Path("../data_folder/analysis_data.csv")
states = gpd.read_file("../data_folder/data/usa-states-census-2014.shp")

-Load Project Data Into Jupyter
analysis_data = pd.read_csv(hospital_data_to_load)

-Read shapefile using geopandas
states = states.to_crs("EPSG:3395")

# To generate data for "Correleations" analysis:
Run file: github.com/gthom73/project-1/Mica/Correlations.ipynb
