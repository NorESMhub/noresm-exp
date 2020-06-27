

# Data storage
All data are CMOR-ized and public available here: https://esg-dn1.nsc.liu.se/search/cmip6-liu/


All raw data from NorESM2-LM DECK simulations are stored on NIRD @ sigma2 under:
```
/projects/NS9560K/noresm/cases/
```

The NorESM2-LM abrupt quadrupling of the atmsopheric CO2 consentration, abrupt-4xCO2, covers the years 1 - 620

- NCO2x4_f19_tn14_20190624 (1 - 140)
- NCO2x4_f19_tn14_20190705 (121 - 150, extra output)
- NCO2x4_f19_tn14_20190724 (151 - 500)
- NCO2x4_f19_tn14_20191129 (501 - 620, run on Nebula @ smhi)

Please note that the years 121 - 140 are calculated twice, in both NCO2x4_f19_tn14_20190624 and NCO2x4_f19_tn14_20190705

The cmorized data can be accessed on NIRD @ sigma2 under: 

```
 /projects/NS9034K/CMIP6/CMIP/NCC/NorESM2-LM/abrupt-4xCO2/r1i1p1f1/
```

# Simulation specifics

## NCO2x4_f19_tn14_20190624 (1 - 140)

|  |  |  
| --- | :--- | 
| CESM parent| CESM2.1.0  | 
| Parent | N1850_f19_tn14_11062019 |
| Run type  | hybrid |
| Branch time from parent | 1600-01-01 |
| Simulated years | 01-01-0001 - 31-12-140 |   
| Compset | 1850_CAM60%NORESM%4xCO2_CLM50%BGC-CROP_CICE%NORESM-CMIP6_MICOM%ECO_MOSART_SGLC_SWAV_BGC%BDRDDMS  |
| Git branch | featureCESM2.1.0-OsloDevelopment |
| Git commit | 6a0b992 |
| Resolution | f19_tn14 |
| Machine  |  Fram  |
| Case folder | /cluster/projects/nn2345k/oyvinds/NorESM2_CMIP6/cases/NCO2x4_f19_tn14_20190624|
| Diagnostics | http://ns2345k.web.sigma2.no/noresm_diagnostics/NCO2x4_f19_tn14_20190624/ |

## NCO2x4_f19_tn14_20190705 (121 - 150, extra output)

|  |  |  
| --- | :--- | 
| CESM parent| CESM2.1.0  | 
| Parent | NCO2x4_f19_tn14_20190624 |
| Run type  | branch |
| Branch time from parent | 0121-01-01 |
| Simulated years | 01-01-0121 - 31-12-150 |   
| Compset | 1850_CAM60%NORESM%4xCO2_CLM50%BGC-CROP_CICE%NORESM-CMIP6_MICOM%ECO_MOSART_SGLC_SWAV_BGC%BDRDDMS  |
| Git branch | featureCESM2.1.0-OsloDevelopment |
| Git commit | e2c861c |
| Resolution | f19_tn14 |
| Machine  |  Fram  |
| Case folder | /cluster/projects/nn2345k/olivie/cases-cmip6/NCO2x4_f19_tn14_20190705 |
| Diagnostics | http://ns2345k.web.sigma2.no/noresm_diagnostics/NCO2x4_f19_tn14_20190624/ |

## NCO2x4_f19_tn14_20190724 (151 - 500)

|  |  |  
| --- | :--- | 
| CESM parent| CESM2.1.0  | 
| Parent | NCO2x4_f19_tn14_20190705 |
| Run type  | branch |
| Branch time from parent | 0151-01-01 |
| Simulated years | 01-01-0121 - 31-12-0500 |   
| Compset | 1850_CAM60%NORESM%4xCO2_CLM50%BGC-CROP_CICE%NORESM-CMIP6_MICOM%ECO_MOSART_SGLC_SWAV_BGC%BDRDDMS  |
| Git branch | featureCESM2.1.0-OsloDevelopment |
| Git commit | e2c861c |
| Resolution | f19_tn14 |
| Machine  |  Fram  |
| Case folder | /cluster/projects/nn2345k/olivie/cases-cmip6/NCO2x4_f19_tn14_20190724 |
| Diagnostics | http://ns2345k.web.sigma2.no/noresm_diagnostics/NCO2x4_f19_tn14_20190724/ |


## NCO2x4_f19_tn14_20191129 (501 - 620)

|  |  |  
| --- | :--- | 
| CESM parent| CESM2.1.0  | 
| Parent | NCO2x4_f19_tn14_20190724 |
| Run type  | branch |
| Branch time from parent | 0501-01-01 |
| Simulated years | 01-01-0501 - 31-12-0620 |   
| Compset | 1850_CAM60%NORESM%4xCO2_CLM50%BGC-CROP_CICE%NORESM-CMIP6_MICOM%ECO_MOSART_SGLC_SWAV_BGC%BDRDDMS  |
| Git branch | featureCESM2.1.0-OsloDevelopment |
| Git commit | 7c32613 |
| Resolution | f19_tn14 |
| Machine  |  Nebula @ smhi |
| Case folder |  /home/sm_adagj/noresm/cases-cmip6/NCO2x4_f19_tn14_20191129 |
| Diagnostics | http://ns2345k.web.sigma2.no/noresm_diagnostics/NCO2x4_f19_tn14_20191129/ |


# Time series of spinup

<figure>
  <img src="images/noresm2lm_4xCO2.png" alt="NorESM2-LM abrupt-4xCO2 simulations" style="width:120%">
  <figcaption><b>NorESM2-LM abrupt-4xCO2 simulations</b><br>
    <b>Left column (from top to bottom):</b> Globally and annually averaged Surface (2m) air temperature, global and volume averaged ocean temperature, Sea surface temperature (SST). <b>Right column (from top to bottom):</b> Globally and annually  Globally and annually averaged Net radiation @ top of model, Atlantic meridional oveturning circulation (AMOC) @ 26.5N.
  </figcaption>
</figure>

<figure>
  <img src="images/noresm2lm_emis_4xCO2.png" alt="NorESM2-LM abrupt-4xCO2 simulations" style="width:120%">
  <figcaption><b>NorESM2-LM abrupt-4xCO2 simulations</b><br>
    <b>Left column (from top to bottom):</b> Globally and annually sum of Sea salt surface emissions, DMS (dimethylsulfide) surface emissions, POM (primary organic matter) surface emissions  <b>Right column (from top to bottom):</b>  Globally and annually averaged shortwave cloud forcing and longwave cloud forcing.
  </figcaption>
</figure>
