# Data storage
All data are CMOR-ized and public available here: https://esg-dn1.nsc.liu.se/search/cmip6-liu/

All raw data from NorESM2-LM historical simulations are stored on NIRD @ sigma2 under:
```
/projects/NS9560K/noresm/cases/
```
# AMIP

Atmospheric Model Intercomparison Project (AMIP) style runs are runs in which the atmosphere and land components are active while values for sea surface temperatures and sea ice are prescribed (that is, read from a file). AMIP historical simulations start with **NFHIST_**

The AMIP simulation which is part of DECK uses observed SSTs, observed sea-ice and NorESM2 derived DMS emissions:

- **NFHISTnorpddmsbc_f19_mg17_20191025 (1975 - 2014)**

In addition, there exist atmosphere-only historical simulations (1850 - 2014) with NorESM-derived SSTs, sea-ice and DMS emissons. For more details, please see NorESM-LM historical

The cmorized data can be accessed on NIRD @ sigma2 under: 

```
 /projects/NS9034K/CMIP6/CMIP/NCC/NorESM2-LM/amip/
```

# Simulation specifics

## NFHISTnorpddmsbc_f19_mg17_20191025 (1975 - 2014)
|  |  |  
| --- | :--- | 
| CESM parent| CESM2.1.0  | 
| Parent | NHIST_f19_tn14_20190710 |
| Run type  | hybrid |
| Branch time from parent | 1975-01-01 |
| Simulated years | 01-01-1975 - 31-12-2014 |   
| Compset | HIST_CAM60%NORESM%NORPDDMSBC_CLM50%BGC-CROP_CICE%PRES_DOCN%DOM_MOSART_SGLC_SWAV |
| Git branch | featureCESM2.1.0-OsloDevelopment |
| Git commit | ad14769 |
| Resolution | f19_tn14 |
| Machine  |  Vilje  |
| Case folder | /home/ntnu/olivie/cases-cmip6/NFHISTnorpddmsbc_f19_mg17_20191025|
| Diagnostics | - |
