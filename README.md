# CO2 Emission by Countries Analysis

## Project Title and Overview
This project performs an exploratory data analysis (EDA) on CO2 emissions by countries, spanning from 1750 to 2020. The primary goal is to understand global CO2 emission trends, identify major contributing countries, and analyze specific country-level patterns. The dataset used is `CO2 emission by countries.csv`, which contains historical CO2 emission data along with country-specific information.

## Goals
*   To load and clean the CO2 emission dataset.
*   To generate comprehensive data profiles for both raw and cleaned data.
*   To identify and visualize the top CO2 emitting countries.
*   To analyze the overall yearly trend of CO2 emissions.
*   To examine the CO2 emission trends and ranking for a specific country (e.g., United States) over time.
*   To detect outliers in the CO2 emission data.

## Methodology
The analysis involved the following steps:
1.  **Data Loading:** The `CO2 emission by countries.csv` dataset was loaded into a pandas DataFrame using `pd.read_csv`, with `latin1` encoding to handle potential character issues.
2.  **Initial Data Profiling:** `ydata-profiling` was used to generate a detailed report of the raw data (`CO2_emission_by_countries_raw_report.html`), providing insights into data types, missing values, and initial distributions.
3.  **Data Cleaning and Preprocessing:**
    *   Filtered the dataset to include only records where 'CO2 emission (Tons)' is greater than 0, as zero values likely represent missing data or periods before significant industrialization.
    *   Selected relevant columns: 'Country', 'Year', and 'CO2 emission (Tons)'.
    *   Checked for missing values in the cleaned dataset.
4.  **Cleaned Data Profiling:** Another `ydata-profiling` report (`cleanedco2_profile.html`) was generated for the cleaned data to reflect the changes after preprocessing.
5.  **Descriptive Analysis:** Basic descriptive statistics were computed for the cleaned CO2 emission data.
6.  **Outlier Detection:** The Interquartile Range (IQR) method was applied to identify potential outliers in the 'CO2 emission (Tons)' column.
7.  **Visualizations:**
    *   A bar chart was created to display the top 10 CO2 emitting countries based on their total emissions.
    *   A line plot showed the overall yearly trend of CO2 emissions globally.
    *   A line plot specifically for the United States was generated to visualize its CO2 emission trend over time.
    *   The ranking of the United States in terms of CO2 emissions for each year was analyzed.

## Key Findings/Results
*   **Top Emitters:** The analysis identified countries like the United States, United Kingdom, and Germany as historically high CO2 emitters.
*   **Yearly Trend:** Global CO2 emissions have shown a significant increasing trend over the centuries, with a particularly sharp rise in recent decades.
*   **United States Emissions:** The United States' CO2 emissions generally increased over time, often holding a top rank, especially in earlier periods.
*   **Outliers:** A substantial number of data points were identified as outliers based on the IQR method. Further investigation revealed that countries like the United Kingdom, United States, Germany, France, and Belgium frequently appear as outliers, indicating their consistently high CO2 emissions over many years (from 1820 up to 2020). These outliers are not necessarily errors but rather reflect the exceptionally high emission levels of these industrialized nations.

## Technologies Used
*   **Python**
*   **pandas:** For data manipulation and analysis.
*   **ydata-profiling:** For comprehensive exploratory data analysis and reporting.
*   **seaborn:** For statistical data visualization.
*   **matplotlib:** For creating static, interactive, and animated visualizations.

## How to Run
1.  Ensure you have Python installed with `pandas`, `ydata-profiling`, `seaborn`, and `matplotlib` libraries.
2.  Download the `CO2 emission by countries.csv` dataset and place it in the same directory as the notebook, or upload it to your Colab environment.
3.  Run all cells in the Jupyter/Colab notebook sequentially.
    *   *Note:* The `!pip install ydata-profiling` command is included in the notebook to install the required profiling library.

## Next Steps/Future Work
*   Investigate the causes behind the identified outliers in CO2 emissions.
*   Perform more in-depth time series analysis to forecast future emission trends.
*   Analyze the correlation between CO2 emissions and other factors like GDP, industrialization, and population growth.
*   Explore the impact of major historical events or policies on CO2 emission patterns.
*   Build predictive models for CO2 emissions based on various features.

## Resources
*   Dataset: [CO2 Emission by Countries (Year-Wise 1750-2022) on Kaggle](https://www.kaggle.com/datasets/moazzimalibhatti/co2-emission-by-countries-year-wise-17502022)
