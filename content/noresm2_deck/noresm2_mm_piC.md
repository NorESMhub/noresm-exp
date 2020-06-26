# Data storage
All data are CMOR-ized and public available here: https://esg-dn1.nsc.liu.se/search/cmip6-liu/


All raw data from NorESM2-MM historical simulations are stored on NIRD @ sigma2 under:
```
/projects/NS9560K/noresm/cases/
```

The NorESM2-MM pre-industial experiment, piControl, covers the years 1200 - 1699

- N1850frc2_f09_tn14_20191001 (1200 - 1299)
- N1850frc2_f09_tn14_20191012 (1300 - 1450)
- N1850frc2_f09_tn14_20191113 (1450 - 1699)

Please note that the year 1450 is calculated twice, in both N1850frc2_f09_tn14_20191012 and N1850frc2_f09_tn14_20191113

The cmorized data can be accessed on NIRD @ sigma2 under: 

```
 /projects/NS9034K/CMIP6/CMIP/NCC/NorESM2-MM/piControl/r1i1p1f1/
```
# Simulation specifics

## N1850frc2_f09_tn14_20191001 (1200 - 1299)
|  |  |  
| --- | :--- | 
| CESM parent| CESM2.1.0  | 
| Parent | N1850_f09_tn14_20190913 |
| Run type  | hybrid |
| Branch time from parent | 1200-01-01 |
| Simulated years | 01-01-1200 - 31-12-1299|   
| Compset | 1850_CAM60%NORESM%FRC2_CLM50%BGC-CROP_CICE%NORESM-CMIP6_MICOM%ECO_MOSART_SGLC_SWAV_BGC%BDRDDMS |
| Git branch | featureCESM2.1.0-OsloDevelopment |
| Git commit | 47aa2a4 |
| Resolution | f09_tn14 |
| Machine  |  Fram  |
| Case folder | /cluster/projects/nn2345k/matsbn/NorESM/cases/N1850frc2_f09_tn14_20191001|
| Diagnostics |http://ns2345k.web.sigma2.no/noresm_diagnostics/N1850frc2_f09_tn14_20191001/ |

## N1850frc2_f09_tn14_20191012 (1300 - 1450)
|  |  |  
| --- | :--- | 
| CESM parent| CESM2.1.0  | 
| Parent | N1850frc2_f09_tn14_20191001 |
| Run type  | branch |
| Branch time from parent | 1300-01-01 |
| Simulated years | 01-01-1300 - 31-12-1450|   
| Compset | 1850_CAM60%NORESM%FRC2_CLM50%BGC-CROP_CICE%NORESM-CMIP6_MICOM%ECO_MOSART_SGLC_SWAV_BGC%BDRDDMS |
| Git branch | featureCESM2.1.0-OsloDevelopment |
| Git commit | 8141ee9 |
| Resolution | f09_tn14 |
| Machine  |  Fram  |
| Case folder | /cluster/projects/nn2345k/matsbn/NorESM/cases/N1850frc2_f09_tn14_20191012|
| Diagnostics |http://ns2345k.web.sigma2.no/noresm_diagnostics/N1850frc2_f09_tn14_20191012/ |

## N1850frc2_f09_tn14_20191113 (1450 - 1699)
|  |  |  
| --- | :--- | 
| CESM parent| CESM2.1.0  | 
| Parent | N1850frc2_f09_tn14_20191001 |
| Run type  | branch |
| Branch time from parent | 1450-01-01 |
| Simulated years | 01-01-1450 - 31-12-1699|   
| Compset | 1850_CAM60%NORESM%FRC2_CLM50%BGC-CROP_CICE%NORESM-CMIP6_MICOM%ECO_MOSART_SGLC_SWAV_BGC%BDRDDMS |
| Git branch | featureCESM2.1.0-OsloDevelopment |
| Git commit | 7a21a65  |
| Resolution | f09_tn14 |
| Machine  |  Fram  |
| Case folder | /cluster/projects/nn2345k/matsbn/NorESM/cases/N1850frc2_f09_tn14_20191113|
| Diagnostics | http://ns2345k.web.sigma2.no/noresm_diagnostics/N1850frc2_f09_tn14_20191113/ |


# Time series of spinup

<figure>
  <img src="images/noresm2mm_piC.png" alt="NorESM2-MM piControl simulations" style="width:120%">
  <figcaption><b>NorESM2-MM spinup simulation</b><br>
    <b>Left column (from top to bottom):</b> Globally and annually averaged Surface (2m) air temperature, global and volume averaged ocean temperature, Sea surface temperature (SST). <b>Right column (from top to bottom):</b> Globally and annually  Globally and annually averaged Net radiation @ top of model, Atlantic meridional oveturning circulation (AMOC) @ 26.5N.
  </figcaption>
</figure>

<figure>
  <img src="images/noresm2mm_piC.png" alt="NorESM2-MM piControl simulations" style="width:120%">
  <figcaption><b>NorESM2-MM spinup simulation</b><br>
    <b>Left column (from top to bottom):</b> Globally and annually sum of Sea salt surface emissions, DMS (dimethylsulfide) surface emissions, POM (primary organic matter) surface emissions  <b>Right column (from top to bottom):</b>  Globally and annually averaged shortwave cloud forcing and longwave cloud forcing.
  </figcaption>
</figure>
