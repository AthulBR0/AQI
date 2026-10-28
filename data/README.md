# Air quality dataset

`city_day.csv` contains daily city-level air-quality observations for 26 Indian cities, from 1 January 2015 through 1 July 2020. The file includes pollutant concentrations, AQI, and AQI category.

## Source and credit

- Original dataset: [Air Quality Data in India (2015–2020)](https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india), compiled from CPCB records.
- This project uses the `city_day.csv` file from the [Hugging Face mirror](https://huggingface.co/datasets/AdityaaXD/AQI-Of-India).
- The TUMI Data Portal catalog for this dataset reports a CC0 1.0 license: [dataset record](https://portal.transport-data.org/@tumi/urban-air-pollution-india-2015-2020).

## How the app uses it

The app keeps `City`, `Date`, PM2.5, PM10, NO2, SO2, CO, O3, AQI, and AQI_Bucket. It excludes rows missing the date, city, any of those six pollutant values, or AQI. If AQI_Bucket is missing or outside the app's category labels, the app derives a category from AQI breakpoints.

This is historical, city-aggregated data; it is not a live feed and does not represent individual monitoring stations. Credit the original dataset and CPCB in project reports.