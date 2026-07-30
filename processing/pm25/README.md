# PM<sub>2.5</sub> - Annual mean PM<sub>2.5</sub>

## Data inputs
To bias correct the SHERPA data(??), you will need to have available the following data:

- For GBD 2023: [IHME (2026](https://doi.org/10.6069/K4TW-Q814) observations

## Pre-processing steps (if we want to bias correct)
First, you will need to collate climate model data ready to calculate monthly PM<sub>2.5</sub> concentrations.

- For GBD 2021: Convert observations from R data to netcdf using `0a_Save_DIMAQ_PM2.5_data.ipynb`
- For GBD 2023: Convert observations from .tiff files to netcdf using `0a__Save_IHME_PM2.5_data.ipynb`

## Processing

- Convert the base year (2022) and delta concentrations (scenario-year) into total concentrations for future scenario-year using `1__Process_SHERPA_files.ipynb`

*Maybe...*
- Bias correct the model product using `3__Bias_correct_PM25.ipynb` with the observations and historical data. 
    - This step includes downscaling the climate model data to the same grid as the observations (0.1°x0.1° resoluution)

### Expected file outputs
`EU_concentration_{scenario}_{year-yyyy}.nc`  

## Data Citations

### SHERPA
...

### Observations
*GBD 2021*  
Gavin Shaddick, Matthew L. Thomas, Heresh Amini, David Broday, Aaron Cohen, Joseph Frostad, Amelia Green, Sophie Gumy, Yang Liu, Randall V. Martin, Annette Pruss-Ustun, Daniel Simpson, Aaron van Donkelaar, and Michael Brauer Environmental Science & Technology 2018 52 (16), 9069-9078 DOI: 10.1021/acs.est.8b02864  
*Saved as an .Rdata file in appendix*  

*GBD 2023*   
Global Burden of Disease Collaborative Network. Global Burden of Disease Study 2023 (GBD 2023) Air Pollution Exposure Estimates and Risk Curves 1990-2023. Seattle, United States of America: Institute for Health Metrics and Evaluation (IHME), 2026.   
*Ambient Particulate Matter Exposure Estimates [CSV] file download*


