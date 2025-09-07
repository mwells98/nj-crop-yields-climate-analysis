# Climate and Crop Yields in New Jersey (2010–2024)

## Overview
This case study examines how three key field crops in New Jersey (soybeans, corn, and wheat) are influenced by climate variables, focusing on average rainfall and temperature between 2010 and 2024.  

The goal was to determine whether year to year changes in climate influence crop yields, while also building and documenting a data pipeline.

## Objectives
1. Collect and clean fragmented datasets from USDA/NASS (crop yields) and NOAA (precipitation and temperature).  
2. Prepare query ready datasets by standardizing headers and adding missing fields.  
3. Aggregate yearly data across multiple tables using SQL in BigQuery.  
4. Explore and visualize trends in crop yields and climate factors using RStudio and ggplot2.  
5. Interpret whether rainfall or temperature significantly impact yield variability.  

## Data Sources
- **Crop yields**: [USDA National Agricultural Statistics Service (NASS)](https://www.nass.usda.gov/)  
- **Climate data (temperature and precipitation)**: [NOAA National Centers for Environmental Information](https://www.ncei.noaa.gov/)  

## Data Cleaning and Preparation
Key steps in preparing the data included:

- **Google Sheets Script Editor**  
  Wrote a custom script to remove unnecessary header rows from 28 yearly climate datasets.  

- **Header Standardization for BigQuery**  
  Converted column names into BigQuery friendly formats using a custom function in Google Sheets.  

- **Adding Year Columns in BigQuery**  
  Added year fields to precipitation and temperature tables for aggregation across multiple years.  

- **SQL Aggregation**  
  Combined yearly tables into complete precipitation and temperature datasets using `UNION ALL`.  
  Aggregated crop yield values by year and commodity to calculate total bushels per acre.  

## Tools and Technologies
- **Google Sheets** (script editor for bulk cleaning)  
- **BigQuery (SQL)** (aggregation and transformation)  
- **RStudio** (analysis and visualization)  
- **tidyverse, ggplot2, dplyr** (data manipulation and visualization)  

## Analysis and Visualizations
- **Crop Yield Trends**  
  Line charts showing yield patterns for soybeans, corn, and wheat from 2010–2024.  

- **Climate Relationships**  
  Scatter plots examining rainfall and temperature against crop yields.  

- **Year-to-Year Changes**  
  Line charts and bar plots showing annual differences in crop yields and climate variables.  

### Key findings
- Soybeans and wheat showed slight upward associations with warmer years.  
- Corn yields were highly volatile, with extreme values not fully explained by rainfall or temperature.  
- No strong linear correlation was observed between precipitation and yields.  

## Conclusion
This case study demonstrates the ability to manage the full data pipeline from raw collection to final insights.  

Highlights include:  
- Cleaning and transforming over 28 fragmented raw climate files into consistent, query ready tables.  
- Building reproducible workflows across SQL and RStudio.  
- Testing hypotheses with clear visualizations to interpret relationships between variables.  
- Communicating results in a structured way that connects raw data to agricultural context.  

While the hypothesis that rainfall or temperature strongly drive yield variability was not confirmed, the project showcases strong skills in data wrangling, exploratory analysis, and end-to-end project execution.

## Repository Structure
- `raw_data/` – Original datasets from USDA/NASS and NOAA  
- `cleaned_data/` – Processed datasets after cleaning and preparation  
- `notebooks/` – R Markdown files used for analysis and visualization  
- `outputs/` – Final visualizations and reports  
