# Data storage
The data is stored on NIRD @ sigma2

/projects/NS2345K/noresm/cases/N1850_f19_tn14_11062019

/projects/NS2345K/noresm/cases/N1850_f19_tn14_11062019_vilje

# Path to case directory

on Fram @ sigma2: /cluster/projects/nn2345k/adagj/NorESM/cases/N1850_f19_tn14_11062019
on Vilje @ sigma2: /home/ntnu/adagj/noresm/cases_2.1.0/N1850_f19_tn14_11062019_vilje


# Summary of simulation
Spin up simulation moved fron Nebula @ nsc.liu to Fram @ sigma2 and an identical simulation on Vilje @ sigma2

No additional code modifications or user name list modifications included compared to N1850OCBDRDDMS_f19_tn14_13052019 and N1850_f19_tn14_06062019.

The increased (x2) error tolerance in energy conservation test, the increased DMS emissions @ high latitudes, the moist convection in CAM6-Nor and the long wave AOD fix were merged to featureCESM2.1.0-OsloDevelopment
and the SourceMod no longer needed

The increased width of Strait of Gibraltar from 15 km to 30 km was included in the micom source code, so the user name list setting in micom was no longer needed

File modifications to components/mosart/src/riverroute/RtmRestFile.F90 which fixed the problems with fill values on Nebula 
and to components/micom/phy/rdlim.F which fixed the time variable output problem in micom were merged into featureCESM2.1.0-OsloDevelopment and the SourceMods no longer needed

# Simulation specifics

|  |  |  
| --- | :--- | 
| CESM parent| CESM2.1.0  | 
| Parent |   N1850_f19_tn14_06062019  |
| Run type  | branch |
| Branch time from parent | 1566-01-01 |
| Simulated years | 01-01-1566 - 31-12-1600 |   
| Compset | 1850_CAM60%PTAERO_CLM50%BGC-CROP_CICE_MICOM%ECO_MOSART_SGLC_SWAV_BGC%BDRDDMS |
| Git branch | featureCESM2.1.0-OsloDevelopment |
| Git commit | 54075ac  |
| Resolution | f19_tn14 |
| Machine  |  Fram and Vilje  |

# Node allocation

```

 <entry id="NTASKS">
      <type>integer</type>
      <values>
        <value compclass="ATM">768</value>
        <value compclass="CPL">768</value>
        <value compclass="OCN">186</value>
        <value compclass="WAV">300</value>
        <value compclass="GLC">768</value>
        <value compclass="ICE">504</value>
        <value compclass="ROF">8</value>
        <value compclass="LND">256</value>
        <value compclass="ESP">1</value>
      </values>
      <desc>number of tasks for each component</desc>
    </entry>


```

# Code modifications (SourceMods)
All code modifications merged to featureCESM2.1.0-OsloDevelopment 54075ac, so no SourceMods needed

# User name lists
All user list settings included in the main source code, so no user list settings needed. 
However, the "old" user_nl_clm (should not have any impact at all)

## user_nl_clm

Reset snow: Remove infiltration excess water as runoff if the temperature of the surface water pool is below freezing. 

```
finidat = '/cluster/shared/noresm/inputdata/cesm2_init/b.e20.B1850.f09_g17.pi_control.all.297/0308-01-01/b.e20.B1850.f09_g17.pi_control.all.297.clm2.r.0308-01-01-00000.nc'
use_init_interp = .true.
reset_snow = .true.
```
