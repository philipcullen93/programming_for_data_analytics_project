# Project: Irish Wind Speed and Energy Potential Analysis

## Project Overview

This project analyses historical Irish weather data from Met Éireann to investigate wind speed patterns and estimate the relative wind energy generation potential at selected weather stations across Ireland. The analysis is carried out using a Jupyter Notebook and focuses on understanding how wind characteristics vary spatially and temporally, with particular relevance to wind farm suitability and green energy generation.

The project demonstrates data acquisition, cleaning, exploratory analysis, visualisation, and applied interpretation.

## Objectives

1. Load and clean historical weather data from Met Éireann

2.  Explore wind speed distributions across multiple Irish weather stations

3. Analyse daily and long-term wind speed trends

4. Estimate relative wind energy generation using a simplified physical model

5. Compare stations to assess suitability for wind energy generation

## Data Source

Provider: Met Éireann – The Irish Meteorological Service

Dataset: Historical Weather Observations (CSV files)

Stations Used:

- Malin Head

- Valentia Observatory

- Dublin Airport

- Mullingar

The raw data files were downloaded manually from the Met Éireann website and stored locally in the data/ directory.

## Project Structure

├── data/

│ ├── malin_head.csv

│ ├── valentia.csv

│ ├── dublin_airport.csv

│ └── mullingar.csv

│

├── wind_energy_analysis.ipynb

├── README.md

## How to Run the Project

1. Clone the repository

2. Ensure Python 3 and the following packages are installed:

  - pandas

  - numpy

  - matplotlib

3. Open wind_energy_analysis.ipynb in Jupyter Notebook

4. Run all cells from top to bottom

## Methodology
### 1. Data Loading and Inspection

- CSV files were read using pandas

- Header rows were handled explicitly due to non-standard formatting

- Initial inspection was performed using .head(), .info(), and missing value checks

### 2. Data Cleaning and Preparation

- Column names were standardised

- Date columns were parsed and converted to datetime format

- Wind speed (wdsp) values were converted to numeric format

- Datasets from multiple stations were combined into a single DataFrame

### 3. Exploratory Wind Speed Analysis

- Summary statistics and distributions of wind speed were examined

- Histograms and boxplots were used to compare stations

- Daily average wind speeds were calculated and visualised over time

### 4. Estimated Wind Energy Potential

- A simplified energy proxy proportional to the cube of wind speed was used:

  - Energy ∝ wind_speed³

- Daily estimated energy generation was calculated for each station

- Time series plots were used to visualise daily and rolling-average energy output

- Long-term energy generation was aggregated to compare stations

### 5. Visualisation

- All plots use consistent station-specific colours

- Line plots, histograms, and bar charts were employed

- Visualisations prioritise clarity and readability

## Key Findings

- Coastal stations (Malin Head and Valentia) exhibit consistently higher wind speeds

- Inland stations (Mullingar) show lower wind speeds and reduced energy potential

- Dublin Airport and Valentia display similar wind patterns, likely due to coastal exposure and prevailing Atlantic winds

- Estimated energy generation is highly variable due to the cubic relationship with wind speed

- Long-term aggregation highlights coastal locations as significantly more suitable for wind energy generation

## Limitations

The energy model used is a simplified proxy and does not account for:

- Turbine cut-in or cut-out speeds

- Turbine efficiency or rated capacity

- Actual wind farm locations or sizes

As a result, energy values are relative rather than absolute.

## Conclusion

This project demonstrates the use of real-world meteorological data to perform applied data analysis with relevance to renewable energy. Through systematic cleaning, exploration, and modelling, it provides insight into how wind resources vary across Ireland and highlights the importance of location in wind energy generation.
