
# Wildfire Impact Analysis in Grand Fork County

In order to assess the effects of wildfires in Grand Fork County, this research will estimate the effects of smoke over the last 60 years. Data extraction, filtering, smoke estimate, and correlation with Air Quality Index (AQI) data are all part of the analysis. Furthermore, a forecasting model has been created for upcoming smoke projections.

## Introduction

This is an analysis of wildfires and how the smoke from wildfires affects the cities near them. This analysis focuses specifically on Grand Forks, North Dakota. Grand Forks is the third most populous county in the state of North Dakota, USA. This analysis aims to understand how wildfires impact the community health of Grand Forks.

The four sections of the project are as follows.
- Part 1- Pulling data from different sources and calculating the smoke estimate
- Part 2- Creating the Extension Plan to conduct further research
- Part 3- Presenting the results in a presentation
- Part 4- Creating the final report and repository

This project's primary source of inspiration is the increasing frequency with which summers in the western United States have been marked by wildfires that send smoke billowing across many western states. Numerous factors have been suggested as the reason for this, including rising awareness, US Forestry policy, and climate change. Wildland fires have a broad impact, regardless of the cause. Wildfire damage has the potential to seriously affect human settlements as well as the environment. 

## Data Extraction

The US Geological Survey's compiled and aggregated combined wildland fire polygons for the United States and select territories from the 1800s to the present day served as the dataset for this investigation. Python modules and a variety of data processing methods are used in the project to extract and process data.

## Data Sources

The data source is as follows:

- Wildland Fire Combined Dataset by USGS.json: The combined wildland fire datasets for the United States and several territories, 1800s-Present (combined wildland fire polygons) serve as the basis for the common analysis research topic. The US Geological Survey gathered and compiled this dataset. The dataset has a fair amount of documentation. ArcGIS and GeoJSON formats are provided for fire polygons. One US city has been given to each of us, and it will serve as the foundation for our unique research. Our specific US city assignment may be found in this Google spreadsheet.
- A geojson file dataset collected and aggregated by the US Geological Survey. This contains fire polygons for wildfires that have occurred across the USA. The file can be found here: https://www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81
- An API accessing sample notebook to obtain the Air Quality Estimates for regions in the USA: https://drive.google.com/file/d/1bxl9qrb_52RocKNGfbZ5znHVqFDMkUzf/view?usp=sharing
- A spreadsheet listing the assignments of different cities: https://docs.google.com/spreadsheets/d/1cmTW5fgU3KyH6JbrRao-qWjzu2GovKk_BkA7a-poGFw/edit#gid=1247370552
- United States Smoking Prevalence by County 1996-2012: https://ghdx.healthdata.org/record/ihme-data/united-states-smoking-prevalence-county-1996-2012
- United States Chronic Respiratory Disease Mortality Rates by County 1980-2014: https://ghdx.healthdata.org/record/ihme-data/united-states-chronic-respiratory-disease-mortality-rates-county-1980-2014
- About Underlying Cause of Death, 1999-2020: https://wonder.cdc.gov/ucd-icd10.html


## Reproducing the analysis

To reproduce this analysis, follow these steps:

- Step 1: Data Acquisition: Obtain the Wildfire and AQI data by collecting data from the specified sources and making API calls to gather additional information required for analysis.
- Step 2: Data Filtering For Scope: Filter the data acquired in Step 1 to include only wildfires that occurred within a 1250-mile radius from the source city and within the years 1963-2023.
- Step 3: Smoke Estimate Calculation: Calculate the smoke estimate using attributes from the filtered wildfire data.
- Step 4: Time Series Forecasting and Prediction: Utilize time series forecasting techniques to predict smoke levels for future dates in the city of interest based on the smoke estimates from Step 3.
- Step 5: Visualization and Analysis: Perform visualizations and analyses as prompted by the instructor:
  - Create a histogram showing the number of fires at 50-mile intervals up to the specified maximum distance from your assigned city.
  - Generate a time series graph displaying the total acres burned per year for fires within the specified distance from your city.
  - Create a time series graph presenting both the fire smoke estimate and AQI estimate for your city.
  - These steps outline the key phases of Data Acquisition, Data Preparation, and Data Analysis within the project. A much more detailed step-by-step procedure to reproduce this project is given in the notebook attached to this repository.
- Step 6: Reading Hospital data: Read the heallth data from the US government on fatalities, prevenlance of smoking, and growth of respiratory diseases.
- Step 7: Plotting Visualization: Plot the graphs showing the trends in the fatalties, prevalance of smoking, and growth of respiratory diseases in Grand Forks over last several yeats.

## Data Filtering and Preprocessing

By choosing fire perimeters within 1250 miles of Grand Fork County, data filtering and preprocessing make it possible to collect pertinent fire data for analysis.

## Smoke Estimation Process

Based on predetermined parameters, the smoke estimate procedure determines and normalizes the smoke impact of each fire incident. Additional processing and correlation are done using the anticipated smoke effects and the available AQI data.

## Correlation Analysis

In order to understand the link between fire smoke and air quality in Grand Fork County, correlation analysis entails examining the relationship between the estimated smoke impacts and the data from the Air Quality Index.

## Predictive Model

In order to assess possible smoke consequences over the next 25 years, the research uses the Prophet library to create a predictive model for future smoke estimations in Grand Fork County.

## Data Visualization

The data analysis results are graphically displayed using a number of time series graphs and histograms, providing a comprehensive overview of the wildfire's impact on Grand Fork County.

Visualization #1:
The distribution of wildfires according to how close they are to a certain city is shown by this histogram. The y-axis shows the number of wildfires, while the x-axis shows the distance from the city in miles, broken down into 50-mile intervals.
![alt text](/images/fires_vs_distance.png)

Visualization #2:
The total acres burnt by wildfires annually within a given radius of the city are shown in this time series graph. The years are shown on the x-axis, while the total acres burnt by wildfires is shown on the y-axis.
![alt text](/images/acres_burnt.png)

Visualization #3:
The estimated fire smoke impact and the city's estimated Air Quality Index (AQI) trends are shown in this time series graph throughout the years. The years are shown by the x-axis, while the AQI and fire smoke estimates' corresponding values are shown on the y-axis.
![alt text](/images/smoke_vs_aqi_est.png)

## Project Structure

The primary scripts for data processing, analysis, and visualization are all included in the project structure. Additional project-related material and resources are also available in the repository.

## Installation

To install the required dependencies, use the following command:

pip install -r requirements.txt

## Folder Structure

The project folder has the following structure:

- **data**: (accessible at <https://drive.google.com/drive/folders/1BgIZlRqGEbBEj8xnLZHUgkclCsyoTdzk?usp=sharing>) Contains the intermediate and final response files, including:
  - `aqi_by_year.json`: JSON file containing AQI data organized by year.
  - `yearly_smoke_impact.json`: JSON file containing data about yearly smoke impact collected from AQI.
  - `grand_fork_wildfire.json`: JSON file containing wildfire data for Grand Fork County.
  - `normalized_smoke_estimate.json`: JSON file with normalized smoke estimate data.

- **wildfire**: Contains external libraries and custom modules.
- **Notebooks**: Contains the notebooks used in the research, 'wildfire_analysis.ipynb' and 'final_analysis.ipynb'.
- **Report**: Contains the final report of the research.
- **Images**: Contains all the visuzalizations generated as part of the research work.

## Limitations
- The availability of a high-quality dataset: Additional information for the research expansion was sourced from the internet. The data, reported by the North Dakota government, though available, is subject to debate regarding its veracity. The inclusion of a few supplementary data points could potentially enhance the accuracy of the prediction model.
- Accuracy of smoke estimate: The smoke estimate was generated based on the limited information provided in the preceding section. Specifically, the concentrations of several primary air pollutants, each weighted to represent its potential impact on health, form the foundation for the analysis of Air Quality Index (AQI) values. Ground-level ozone (O3), particulate matter (PM10 and PM2.5), carbon monoxide (CO), sulfur dioxide (SO2), and nitrogen dioxide (NO2) are common pollutants considered in the calculation of AQI.
- Unavailability of data: One of the factors that could have contributed to the increase in respiratory diseases is increase in air pollution due to vehicular traffic. However, there was no dataset found in the initial search that could have been used for further analysis.
- Assuming Autocorrelation: Since we are utilizing an autoregressive model to forecast the amount of smoke for the next 25 years, we are making the assumption that the data from earlier time steps will be helpful in forecasting the amount of smoke for the future. This may not be true since a lot of wildfires occur due to accidents and unforeseen natural and manmade conditions.
- Additional elements influencing the healthcare system: In the course of researching wildfire smoke, the focus has been on understanding its contributions to the various consequences discussed in the paper. However, it is important to acknowledge that several additional factors may directly impact the study topics. For example, a general increase in healthcare costs could be a contributing factor to the rise in hospital income, and this is not exclusive to the effects of wildfires.


## Contributing

Contributions to this project are welcome. To contribute, follow these steps:

Fork the repository
Create a new branch
Make your modifications
Commit your changes
Push to the branch
Open a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
