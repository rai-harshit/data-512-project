
# Wildfire Impact Analysis in Grand Fork County

In order to assess the effects of wildfires in Grand Fork County, this research will estimate the effects of smoke over the last 60 years. Data extraction, filtering, smoke estimate, and correlation with Air Quality Index (AQI) data are all part of the analysis. Furthermore, a forecasting model has been created for upcoming smoke projections.

## Introduction

Wildfires are becoming a regular feature of summers in the western United States, causing massive amounts of smoke that affect many facets of civilization. With an emphasis on Grand Fork County's wildfire effect research, this project seeks to shed light on the historical and projected levels of smoke exposure in the city.

## Data Extraction

The US Geological Survey's compiled and aggregated combined wildland fire polygons for the United States and select territories from the 1800s to the present day served as the dataset for this investigation. Python modules and a variety of data processing methods are used in the project to extract and process data.

## Data Sources

The data source is as follows:

Wildland Fire Combined Dataset by USGS.json: The combined wildland fire datasets for the United States and several territories, 1800s-Present (combined wildland fire polygons) serve as the basis for the common analysis research topic. The US Geological Survey gathered and compiled this dataset. The dataset has a fair amount of documentation. ArcGIS and GeoJSON formats are provided for fire polygons. One US city has been given to each of us, and it will serve as the foundation for our unique research. Our specific US city assignment may be found in this Google spreadsheet.

The following example codes, which are available under the Creative Commons CC-BY license, were used as references for the tasks listed below:

An example notebook for computing geodetic distance
An example of how to use the US EPA Air Quality System API code
Code example for the GeoJSON reader

Link: <https://drive.google.com/drive/folders/1OJktGAx86hvMtirCUkGnS292r-FpPvLo>

## Reproducing the analysis

To reproduce this analysis, follow these steps:

1. Make a local copy of this repository.
2. Verify that Python has the necessary libraries installed.
3. After downloading and extracting the "USGS_Wildland_Fire_Combined_Dataset.json" file, locate the data folder within the GeoJSON Files.zip file from this URL.
4. To create smoke analysis, AQI analysis, comparison between them, etc., run wildfire_analysis.ipynb.
5. Examine the outcomes.

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
- **notebooks**: Contains the main project file, 'wildfire_analysis.ipynb'.

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
