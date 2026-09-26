# Data

The dataset (about 1.6 M zone-day rows for the wilaya of Béjaïa, 2009–2022) isn't included in this repository because of its size. It was built from these open sources:

| Data | Source |
|---|---|
| Administrative divisions and population | FAO |
| Land cover and vegetation indices (NDVI, VHI, ASI, precipitation index) | FAO |
| Soil composition (topsoil) | FAO |
| Digital elevation model, slopes | NASA SRTM |
| Daily weather (2009–2022) | Historique Météo |
| Fire history | NASA fire detections (e.g. VIIRS) |

## Schema of the final dataset

| Group | Columns |
|---|---|
| Vegetation | `GRIDCODE`, `LCCCODE` |
| Soil | `sand % topsoil`, `silt % topsoil`, `clay % topsoil`, `pH water topsoil`, `OC % topsoil`, `N % topsoil`, `BS % topsoil`, `CEC topsoil`, `CaCO3 % topsoil`, `BD topsoil`, `C/N topsoil` |
| Human | `Population` |
| Slope | `Moyenne`, `Min`, `Max` |
| Weather | `MAX_TEMPERATURE_C`, `MIN_TEMPERATURE_C`, `WINDSPEED_MAX_KMH`, `HUMIDITY_MAX_PERCENT`, `PRESSURE_MAX_MB`, `HEATINDEX_MAX_C`, `DEWPOINT_MAX_C`, `WINDTEMP_MAX_C`, `TOTAL_SNOW_MM`, `UV_INDEX`, `TEMPERATURE_JOURNEE`, `TEMPERATURE_NIGHT` |
| Vegetation indices | `VHI`, `ASI`, `NDVI`, `IP` |
| Date | `Month`, `Day` |
| Target | `fire` (1 if a fire was detected in the zone within the previous 7 days) |

The notebooks expect `trainset.csv` and `testset.csv` (split before any resampling). Update the Google Drive paths in the notebooks to point to your copy.
