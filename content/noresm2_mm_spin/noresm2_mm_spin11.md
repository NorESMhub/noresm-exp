
# Data storage
The data is stored on NIRD @ sigma2

/projects/NS2345K/noresm/cases/N1850_f09_tn14_20190604


# Path to case directory

on Fram @ sigma2

/cluster/projects/nn2345k/matsbn/NorESM/cases/N1850_f09_tn14_20190604/

# Path to diagnostics

http://ns2345k.web.sigma2.no/noresm_diagnostics/N1850_f09_tn14_20190604/

# Summary of simulation

New in this simulation: 
- CESM2.0 updated to CESM2.1 (branch featureCESM2.1.0-OsloDevelopment)
- Bug fix in moist plume calculation and initialisation of tu (moist thermo in zm_conv.F90)
- Different reference time in netCDF output of BLOM/MICOM (rdlim.F), do not change answer.
- Name list changes to user_nl_cam:
  - Decreased gamma from 0.308 to 0.283
  - cldfrc2m_rhmini = 0.80D0 -> 0.90D0
  - micro_mg_dcs = 500.D-6 -> 5.5e-4
- Compset name changed from N1850OCBDRDDMS to N1850, but the copset longname is the same


Continued to use:
- the correction of bug in the second-order in time term of the AM correction (cd_core.F90)
- the removal of an inconsistency in the treatment of riverine carbon inputs in iHAMOCC (mo_riverinpt.F90)
- the increased (x2) error tolerance in energy conservation test in CICE
- the long wave aerosol optical depth (AOD) bug fixer optinterpol.F90 included as SourceMod
- the updated emission files for CAM6-Nor (often referred to as FRC2)
- the increase in DMS emissions @ high latitudes in order to reduce the net radiation imbalance @TOM (top of model)
- the increase in width of Strait of Gibraltar from 15 km to 30 km
- the modifications to the parameterisation of ice clouds (iceopt=5 and cldfrc2m.F90)
- the modifications to the parameters bkopal, rcalc and ropal in iHAMOCC included as SourceMod
- the modifications to the convection code included as SourceMod: zm_conv.F90: "zmst" modifications.
- aerotab_table_dir = '/cluster/shared/noresm/inputdata/noresm-only/atm/cam/camoslo/AeroTab_8jun17'

    
File modifications to 
- CAM6-Nor: cd_core.F90, optinterpol.F90. 
- CICE:  ice_therm_vertical.F90
- iHAMOCC: mo_riverinpt.F90, beleg_bgc.F90

were merged into featureCESM2.1.0-OsloDevelopment and the SourceMods no longer needed. Also the new emission files (frc2) and many of the parameter settings in user_nl_cam were included and no longer needed to be listed in user_nl_cam.

The increase in width of Strait of Gibraltar from 15 km to 30 km was included as default and no longer listed in user_nl_micom

The reset snow addition in user_nl_clm was included as default and no longer needed.

For all SourceMods and user name list specifics, see bottom of this page

# Simulation specifics

|  |  |  
| --- | :--- | 
| CESM parent| CESM2.1.0  | 
| Parent | N1850OCBDRDDMS_f09_tn14_20190515 |
| Run type  | hybrid |
| Branch time from parent | 01-01-0451 |
| Simulated years | 01-01-0451 - 31-12-0480 |   
| Compset | 1850_CAM60%PTAERO_CLM50%BGC-CROP_CICE_MICOM%ECO_MOSART_SGLC_SWAV_BGC%BDRDDMS |
| Git branch | featureCESM2.1.0-OsloDevelopment | 
| Git commit | eac8f29 |
| Resolution | f09_tn14 |
| Machine  |  Fram  |

# Node allocation

```
    <entry id="NTASKS">
      <type>integer</type>
      <values>
        <value compclass="ATM">1536</value>
        <value compclass="CPL">1536</value>
        <value compclass="OCN">91</value>
        <value compclass="WAV">300</value>
        <value compclass="GLC">1536</value>
        <value compclass="ICE">736</value>
        <value compclass="ROF">20</value>
        <value compclass="LND">780</value>
        <value compclass="ESP">1</value>
      </values>
      <desc>number of tasks for each component</desc>
    </entry>


```
# Code modifications (SourceMods)


## Ice cloud parameterisation changes
Modified "aist" threshold
in components/cam/src/physics/cam/cldfrc2m.F90

Line 47 and 48 from 

```
real(r8),  parameter :: qist_min     = 1.e-7_r8      ! Minimum in-stratus ice IWC constraint [ kg/kg ]
real(r8),  parameter :: qist_max     = 5.e-3_r8      ! Maximum in-stratus ice IWC constraint [ kg/kg ]
```

to 

```
real(r8),  parameter :: qist_min     = 5.e-6_r8      ! Minimum in-stratus ice IWC constraint [ kg/kg ] 
real(r8),  parameter :: qist_max     = 2.5e-4_r8     ! Maximum in-stratus ice IWC constraint [ kg/kg ]
```


Line 883 and Line 1137 from

```
aist = max(0._r8,min(1._r8,qi/qist_min)) 
```
to 

```
aist = max(0._r8,min(1._r8,sqrt(aist*qi/qist_min)))
```

# User name lists

## gamma

*Gamma* controls the skewness of Gaussian PDF for the subgrid vertical velocities (used in the Cloud Layers Unified By Binormals (CLUBB) scheme).  A low gamma generally increases the amount of low clouds and hence gives a higher short-wave cloud forcing.

## iceopt

Iceopt is used for setting the parameterisation of ice-cloud fraction. The CESM2 default scheme for the parameterisation of the ice-cloud fraction is iceopt = 5, which includes a functional dependence of ice cloud fraction on the environmental relative humidity. 


## user_nl_cam
``` 
! Users should add all user specific namelist changes below in the form of
! namelist_var = new_namelist_value

&dyn_fv_inparm
 fv_am_correction= .true.
 fv_am_diag      = .true.
 fv_am_fix_lbl   = .true.
 fv_am_fixer     = .true.

&phys_ctl_nl
 dme_energy_adjust = .true.
 aerotab_table_dir = '/cluster/shared/noresm/inputdata/noresm-only/atm/cam/camoslo/AeroTab_8jun17'

&circ_diag_nl
 do_circulation_diags = .true.

 clubb_history  = .false.
 history_budget = .false.
 history_vdiag  = .false.

&zmconv_nl
 zmconv_c0_lnd    =  0.0200D0
 zmconv_c0_ocn    =  0.0200D0
 zmconv_ke        =  8.0E-6

&micro_mg_nl
 micro_mg_dcs     = 5.5e-4

&clubb_params_nl
 clubb_gamma_coef = 0.283

&gw_drag_nl
 tau_0_ubc        = .true.

&cldfrc2m_nl
 cldfrc2m_rhmini =0.90D0
                                                                                                                                   
``` 

# Time series of spinup

<figure>
  <img src="images/spinupmm_11.png" alt="NorESM2-MM spinup simulations" style="width:120%">
  <figcaption><b>NorESM2-MM spinup simulation</b><br>
    <b>Left column (from top to bottom):</b> Globally and annually averaged Surface (2m) air temperature, global and volume averaged ocean temperature, Sea surface temperature (SST). <b>Right column (from top to bottom):</b> Globally and annually  Globally and annually averaged Net radiation @ top of model, Atlantic meridional oveturning circulation (AMOC) @ 26.5N.
  </figcaption>
</figure>

<figure>
  <img src="images/spinupmm_emis11.png" alt="NorESM2-MM spinup simulations" style="width:120%">
  <figcaption><b>NorESM2-MM spinup simulation</b><br>
    <b>Left column (from top to bottom):</b> Globally and annually sum of Sea salt surface emissions, DMS (dimethylsulfide) surface emissions, POM (primary organic matter) surface emissions  <b>Right column (from top to bottom):</b>  Globally and annually averaged shortwave cloud forcing and longwave cloud forcing.
  </figcaption>
</figure>
