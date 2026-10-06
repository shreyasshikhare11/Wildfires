# Wildfires

This repository contains a Google Earth Engine (GEE) workflow for analyzing wildfire risk and behavior in a selected country. The script combines weather reanalysis, satellite fire detections, and land-cover information to estimate wildfire generation classes and highlight areas with elevated fire propagation potential.

## What the script does

- Defines a target year and country (currently set to Greece)
- Loads country boundaries and land-cover data
- Pulls daily ERA5-Land weather data for the selected fire season
- Calculates wildfire risk indicators such as dynamic ISI and FWI values
- Loads VIIRS thermal hotspot data from NASA
- Matches fire detections with weather conditions to estimate behavioral fire generation classes
- Produces a maximum fire-generation map and summary charts
- Displays a map layer and legend in the Google Earth Engine interface

## Key datasets used

- Country boundary: USDA/LSIB_SIMPLE
- Land cover: ESA WorldCover
- Weather: ECMWF/ERA5_LAND/DAILY_AGGR
- Fire detections: NASA/LANCE/SNPP_VIIRS/C2

## Fire generation classes

The script assigns wildfire classes from 1 to 6:

- 1: Surface-driven spread with minimal intensity
- 2: Increased fuel load intensity
- 3: High-speed linear fire fronts influenced by wind
- 4: Wildland-urban interface (WUI) activity
- 5: Multi-front stress conditions and elevated operational pressure
- 6: Extreme radiant heat and severe fire behavior

## How to use

1. Open the Google Earth Engine Code Editor.
2. Paste the contents of the `GEE code` file into a new script.
3. Update the variables as needed:
   - `targetYear`
   - `countryName`
   - `startDate`
   - `endDate`
4. Run the script to generate the wildfire risk map and charts.

## Notes

- The example is configured for Greece during the 2026 fire season.
- This workflow is intended for exploratory wildfire monitoring and risk visualization.
- It is best suited for geospatial analysis and situational awareness, not formal fire spread prediction.

## Repository purpose

This project demonstrates how Earth Engine tools can be used to assess wildfire risk using meteorological and satellite data. 