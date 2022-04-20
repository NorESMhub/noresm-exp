# NorESM2-MM AMIP

## Data storage
All data are CMOR-ized and public available here: https://esg-dn1.nsc.liu.se/search/cmip6-liu/

All raw data from NorESM2-LM historical simulations are stored on NIRD @ sigma2 under:
```
/projects/NS9560K/noresm/cases/
```
## AMIP

Atmospheric Model Intercomparison Project (AMIP) style runs are runs in which the atmosphere and land components are active while values for sea surface temperatures and sea ice are prescribed (that is, read from a file). AMIP historical simulations start with **NFHIST_**

The AMIP simulation which is part of DECK uses observed SSTs and observed sea-ice:

- **NFHISTfrc2_f09_mg17_20191107 (1975 - 2012)**

Please note, this simulation does not have the NorESM2 derived DMS emissions, but uses Lana.

The cmorized data can be accessed on NIRD @ sigma2 under: 

```
 /projects/NS9034K/CMIP6/CMIP/NCC/NorESM2-MM/amip/
```


## Simulation specifics

### NFHISTfrc2_f09_mg17_20191107 (1975 - 2012)
|  |  |  
| --- | :--- | 
| CESM parent| CESM2.1.0  | 
| Parent | - |
| Run type  | hybrid |
| Branch time from parent | 1975-01-01 |
| Simulated years | 01-01-1975 - 31-12-2012 |   
| Compset | HIST_CAM60%NORESM%NORPDDMSBC_CLM50%BGC-CROP_CICE%PRES_DOCN%DOM_MOSART_SGLC_SWAV |
| Git branch | featureCESM2.1.0-OsloDevelopment |
| Git commit |- |
| Resolution | f09_tn14 |
| Machine  |  -  |
| Case folder | -|
| Diagnostics | - |
