# Weather Project

Seattle vs. Vancouver: A Statistical Comparison of Precipitation by Season and Month

---

## Project Overview


- **Objective:** To figure out which city rains more between Seattle and Vancouver
- **Domain:** Climate
- **Key Techniques:** t-test, z-test

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** (https://www.noaa.gov/)
- **Description:** seattle_weather.csv : weather data of Seattle during 2018.01.01 ~ 2022.12.31
van.csv : weather data of Vancouver during 2018.01.01 ~ 2022.12.31
clean_seattle_vancouver_weather.csv : precipitation data of Seattle and Vancouver during 2018.01.01 ~ 2022.12.31 after data wrangling.

---

## Analysis

To clean the data, we used one station for each city:  Seattle (station: USW00094290) and Vancouver (station: CA001108395). Since the DATE column was stored as a string, we converted it to datetime format. We then selected the PRCP column and organized the data into a tidy format. Because there were some missing values, we replaced them with the mean precipitation for the same calendar day across the other years.
After wrangling the data, we conducted exploratory data analysis (EDA) and tested our hypotheses using t-tests and two-proportion z-tests.

To reproduce the results, the code should be run in the following order: first, load the data and select the stations; second, convert the DATE column to datetime format and select the PRCP data; third, reshape the data into a tidy format; fourth, identify and replace missing values; and finally, create the variables, perform the statistical analyses and hypothesis tests, and generate the visualizations.

---

## Results

Seattle received significantly less mean precipitation than Vancouver, but the proportion of rainy days did not differ significantly. Because the frequency of rain is similar while the mean precipitation is lower, this might suggest that Seattle receives less precipitation on the days when it rains

---

## Authors

- Jisoo Ahn - [@jisoo-ahn](https://github.com/jisoo-ahn)

---

## Acknowledgements

- Tools/libraries used : Pandas, Numpy, Matplotlib, Scipy, Calendar, Seaborn
- Tutorials or papers referenced : Course materials from DATA 5100, Fall Quarter 2026, Seattle University
