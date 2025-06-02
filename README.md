<p align="center">
  <img src="https://images.ctfassets.net/p6ae3zqfb1e3/2l8ZrEyDeCq8F6oBvda0WP/f92c98aa4dd42818ab413f193945777b/CaBi_Homepage_Hero_2x.png?w=2500&q=60&fm=webp" alt="Bikesharing Project Banner" width="800"/>
</p>

# Bikesharing Project

## Overview

This project analyzes bikesharing data from Washington, D.C., focusing on usage patterns, weather impacts, and demographic influences. The goal is to derive insights that can inform strategies to enhance the efficiency and accessibility of bikesharing services in the city.

## Datasets

The project utilizes the following datasets:

- `CBS_2021-2023_Daily_Weather.csv`: Daily weather observations in Washington, D.C. from 2021 to 2023.
- `CBS_2021-2023_Hourly_Weather.csv`: Hourly weather data for the same time period.
- `CBS_2021-2023_Full.csv`: Main dataset containing detailed trip data including timestamps, start/end stations, geocoordinates, and user types. *(not included in the repository)*.
- `demographic_characteristics_wards.csv`: Demographic information by ward 
- `economic_characteristics_dc_wards.csv`: Economic indicators by ward.
- `wards_from_2022.geojson`: GeoJSON file with ward boundaries for Washington, D.C.
- `bicycle_lanes_dc.geojson`: GeoJSON file showing the bicycle lane network across the city.

## Project Structure

```
├── data/
│   ├── CBS_2021-2023_Daily_Weather.csv
│   ├── CBS_2021-2023_Hourly_Weather.csv
│   ├── CBS_2021-2023_Full.csv # Not included 
│   ├── demographic_characteristics_wards.csv  
│   ├── economic_characteristics_dc_wards.csv
│   ├── wards_from_2022.geojson
│   └── bicycle_lanes_dc.geojson
├── notebooks/
│   ├── bike_project_2021_EDA.ipynb
│   ├── bike_project_2022_EDA.ipynb
│   ├── bike_project_2023_EDA.ipynb
│   ├── bike_project_ML_linear_poly_W2.ipynb
│   └── bike_project_ML_linear_poly_W7.ipynb
├── .gitignore
└── README.md
```

## Analysis and Methodology

The project includes the following analytical components:

- **Exploratory Data Analysis (EDA)**: Investigated temporal patterns (seasonality, daily peaks), the impact of weather conditions on ridership, and general user trends.
- **Ward-Level Comparison**: Focused analysis on **Ward 2** and **Ward 7**, which display opposite usage patterns:
  - **Ward 2** has high bikesharing usage, dense station coverage, and extensive bike lanes.
  - **Ward 7** has low bikesharing usage, fewer stations, and limited bike infrastructure.
  - To understand this disparity, the analysis explores not only infrastructure but also **demographic and economic differences** between the wards.
- **Geospatial Analysis**: Used `folium` and `geopandas` to map trip flows, station density, and bike lane coverage by ward.
- **Machine Learning Models**: Applied linear and polynomial regression models to predict ridership levels using weather and time-based features.

## Getting Started

### Prerequisites

Make sure you have the following installed:

- Python 3.7 or higher
- Jupyter Notebook
- Required Python libraries:
  - pandas  
  - numpy  
  - matplotlib  
  - seaborn  
  - scikit-learn  
  - folium  
  - geopandas  

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Jul-9579/Bikesharing-Project.git
   cd Bikesharing-Project
   ```

2. Create a virtual environment and activate it:

   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. Install the required libraries:

   ```bash
   pip install -r requirements.txt
   ```

   *Note: If `requirements.txt` is not included, generate it with:*

   ```bash
   pip freeze > requirements.txt
   ```

4. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

   Open any notebook from the `notebooks/` directory to begin exploring.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your enhancements.

## License

This project is licensed under the MIT License.
