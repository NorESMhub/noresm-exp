# Data storage
All data are CMOR-ized and public available here: https://esg-dn1.nsc.liu.se/search/cmip6-liu/

All raw data from NorESM2-MM historical simulations are stored on NIRD @ sigma2 under:
```
/projects/NS9560K/noresm/cases/
```

## Fully coupled simulations:

Fully coupled historcal simulations start with NHIST_

- Ensemble member 1: 
  - NHISTfrc2_f09_tn14_20191001 (1850 - 1949) 
  - NHISTfrc2_f09_tn14_20191025 (1950-2014)
  
- Ensemble member 2: 
  - NHISTfrc2_02_f09_tn14_20200427 (1850 - 1949)
  - NHISTfrc2_02_f09_tn14_20200519 (1950-2014)
  
- Ensemble member 3: 
  - NHISTfrc2_03_f09_tn14_20200519 (1850 - 1949) 
  - years 1950-2014 not completed,

The cmorized data can be accessed on NIRD @ sigma2 under: 

```
/projects/NS9034K/CMIP6/CMIP/NCC/NorESM2-MM/historical/
```
  
## AMIP:

Atmospheric Model Intercomparison Project (AMIP) style runs are runs in which the atmosphere and land components are active while values for sea surface temperatures and sea ice are prescribed (that is, read from a file). AMIP historical simulations start with NFHIST_

- Ensemble member 1: 
  - NFHISTfrc2_f09_mg17_20191107 (1975 - 2013)

The cmorized data can be accessed on NIRD @ sigma2 under: 

```
 /projects/NS9034K/CMIP6/CMIP/NCC/NorESM2-MM/amip/
```

# Path to case directory

on Fram @ sigma2

- Fully coupled, ensemble member 1: 
  - /cluster/projects/nn2345k/matsbn/NorESM/cases/NHISTfrc2_f09_tn14_20191001 (1850 - 1949) 
  - /cluster/projects/nn2345k/matsbn/NorESM/cases/NHISTfrc2_f09_tn14_20191025 (1950-2014)

- Fully coupled, ensemble member 2: 
  - /cluster/projects/nn2345k/adagj/NorESM/cases-cmip6/NHISTfrc2_02_f09_tn14_20200427 (1850 - 1949)
  - /cluster/projects/nn2345k/adagj/NorESM/cases-cmip6/NHISTfrc2_02_f09_tn14_20200519 (1950-2014)
  
- Fully coupled, ensemble member 3: 
  - /cluster/projects/nn2345k/adagj/NorESM/cases-cmip6/NHISTfrc2_03_f09_tn14_20200519 (1850 - 1949) 
  
- AMIP:
  - /cluster/projects/nn2345k/matsbn/NorESM/cases/NFHISTfrc2_f09_mg17_20191107 (1975-2013)

# Path to diagnostics

http://ns2345k.web.sigma2.no/noresm_diagnostics/NHISTfrc2_f09_tn14_20191025/

# Time series of spinup

<figure>
  <img src="images/noresm2mm_hist1.png" alt="NorESM2-MM spinup simulations" style="width:120%">
  <figcaption><b>NorESM2-MM spinup simulation</b><br>
    <b>Left column (from top to bottom):</b> Globally and annually averaged Surface (2m) air temperature, global and volume averaged ocean temperature, Sea surface temperature (SST). <b>Right column (from top to bottom):</b> Globally and annually  Globally and annually averaged Net radiation @ top of model, Atlantic meridional oveturning circulation (AMOC) @ 26.5N.
  </figcaption>
</figure>

<figure>
  <img src="images/noresm2mm_hist_emis1.png" alt="NorESM2-MM spinup simulations" style="width:120%">
  <figcaption><b>NorESM2-MM spinup simulation</b><br>
    <b>Left column (from top to bottom):</b> Globally and annually sum of Sea salt surface emissions, DMS (dimethylsulfide) surface emissions, POM (primary organic matter) surface emissions  <b>Right column (from top to bottom):</b>  Globally and annually averaged shortwave cloud forcing and longwave cloud forcing.
  </figcaption>
</figure>
