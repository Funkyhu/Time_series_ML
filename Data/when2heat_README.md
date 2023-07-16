
DATAPACKAGE: WHEN2HEAT HEATING PROFILES
===========================================================================

https://doi.org/10.25832/when2heat/2022-02-22

by Open Power System Data: http://www.open-power-system-data.org/

Package Version: 2022-02-22

Simulated hourly country-aggregated heat demand and COP time series

This dataset comprises national time series for representing building heat
pumps in power system models. The heat demand of buildings and the
coefficient of performance (COP) of heat pumps is calculated for 28
European countries from 2008 to 2020 in an hourly resolution.
Heat demand time series for space and water heating are computed by
combining gas standard load profiles with spatial temperature and wind
speed reanalysis data as well as population geodata. The profiles are
year-wise scaled to 1 TWh each. For the years 2008 to 2015, the data is
additionally scaled with annual statistics on the final energy consumption
for heating.
COP time series for different heat sources – air, ground, and groundwater
– and different heat sinks – floor heating, radiators, and water
heating – are calculated based on COP and heating curves using reanalysis
temperature data, spatially aggregated with respect to the heat demand, and
corrected based on field measurements.
All data processing as well as the download of relevant input data is
conducted in python and pandas and has been documented in the Jupyter
notebooks linked below. Please also consider and cite our <a
href="https://doi.org/10.1038/s41597-019-0199-y">Data Descriptor</a> of the
original dataset as well as our <a
href="http://hdl.handle.net/10419/249997">Working Paper</a> at on recent
updates and extensions of the dataset.

The data package covers the geographical region of 28 European countries.

We follow the Data Package standard by the Frictionless Data project, a
part of the Open Knowledge Foundation: http://frictionlessdata.io/


Documentation and script
===========================================================================

This README only contains the most basic information about the data package.
For the full documentation, please see the notebook script that was used to
generate the data package. You can find it at:

https://nbviewer.jupyter.org/github/oruhnau/when2heat/blob/2022-02-22/main.ipynb

Or on GitHub at:

https://github.com/oruhnau/when2heat/blob/2022-02-22/main.ipynb

License and attribution
===========================================================================

Data license: 
    [Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/)

Script license:
    [MIT License](https://opensource.org/licenses/MIT)

Attribution:
    Attribution should be given as follows:

- Ruhnau, O., Hirth, L., and
    Praktiknjo, A. (2019). Time series of heat demand and heat pump
    efficiency for energy system modeling. Scientific Data, 6, 189.
    https://doi.org/10.1038/s41597-019-0199-y
- Ruhnau, O., Muessel, J.
    (2022). Update and extension of the When2Heat dataset. Econstor Working
    Paper. http://hdl.handle.net/10419/249997
- Ruhnau, O., Muessel, J.
    (2022). When2Heat Heating Profiles. Open Power System Data.
    https://doi.org/10.25832/when2heat/2022-02-22


Version history
===========================================================================

* 2022-02-22 Update and extension
* 2019-08-06 Minor revisions


Resources
===========================================================================

* [Package description page](http://data.open-power-system-data.org/when2heat/2022-02-22/)
* [ZIP Package](http://data.open-power-system-data.org/when2heat/opsd-when2heat-2022-02-22.zip)
* [Script and documentation](https://github.com/oruhnau/when2heat/blob/2022-02-22/main.ipynb)
* [Original input data](http://data.open-power-system-data.org/when2heat/2022-02-22/original_data/)


Sources
===========================================================================

* [ECMWF](https://www.ecmwf.int/en/forecasts/datasets/reanalysis-datasets/era5)
* [Eurostat](http://ec.europa.eu/eurostat/web/gisco/geodata/reference-data/population-distribution-demography/geostat)
* [JRC-IDEEES](https://ec.europa.eu/jrc/en/potencia/jrc-idees)
* [BGW](http://www.gwb-netz.de/wa_files/05_bgw_leitfaden_lastprofile_56550.pdf)
* [BDEW](https://www.enwg-veroeffentlichungen.de/badtoelz/Netze/Gasnetz/Netzbeschreibung/LF-Abwicklung-von-Standardlastprofilen-Gas-20110630-final.pdf)


Field documentation
===========================================================================


when2heat.csv
---------------------------------------------------------------------------

* utc_timestamp
    - Type: datetime
    - Format: YYYY-MM-DDThh:mm:ssZ
    - Description: Start of timeperiod in Coordinated Universal Time
* cet_cest_timestamp
    - Type: datetime
    - Format: YYYY-MM-DDThh:mm:ss
    - Description: Start of timeperiod in Central European (Summer-) Time
* AT_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Austria with floor heating
* AT_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Austria with radiators
* AT_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Austria
* AT_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Austria with floor heating
* AT_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Austria with radiators
* AT_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Austria
* AT_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Austria with floor heating
* AT_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Austria with radiators
* AT_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Austria
* AT_heat_demand_space
    - Type: number
    - Description: Heat demand in Austria in MW for space heating
* AT_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Austria in MW for space heating in commercial buildings
* AT_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Austria in MW for space heating in multi-family houses
* AT_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Austria in MW for space heating in single-family houses
* AT_heat_demand_total
    - Type: number
    - Description: Heat demand in Austria in MW for space and water heating
* AT_heat_demand_water
    - Type: number
    - Description: Heat demand in Austria in MW for water heating
* AT_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Austria in MW for water heating in commercial buildings
* AT_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Austria in MW for water heating in multi-family houses
* AT_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Austria in MW for water heating in single-family houses
* AT_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Austria in MW/TWh for space heating in commercial buildings
* AT_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Austria in MW/TWh for space heating in multi-family houses
* AT_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Austria in MW/TWh for space heating in single-family houses
* AT_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Austria in MW/TWh for water heating in commercial buildings
* AT_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Austria in MW/TWh for water heating in multi-family houses
* AT_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Austria in MW/TWh for water heating in single-family houses
* BE_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Belgium with floor heating
* BE_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Belgium with radiators
* BE_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Belgium
* BE_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Belgium with floor heating
* BE_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Belgium with radiators
* BE_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Belgium
* BE_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Belgium with floor heating
* BE_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Belgium with radiators
* BE_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Belgium
* BE_heat_demand_space
    - Type: number
    - Description: Heat demand in Belgium in MW for space heating
* BE_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Belgium in MW for space heating in commercial buildings
* BE_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Belgium in MW for space heating in multi-family houses
* BE_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Belgium in MW for space heating in single-family houses
* BE_heat_demand_total
    - Type: number
    - Description: Heat demand in Belgium in MW for space and water heating
* BE_heat_demand_water
    - Type: number
    - Description: Heat demand in Belgium in MW for water heating
* BE_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Belgium in MW for water heating in commercial buildings
* BE_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Belgium in MW for water heating in multi-family houses
* BE_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Belgium in MW for water heating in single-family houses
* BE_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Belgium in MW/TWh for space heating in commercial buildings
* BE_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Belgium in MW/TWh for space heating in multi-family houses
* BE_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Belgium in MW/TWh for space heating in single-family houses
* BE_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Belgium in MW/TWh for water heating in commercial buildings
* BE_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Belgium in MW/TWh for water heating in multi-family houses
* BE_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Belgium in MW/TWh for water heating in single-family houses
* BG_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Bulgaria with floor heating
* BG_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Bulgaria with radiators
* BG_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Bulgaria
* BG_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Bulgaria with floor heating
* BG_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Bulgaria with radiators
* BG_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Bulgaria
* BG_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Bulgaria with floor heating
* BG_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Bulgaria with radiators
* BG_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Bulgaria
* BG_heat_demand_space
    - Type: number
    - Description: Heat demand in Bulgaria in MW for space heating
* BG_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Bulgaria in MW for space heating in commercial buildings
* BG_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Bulgaria in MW for space heating in multi-family houses
* BG_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Bulgaria in MW for space heating in single-family houses
* BG_heat_demand_total
    - Type: number
    - Description: Heat demand in Bulgaria in MW for space and water heating
* BG_heat_demand_water
    - Type: number
    - Description: Heat demand in Bulgaria in MW for water heating
* BG_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Bulgaria in MW for water heating in commercial buildings
* BG_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Bulgaria in MW for water heating in multi-family houses
* BG_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Bulgaria in MW for water heating in single-family houses
* BG_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Bulgaria in MW/TWh for space heating in commercial buildings
* BG_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Bulgaria in MW/TWh for space heating in multi-family houses
* BG_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Bulgaria in MW/TWh for space heating in single-family houses
* BG_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Bulgaria in MW/TWh for water heating in commercial buildings
* BG_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Bulgaria in MW/TWh for water heating in multi-family houses
* BG_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Bulgaria in MW/TWh for water heating in single-family houses
* CH_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Switzerland with floor heating
* CH_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Switzerland with radiators
* CH_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Switzerland
* CH_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Switzerland with floor heating
* CH_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Switzerland with radiators
* CH_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Switzerland
* CH_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Switzerland with floor heating
* CH_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Switzerland with radiators
* CH_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Switzerland
* CH_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Switzerland in MW/TWh for space heating in commercial buildings
* CH_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Switzerland in MW/TWh for space heating in multi-family houses
* CH_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Switzerland in MW/TWh for space heating in single-family houses
* CH_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Switzerland in MW/TWh for water heating in commercial buildings
* CH_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Switzerland in MW/TWh for water heating in multi-family houses
* CH_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Switzerland in MW/TWh for water heating in single-family houses
* CZ_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Czech Republic with floor heating
* CZ_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Czech Republic with radiators
* CZ_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Czech Republic
* CZ_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Czech Republic with floor heating
* CZ_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Czech Republic with radiators
* CZ_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Czech Republic
* CZ_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Czech Republic with floor heating
* CZ_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Czech Republic with radiators
* CZ_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Czech Republic
* CZ_heat_demand_space
    - Type: number
    - Description: Heat demand in Czech Republic in MW for space heating
* CZ_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Czech Republic in MW for space heating in commercial buildings
* CZ_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Czech Republic in MW for space heating in multi-family houses
* CZ_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Czech Republic in MW for space heating in single-family houses
* CZ_heat_demand_total
    - Type: number
    - Description: Heat demand in Czech Republic in MW for space and water heating
* CZ_heat_demand_water
    - Type: number
    - Description: Heat demand in Czech Republic in MW for water heating
* CZ_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Czech Republic in MW for water heating in commercial buildings
* CZ_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Czech Republic in MW for water heating in multi-family houses
* CZ_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Czech Republic in MW for water heating in single-family houses
* CZ_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Czech Republic in MW/TWh for space heating in commercial buildings
* CZ_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Czech Republic in MW/TWh for space heating in multi-family houses
* CZ_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Czech Republic in MW/TWh for space heating in single-family houses
* CZ_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Czech Republic in MW/TWh for water heating in commercial buildings
* CZ_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Czech Republic in MW/TWh for water heating in multi-family houses
* CZ_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Czech Republic in MW/TWh for water heating in single-family houses
* DE_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Germany with floor heating
* DE_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Germany with radiators
* DE_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Germany
* DE_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Germany with floor heating
* DE_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Germany with radiators
* DE_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Germany
* DE_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Germany with floor heating
* DE_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Germany with radiators
* DE_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Germany
* DE_heat_demand_space
    - Type: number
    - Description: Heat demand in Germany in MW for space heating
* DE_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Germany in MW for space heating in commercial buildings
* DE_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Germany in MW for space heating in multi-family houses
* DE_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Germany in MW for space heating in single-family houses
* DE_heat_demand_total
    - Type: number
    - Description: Heat demand in Germany in MW for space and water heating
* DE_heat_demand_water
    - Type: number
    - Description: Heat demand in Germany in MW for water heating
* DE_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Germany in MW for water heating in commercial buildings
* DE_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Germany in MW for water heating in multi-family houses
* DE_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Germany in MW for water heating in single-family houses
* DE_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Germany in MW/TWh for space heating in commercial buildings
* DE_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Germany in MW/TWh for space heating in multi-family houses
* DE_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Germany in MW/TWh for space heating in single-family houses
* DE_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Germany in MW/TWh for water heating in commercial buildings
* DE_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Germany in MW/TWh for water heating in multi-family houses
* DE_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Germany in MW/TWh for water heating in single-family houses
* DK_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Denmark with floor heating
* DK_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Denmark with radiators
* DK_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Denmark
* DK_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Denmark with floor heating
* DK_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Denmark with radiators
* DK_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Denmark
* DK_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Denmark with floor heating
* DK_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Denmark with radiators
* DK_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Denmark
* DK_heat_demand_space
    - Type: number
    - Description: Heat demand in Denmark in MW for space heating
* DK_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Denmark in MW for space heating in commercial buildings
* DK_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Denmark in MW for space heating in multi-family houses
* DK_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Denmark in MW for space heating in single-family houses
* DK_heat_demand_total
    - Type: number
    - Description: Heat demand in Denmark in MW for space and water heating
* DK_heat_demand_water
    - Type: number
    - Description: Heat demand in Denmark in MW for water heating
* DK_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Denmark in MW for water heating in commercial buildings
* DK_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Denmark in MW for water heating in multi-family houses
* DK_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Denmark in MW for water heating in single-family houses
* DK_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Denmark in MW/TWh for space heating in commercial buildings
* DK_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Denmark in MW/TWh for space heating in multi-family houses
* DK_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Denmark in MW/TWh for space heating in single-family houses
* DK_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Denmark in MW/TWh for water heating in commercial buildings
* DK_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Denmark in MW/TWh for water heating in multi-family houses
* DK_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Denmark in MW/TWh for water heating in single-family houses
* EE_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Estonia with floor heating
* EE_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Estonia with radiators
* EE_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Estonia
* EE_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Estonia with floor heating
* EE_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Estonia with radiators
* EE_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Estonia
* EE_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Estonia with floor heating
* EE_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Estonia with radiators
* EE_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Estonia
* EE_heat_demand_space
    - Type: number
    - Description: Heat demand in Estonia in MW for space heating
* EE_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Estonia in MW for space heating in commercial buildings
* EE_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Estonia in MW for space heating in multi-family houses
* EE_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Estonia in MW for space heating in single-family houses
* EE_heat_demand_total
    - Type: number
    - Description: Heat demand in Estonia in MW for space and water heating
* EE_heat_demand_water
    - Type: number
    - Description: Heat demand in Estonia in MW for water heating
* EE_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Estonia in MW for water heating in commercial buildings
* EE_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Estonia in MW for water heating in multi-family houses
* EE_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Estonia in MW for water heating in single-family houses
* EE_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Estonia in MW/TWh for space heating in commercial buildings
* EE_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Estonia in MW/TWh for space heating in multi-family houses
* EE_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Estonia in MW/TWh for space heating in single-family houses
* EE_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Estonia in MW/TWh for water heating in commercial buildings
* EE_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Estonia in MW/TWh for water heating in multi-family houses
* EE_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Estonia in MW/TWh for water heating in single-family houses
* ES_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Spain with floor heating
* ES_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Spain with radiators
* ES_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Spain
* ES_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Spain with floor heating
* ES_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Spain with radiators
* ES_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Spain
* ES_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Spain with floor heating
* ES_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Spain with radiators
* ES_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Spain
* ES_heat_demand_space
    - Type: number
    - Description: Heat demand in Spain in MW for space heating
* ES_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Spain in MW for space heating in commercial buildings
* ES_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Spain in MW for space heating in multi-family houses
* ES_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Spain in MW for space heating in single-family houses
* ES_heat_demand_total
    - Type: number
    - Description: Heat demand in Spain in MW for space and water heating
* ES_heat_demand_water
    - Type: number
    - Description: Heat demand in Spain in MW for water heating
* ES_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Spain in MW for water heating in commercial buildings
* ES_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Spain in MW for water heating in multi-family houses
* ES_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Spain in MW for water heating in single-family houses
* ES_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Spain in MW/TWh for space heating in commercial buildings
* ES_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Spain in MW/TWh for space heating in multi-family houses
* ES_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Spain in MW/TWh for space heating in single-family houses
* ES_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Spain in MW/TWh for water heating in commercial buildings
* ES_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Spain in MW/TWh for water heating in multi-family houses
* ES_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Spain in MW/TWh for water heating in single-family houses
* FI_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Finland with floor heating
* FI_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Finland with radiators
* FI_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Finland
* FI_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Finland with floor heating
* FI_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Finland with radiators
* FI_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Finland
* FI_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Finland with floor heating
* FI_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Finland with radiators
* FI_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Finland
* FI_heat_demand_space
    - Type: number
    - Description: Heat demand in Finland in MW for space heating
* FI_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Finland in MW for space heating in commercial buildings
* FI_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Finland in MW for space heating in multi-family houses
* FI_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Finland in MW for space heating in single-family houses
* FI_heat_demand_total
    - Type: number
    - Description: Heat demand in Finland in MW for space and water heating
* FI_heat_demand_water
    - Type: number
    - Description: Heat demand in Finland in MW for water heating
* FI_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Finland in MW for water heating in commercial buildings
* FI_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Finland in MW for water heating in multi-family houses
* FI_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Finland in MW for water heating in single-family houses
* FI_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Finland in MW/TWh for space heating in commercial buildings
* FI_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Finland in MW/TWh for space heating in multi-family houses
* FI_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Finland in MW/TWh for space heating in single-family houses
* FI_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Finland in MW/TWh for water heating in commercial buildings
* FI_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Finland in MW/TWh for water heating in multi-family houses
* FI_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Finland in MW/TWh for water heating in single-family houses
* FR_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in France with floor heating
* FR_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in France with radiators
* FR_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in France
* FR_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in France with floor heating
* FR_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in France with radiators
* FR_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in France
* FR_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in France with floor heating
* FR_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in France with radiators
* FR_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in France
* FR_heat_demand_space
    - Type: number
    - Description: Heat demand in France in MW for space heating
* FR_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in France in MW for space heating in commercial buildings
* FR_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in France in MW for space heating in multi-family houses
* FR_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in France in MW for space heating in single-family houses
* FR_heat_demand_total
    - Type: number
    - Description: Heat demand in France in MW for space and water heating
* FR_heat_demand_water
    - Type: number
    - Description: Heat demand in France in MW for water heating
* FR_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in France in MW for water heating in commercial buildings
* FR_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in France in MW for water heating in multi-family houses
* FR_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in France in MW for water heating in single-family houses
* FR_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in France in MW/TWh for space heating in commercial buildings
* FR_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in France in MW/TWh for space heating in multi-family houses
* FR_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in France in MW/TWh for space heating in single-family houses
* FR_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in France in MW/TWh for water heating in commercial buildings
* FR_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in France in MW/TWh for water heating in multi-family houses
* FR_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in France in MW/TWh for water heating in single-family houses
* GB_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Great Britain with floor heating
* GB_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Great Britain with radiators
* GB_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Great Britain
* GB_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Great Britain with floor heating
* GB_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Great Britain with radiators
* GB_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Great Britain
* GB_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Great Britain with floor heating
* GB_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Great Britain with radiators
* GB_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Great Britain
* GB_heat_demand_space
    - Type: number
    - Description: Heat demand in Great Britain in MW for space heating
* GB_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Great Britain in MW for space heating in commercial buildings
* GB_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Great Britain in MW for space heating in multi-family houses
* GB_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Great Britain in MW for space heating in single-family houses
* GB_heat_demand_total
    - Type: number
    - Description: Heat demand in Great Britain in MW for space and water heating
* GB_heat_demand_water
    - Type: number
    - Description: Heat demand in Great Britain in MW for water heating
* GB_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Great Britain in MW for water heating in commercial buildings
* GB_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Great Britain in MW for water heating in multi-family houses
* GB_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Great Britain in MW for water heating in single-family houses
* GB_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Great Britain in MW/TWh for space heating in commercial buildings
* GB_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Great Britain in MW/TWh for space heating in multi-family houses
* GB_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Great Britain in MW/TWh for space heating in single-family houses
* GB_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Great Britain in MW/TWh for water heating in commercial buildings
* GB_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Great Britain in MW/TWh for water heating in multi-family houses
* GB_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Great Britain in MW/TWh for water heating in single-family houses
* GR_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Greece with floor heating
* GR_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Greece with radiators
* GR_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Greece
* GR_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Greece with floor heating
* GR_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Greece with radiators
* GR_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Greece
* GR_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Greece with floor heating
* GR_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Greece with radiators
* GR_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Greece
* GR_heat_demand_space
    - Type: number
    - Description: Heat demand in Greece in MW for space heating
* GR_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Greece in MW for space heating in commercial buildings
* GR_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Greece in MW for space heating in multi-family houses
* GR_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Greece in MW for space heating in single-family houses
* GR_heat_demand_total
    - Type: number
    - Description: Heat demand in Greece in MW for space and water heating
* GR_heat_demand_water
    - Type: number
    - Description: Heat demand in Greece in MW for water heating
* GR_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Greece in MW for water heating in commercial buildings
* GR_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Greece in MW for water heating in multi-family houses
* GR_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Greece in MW for water heating in single-family houses
* GR_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Greece in MW/TWh for space heating in commercial buildings
* GR_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Greece in MW/TWh for space heating in multi-family houses
* GR_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Greece in MW/TWh for space heating in single-family houses
* GR_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Greece in MW/TWh for water heating in commercial buildings
* GR_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Greece in MW/TWh for water heating in multi-family houses
* GR_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Greece in MW/TWh for water heating in single-family houses
* HR_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Croatia with floor heating
* HR_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Croatia with radiators
* HR_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Croatia
* HR_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Croatia with floor heating
* HR_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Croatia with radiators
* HR_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Croatia
* HR_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Croatia with floor heating
* HR_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Croatia with radiators
* HR_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Croatia
* HR_heat_demand_space
    - Type: number
    - Description: Heat demand in Croatia in MW for space heating
* HR_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Croatia in MW for space heating in commercial buildings
* HR_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Croatia in MW for space heating in multi-family houses
* HR_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Croatia in MW for space heating in single-family houses
* HR_heat_demand_total
    - Type: number
    - Description: Heat demand in Croatia in MW for space and water heating
* HR_heat_demand_water
    - Type: number
    - Description: Heat demand in Croatia in MW for water heating
* HR_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Croatia in MW for water heating in commercial buildings
* HR_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Croatia in MW for water heating in multi-family houses
* HR_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Croatia in MW for water heating in single-family houses
* HR_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Croatia in MW/TWh for space heating in commercial buildings
* HR_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Croatia in MW/TWh for space heating in multi-family houses
* HR_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Croatia in MW/TWh for space heating in single-family houses
* HR_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Croatia in MW/TWh for water heating in commercial buildings
* HR_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Croatia in MW/TWh for water heating in multi-family houses
* HR_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Croatia in MW/TWh for water heating in single-family houses
* HU_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Hungary with floor heating
* HU_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Hungary with radiators
* HU_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Hungary
* HU_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Hungary with floor heating
* HU_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Hungary with radiators
* HU_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Hungary
* HU_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Hungary with floor heating
* HU_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Hungary with radiators
* HU_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Hungary
* HU_heat_demand_space
    - Type: number
    - Description: Heat demand in Hungary in MW for space heating
* HU_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Hungary in MW for space heating in commercial buildings
* HU_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Hungary in MW for space heating in multi-family houses
* HU_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Hungary in MW for space heating in single-family houses
* HU_heat_demand_total
    - Type: number
    - Description: Heat demand in Hungary in MW for space and water heating
* HU_heat_demand_water
    - Type: number
    - Description: Heat demand in Hungary in MW for water heating
* HU_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Hungary in MW for water heating in commercial buildings
* HU_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Hungary in MW for water heating in multi-family houses
* HU_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Hungary in MW for water heating in single-family houses
* HU_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Hungary in MW/TWh for space heating in commercial buildings
* HU_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Hungary in MW/TWh for space heating in multi-family houses
* HU_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Hungary in MW/TWh for space heating in single-family houses
* HU_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Hungary in MW/TWh for water heating in commercial buildings
* HU_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Hungary in MW/TWh for water heating in multi-family houses
* HU_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Hungary in MW/TWh for water heating in single-family houses
* IE_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Ireland with floor heating
* IE_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Ireland with radiators
* IE_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Ireland
* IE_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Ireland with floor heating
* IE_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Ireland with radiators
* IE_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Ireland
* IE_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Ireland with floor heating
* IE_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Ireland with radiators
* IE_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Ireland
* IE_heat_demand_space
    - Type: number
    - Description: Heat demand in Ireland in MW for space heating
* IE_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Ireland in MW for space heating in commercial buildings
* IE_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Ireland in MW for space heating in multi-family houses
* IE_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Ireland in MW for space heating in single-family houses
* IE_heat_demand_total
    - Type: number
    - Description: Heat demand in Ireland in MW for space and water heating
* IE_heat_demand_water
    - Type: number
    - Description: Heat demand in Ireland in MW for water heating
* IE_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Ireland in MW for water heating in commercial buildings
* IE_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Ireland in MW for water heating in multi-family houses
* IE_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Ireland in MW for water heating in single-family houses
* IE_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Ireland in MW/TWh for space heating in commercial buildings
* IE_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Ireland in MW/TWh for space heating in multi-family houses
* IE_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Ireland in MW/TWh for space heating in single-family houses
* IE_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Ireland in MW/TWh for water heating in commercial buildings
* IE_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Ireland in MW/TWh for water heating in multi-family houses
* IE_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Ireland in MW/TWh for water heating in single-family houses
* IT_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Italy with floor heating
* IT_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Italy with radiators
* IT_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Italy
* IT_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Italy with floor heating
* IT_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Italy with radiators
* IT_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Italy
* IT_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Italy with floor heating
* IT_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Italy with radiators
* IT_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Italy
* IT_heat_demand_space
    - Type: number
    - Description: Heat demand in Italy in MW for space heating
* IT_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Italy in MW for space heating in commercial buildings
* IT_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Italy in MW for space heating in multi-family houses
* IT_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Italy in MW for space heating in single-family houses
* IT_heat_demand_total
    - Type: number
    - Description: Heat demand in Italy in MW for space and water heating
* IT_heat_demand_water
    - Type: number
    - Description: Heat demand in Italy in MW for water heating
* IT_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Italy in MW for water heating in commercial buildings
* IT_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Italy in MW for water heating in multi-family houses
* IT_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Italy in MW for water heating in single-family houses
* IT_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Italy in MW/TWh for space heating in commercial buildings
* IT_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Italy in MW/TWh for space heating in multi-family houses
* IT_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Italy in MW/TWh for space heating in single-family houses
* IT_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Italy in MW/TWh for water heating in commercial buildings
* IT_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Italy in MW/TWh for water heating in multi-family houses
* IT_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Italy in MW/TWh for water heating in single-family houses
* LT_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Lithuania with floor heating
* LT_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Lithuania with radiators
* LT_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Lithuania
* LT_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Lithuania with floor heating
* LT_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Lithuania with radiators
* LT_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Lithuania
* LT_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Lithuania with floor heating
* LT_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Lithuania with radiators
* LT_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Lithuania
* LT_heat_demand_space
    - Type: number
    - Description: Heat demand in Lithuania in MW for space heating
* LT_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Lithuania in MW for space heating in commercial buildings
* LT_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Lithuania in MW for space heating in multi-family houses
* LT_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Lithuania in MW for space heating in single-family houses
* LT_heat_demand_total
    - Type: number
    - Description: Heat demand in Lithuania in MW for space and water heating
* LT_heat_demand_water
    - Type: number
    - Description: Heat demand in Lithuania in MW for water heating
* LT_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Lithuania in MW for water heating in commercial buildings
* LT_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Lithuania in MW for water heating in multi-family houses
* LT_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Lithuania in MW for water heating in single-family houses
* LT_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Lithuania in MW/TWh for space heating in commercial buildings
* LT_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Lithuania in MW/TWh for space heating in multi-family houses
* LT_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Lithuania in MW/TWh for space heating in single-family houses
* LT_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Lithuania in MW/TWh for water heating in commercial buildings
* LT_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Lithuania in MW/TWh for water heating in multi-family houses
* LT_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Lithuania in MW/TWh for water heating in single-family houses
* LU_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Luxembourg with floor heating
* LU_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Luxembourg with radiators
* LU_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Luxembourg
* LU_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Luxembourg with floor heating
* LU_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Luxembourg with radiators
* LU_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Luxembourg
* LU_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Luxembourg with floor heating
* LU_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Luxembourg with radiators
* LU_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Luxembourg
* LU_heat_demand_space
    - Type: number
    - Description: Heat demand in Luxembourg in MW for space heating
* LU_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Luxembourg in MW for space heating in commercial buildings
* LU_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Luxembourg in MW for space heating in multi-family houses
* LU_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Luxembourg in MW for space heating in single-family houses
* LU_heat_demand_total
    - Type: number
    - Description: Heat demand in Luxembourg in MW for space and water heating
* LU_heat_demand_water
    - Type: number
    - Description: Heat demand in Luxembourg in MW for water heating
* LU_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Luxembourg in MW for water heating in commercial buildings
* LU_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Luxembourg in MW for water heating in multi-family houses
* LU_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Luxembourg in MW for water heating in single-family houses
* LU_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Luxembourg in MW/TWh for space heating in commercial buildings
* LU_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Luxembourg in MW/TWh for space heating in multi-family houses
* LU_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Luxembourg in MW/TWh for space heating in single-family houses
* LU_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Luxembourg in MW/TWh for water heating in commercial buildings
* LU_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Luxembourg in MW/TWh for water heating in multi-family houses
* LU_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Luxembourg in MW/TWh for water heating in single-family houses
* LV_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Latvia with floor heating
* LV_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Latvia with radiators
* LV_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Latvia
* LV_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Latvia with floor heating
* LV_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Latvia with radiators
* LV_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Latvia
* LV_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Latvia with floor heating
* LV_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Latvia with radiators
* LV_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Latvia
* LV_heat_demand_space
    - Type: number
    - Description: Heat demand in Latvia in MW for space heating
* LV_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Latvia in MW for space heating in commercial buildings
* LV_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Latvia in MW for space heating in multi-family houses
* LV_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Latvia in MW for space heating in single-family houses
* LV_heat_demand_total
    - Type: number
    - Description: Heat demand in Latvia in MW for space and water heating
* LV_heat_demand_water
    - Type: number
    - Description: Heat demand in Latvia in MW for water heating
* LV_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Latvia in MW for water heating in commercial buildings
* LV_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Latvia in MW for water heating in multi-family houses
* LV_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Latvia in MW for water heating in single-family houses
* LV_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Latvia in MW/TWh for space heating in commercial buildings
* LV_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Latvia in MW/TWh for space heating in multi-family houses
* LV_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Latvia in MW/TWh for space heating in single-family houses
* LV_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Latvia in MW/TWh for water heating in commercial buildings
* LV_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Latvia in MW/TWh for water heating in multi-family houses
* LV_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Latvia in MW/TWh for water heating in single-family houses
* NL_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Netherlands with floor heating
* NL_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Netherlands with radiators
* NL_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Netherlands
* NL_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Netherlands with floor heating
* NL_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Netherlands with radiators
* NL_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Netherlands
* NL_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Netherlands with floor heating
* NL_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Netherlands with radiators
* NL_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Netherlands
* NL_heat_demand_space
    - Type: number
    - Description: Heat demand in Netherlands in MW for space heating
* NL_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Netherlands in MW for space heating in commercial buildings
* NL_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Netherlands in MW for space heating in multi-family houses
* NL_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Netherlands in MW for space heating in single-family houses
* NL_heat_demand_total
    - Type: number
    - Description: Heat demand in Netherlands in MW for space and water heating
* NL_heat_demand_water
    - Type: number
    - Description: Heat demand in Netherlands in MW for water heating
* NL_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Netherlands in MW for water heating in commercial buildings
* NL_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Netherlands in MW for water heating in multi-family houses
* NL_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Netherlands in MW for water heating in single-family houses
* NL_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Netherlands in MW/TWh for space heating in commercial buildings
* NL_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Netherlands in MW/TWh for space heating in multi-family houses
* NL_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Netherlands in MW/TWh for space heating in single-family houses
* NL_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Netherlands in MW/TWh for water heating in commercial buildings
* NL_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Netherlands in MW/TWh for water heating in multi-family houses
* NL_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Netherlands in MW/TWh for water heating in single-family houses
* NO_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Norway with floor heating
* NO_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Norway with radiators
* NO_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Norway
* NO_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Norway with floor heating
* NO_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Norway with radiators
* NO_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Norway
* NO_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Norway with floor heating
* NO_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Norway with radiators
* NO_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Norway
* NO_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Norway in MW/TWh for space heating in commercial buildings
* NO_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Norway in MW/TWh for space heating in multi-family houses
* NO_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Norway in MW/TWh for space heating in single-family houses
* NO_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Norway in MW/TWh for water heating in commercial buildings
* NO_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Norway in MW/TWh for water heating in multi-family houses
* NO_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Norway in MW/TWh for water heating in single-family houses
* PL_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Poland with floor heating
* PL_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Poland with radiators
* PL_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Poland
* PL_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Poland with floor heating
* PL_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Poland with radiators
* PL_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Poland
* PL_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Poland with floor heating
* PL_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Poland with radiators
* PL_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Poland
* PL_heat_demand_space
    - Type: number
    - Description: Heat demand in Poland in MW for space heating
* PL_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Poland in MW for space heating in commercial buildings
* PL_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Poland in MW for space heating in multi-family houses
* PL_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Poland in MW for space heating in single-family houses
* PL_heat_demand_total
    - Type: number
    - Description: Heat demand in Poland in MW for space and water heating
* PL_heat_demand_water
    - Type: number
    - Description: Heat demand in Poland in MW for water heating
* PL_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Poland in MW for water heating in commercial buildings
* PL_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Poland in MW for water heating in multi-family houses
* PL_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Poland in MW for water heating in single-family houses
* PL_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Poland in MW/TWh for space heating in commercial buildings
* PL_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Poland in MW/TWh for space heating in multi-family houses
* PL_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Poland in MW/TWh for space heating in single-family houses
* PL_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Poland in MW/TWh for water heating in commercial buildings
* PL_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Poland in MW/TWh for water heating in multi-family houses
* PL_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Poland in MW/TWh for water heating in single-family houses
* PT_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Portugal with floor heating
* PT_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Portugal with radiators
* PT_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Portugal
* PT_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Portugal with floor heating
* PT_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Portugal with radiators
* PT_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Portugal
* PT_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Portugal with floor heating
* PT_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Portugal with radiators
* PT_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Portugal
* PT_heat_demand_space
    - Type: number
    - Description: Heat demand in Portugal in MW for space heating
* PT_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Portugal in MW for space heating in commercial buildings
* PT_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Portugal in MW for space heating in multi-family houses
* PT_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Portugal in MW for space heating in single-family houses
* PT_heat_demand_total
    - Type: number
    - Description: Heat demand in Portugal in MW for space and water heating
* PT_heat_demand_water
    - Type: number
    - Description: Heat demand in Portugal in MW for water heating
* PT_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Portugal in MW for water heating in commercial buildings
* PT_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Portugal in MW for water heating in multi-family houses
* PT_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Portugal in MW for water heating in single-family houses
* PT_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Portugal in MW/TWh for space heating in commercial buildings
* PT_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Portugal in MW/TWh for space heating in multi-family houses
* PT_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Portugal in MW/TWh for space heating in single-family houses
* PT_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Portugal in MW/TWh for water heating in commercial buildings
* PT_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Portugal in MW/TWh for water heating in multi-family houses
* PT_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Portugal in MW/TWh for water heating in single-family houses
* RO_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Romania with floor heating
* RO_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Romania with radiators
* RO_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Romania
* RO_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Romania with floor heating
* RO_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Romania with radiators
* RO_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Romania
* RO_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Romania with floor heating
* RO_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Romania with radiators
* RO_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Romania
* RO_heat_demand_space
    - Type: number
    - Description: Heat demand in Romania in MW for space heating
* RO_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Romania in MW for space heating in commercial buildings
* RO_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Romania in MW for space heating in multi-family houses
* RO_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Romania in MW for space heating in single-family houses
* RO_heat_demand_total
    - Type: number
    - Description: Heat demand in Romania in MW for space and water heating
* RO_heat_demand_water
    - Type: number
    - Description: Heat demand in Romania in MW for water heating
* RO_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Romania in MW for water heating in commercial buildings
* RO_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Romania in MW for water heating in multi-family houses
* RO_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Romania in MW for water heating in single-family houses
* RO_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Romania in MW/TWh for space heating in commercial buildings
* RO_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Romania in MW/TWh for space heating in multi-family houses
* RO_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Romania in MW/TWh for space heating in single-family houses
* RO_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Romania in MW/TWh for water heating in commercial buildings
* RO_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Romania in MW/TWh for water heating in multi-family houses
* RO_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Romania in MW/TWh for water heating in single-family houses
* SE_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Sweden with floor heating
* SE_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Sweden with radiators
* SE_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Sweden
* SE_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Sweden with floor heating
* SE_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Sweden with radiators
* SE_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Sweden
* SE_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Sweden with floor heating
* SE_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Sweden with radiators
* SE_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Sweden
* SE_heat_demand_space
    - Type: number
    - Description: Heat demand in Sweden in MW for space heating
* SE_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Sweden in MW for space heating in commercial buildings
* SE_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Sweden in MW for space heating in multi-family houses
* SE_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Sweden in MW for space heating in single-family houses
* SE_heat_demand_total
    - Type: number
    - Description: Heat demand in Sweden in MW for space and water heating
* SE_heat_demand_water
    - Type: number
    - Description: Heat demand in Sweden in MW for water heating
* SE_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Sweden in MW for water heating in commercial buildings
* SE_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Sweden in MW for water heating in multi-family houses
* SE_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Sweden in MW for water heating in single-family houses
* SE_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Sweden in MW/TWh for space heating in commercial buildings
* SE_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Sweden in MW/TWh for space heating in multi-family houses
* SE_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Sweden in MW/TWh for space heating in single-family houses
* SE_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Sweden in MW/TWh for water heating in commercial buildings
* SE_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Sweden in MW/TWh for water heating in multi-family houses
* SE_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Sweden in MW/TWh for water heating in single-family houses
* SI_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Slovenia with floor heating
* SI_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Slovenia with radiators
* SI_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Slovenia
* SI_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Slovenia with floor heating
* SI_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Slovenia with radiators
* SI_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Slovenia
* SI_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Slovenia with floor heating
* SI_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Slovenia with radiators
* SI_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Slovenia
* SI_heat_demand_space
    - Type: number
    - Description: Heat demand in Slovenia in MW for space heating
* SI_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Slovenia in MW for space heating in commercial buildings
* SI_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Slovenia in MW for space heating in multi-family houses
* SI_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Slovenia in MW for space heating in single-family houses
* SI_heat_demand_total
    - Type: number
    - Description: Heat demand in Slovenia in MW for space and water heating
* SI_heat_demand_water
    - Type: number
    - Description: Heat demand in Slovenia in MW for water heating
* SI_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Slovenia in MW for water heating in commercial buildings
* SI_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Slovenia in MW for water heating in multi-family houses
* SI_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Slovenia in MW for water heating in single-family houses
* SI_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Slovenia in MW/TWh for space heating in commercial buildings
* SI_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Slovenia in MW/TWh for space heating in multi-family houses
* SI_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Slovenia in MW/TWh for space heating in single-family houses
* SI_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Slovenia in MW/TWh for water heating in commercial buildings
* SI_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Slovenia in MW/TWh for water heating in multi-family houses
* SI_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Slovenia in MW/TWh for water heating in single-family houses
* SK_COP_ASHP_floor
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Slovakia with floor heating
* SK_COP_ASHP_radiator
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for space heating in Slovakia with radiators
* SK_COP_ASHP_water
    - Type: number
    - Description: COP of air-source heat pumps (ASHP) for water heating in Slovakia
* SK_COP_GSHP_floor
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Slovakia with floor heating
* SK_COP_GSHP_radiator
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for space heating in Slovakia with radiators
* SK_COP_GSHP_water
    - Type: number
    - Description: COP of ground-source heat pumps (GSHP) for water heating in Slovakia
* SK_COP_WSHP_floor
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Slovakia with floor heating
* SK_COP_WSHP_radiator
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for space heating in Slovakia with radiators
* SK_COP_WSHP_water
    - Type: number
    - Description: COP of groundwater-source heat pumps (WSHP) for water heating in Slovakia
* SK_heat_demand_space
    - Type: number
    - Description: Heat demand in Slovakia in MW for space heating
* SK_heat_demand_space_COM
    - Type: number
    - Description: Heat demand in Slovakia in MW for space heating in commercial buildings
* SK_heat_demand_space_MFH
    - Type: number
    - Description: Heat demand in Slovakia in MW for space heating in multi-family houses
* SK_heat_demand_space_SFH
    - Type: number
    - Description: Heat demand in Slovakia in MW for space heating in single-family houses
* SK_heat_demand_total
    - Type: number
    - Description: Heat demand in Slovakia in MW for space and water heating
* SK_heat_demand_water
    - Type: number
    - Description: Heat demand in Slovakia in MW for water heating
* SK_heat_demand_water_COM
    - Type: number
    - Description: Heat demand in Slovakia in MW for water heating in commercial buildings
* SK_heat_demand_water_MFH
    - Type: number
    - Description: Heat demand in Slovakia in MW for water heating in multi-family houses
* SK_heat_demand_water_SFH
    - Type: number
    - Description: Heat demand in Slovakia in MW for water heating in single-family houses
* SK_heat_profile_space_COM
    - Type: number
    - Description: Normalized heat demand in Slovakia in MW/TWh for space heating in commercial buildings
* SK_heat_profile_space_MFH
    - Type: number
    - Description: Normalized heat demand in Slovakia in MW/TWh for space heating in multi-family houses
* SK_heat_profile_space_SFH
    - Type: number
    - Description: Normalized heat demand in Slovakia in MW/TWh for space heating in single-family houses
* SK_heat_profile_water_COM
    - Type: number
    - Description: Normalized heat demand in Slovakia in MW/TWh for water heating in commercial buildings
* SK_heat_profile_water_MFH
    - Type: number
    - Description: Normalized heat demand in Slovakia in MW/TWh for water heating in multi-family houses
* SK_heat_profile_water_SFH
    - Type: number
    - Description: Normalized heat demand in Slovakia in MW/TWh for water heating in single-family houses


Feedback
===========================================================================

Thank you for using data provided by Open Power System Data. If you have
any question or feedback, please do not hesitate to contact us.

For this data package, contact:
Oliver Ruhnau <ruhnau@hertie-school.org>

Jarusch Muessel <muessel@hertie-school.org>

For general issues, find our team contact details on our website:
http://www.open-power-system-data.org














