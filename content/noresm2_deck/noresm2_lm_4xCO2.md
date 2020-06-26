

# Data storage
All data are CMOR-ized and public available here: https://esg-dn1.nsc.liu.se/search/cmip6-liu/


All raw data from NorESM2-MM historical simulations are stored on NIRD @ sigma2 under:
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
 /projects/NS9034K/CMIP6/CMIP/NCC/NorESM2-MM/piControl/r1i1p1f1/
```

# Path to case directories

on Fram @ sigma2

- /cluster/projects/nn2345k/matsbn/NorESM/cases/N1850frc2_f09_tn14_20191001
- /cluster/projects/nn2345k/matsbn/NorESM/cases/N1850frc2_f09_tn14_20191012
- /cluster/projects/nn2345k/matsbn/NorESM/cases/N1850frc2_f09_tn14_20191113

# Path to diagnostics

http://ns2345k.web.sigma2.no/noresm_diagnostics/N1850frc2_f09_tn14_20191001/
http://ns2345k.web.sigma2.no/noresm_diagnostics/N1850frc2_f09_tn14_20191012/
http://ns2345k.web.sigma2.no/noresm_diagnostics/N1850frc2_f09_tn14_20191113/

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