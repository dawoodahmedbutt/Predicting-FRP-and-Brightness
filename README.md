# Predicting-FRP-and-Brightness
Predicting Fire Radiative Power and Brightness using Regression

Multiple files have been uploaded to this repository. This is so that my analysis could be kept as clean as possible. 

Below is an explanation of the individual files. 
1. NASA Fire Data Cleaning - uploading the fire data, cleaning and filtering for desired bounds
2. era5 Weather Processing - uploading the weather data as a grib file, and extracting as a CSV
3. ERA5 Fire Matching - using IDW, mathcing the weather data to each of the fire events. Multiple combinations of Number of Neighbours and Power were run manually, and then uploaded in order to compare performance
4. SRTM Terrain Data Extraction - Extracting terrain data from a tif file into CSV. Due to the large file and computing limitations, the file had to be split into 25 small chunks in order to extract the relevant data.
5. Fire Weather Terrain Matching - using IDW to match the terrain data with each of the fire events. Again, due to large file sizes, this process had to be completed in batches.
   - Filter the fire weather data for the coordinates in the extracted terrain file
   - Perform IDW
   - Save as a CSV
   - Repeat
   - Concatenate
6. Data Vis - graphs, charts and visualisations to present my data
7. Machine Learning - After cleaning the data (such as removing redundant columns), a ML algorithm was trained on my dataset. Multiple ML algorithms were tested out, along with tuned versions. The best performing model was XGBoost Tuned v1.
                      Performance comparison can be seen in the attached slides


Due to GitHub file upload limitations, the model could not be uploaded to this repository, however the appropriate steps have been captured in this notebook. 
Similarly, the app could not be deployed in Streamlit as of yet. This is a work in progress. 

