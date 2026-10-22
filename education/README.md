

# Education Project

- Predicting School-Level ACT Scores Using Socioeconomic Factors: A Regression Analysis

---

## Project Overview


- **Objective:**
-  This study investigates whether socioeconomic variables improve the prediction of school-level ACT scores beyond a baseline model using the percentage of students eligible for free or reduced-price lunch. Three datasets from EdGap, the National Center for Education Statistics (NCES), and Zillow were combined, resulting in 7,227 high schools after data cleaning and imputation. Five socioeconomic variables were evaluated using linear, logarithmic, and quadratic functional forms, with model performance assessed using R² and mean absolute error (MAE). Among the initial extended models, the percentage of adults with a college degree achieved the best performance (R² = 0.6332, MAE = 1.1245). Adding a quadratic term increased R² to 0.6407, while MAE remained unchanged. These results suggest that socioeconomic variables, particularly adult college attainment, can improve the explanation of variation in school-level ACT scores. However, geographic limitations and imputed housing prices may affect the generalizability of the findings.
  
- **Domain:** 
- Previous studies have examined the relationship between socioeconomic conditions and academic achievement. Research on the Community Eligibility Provision (CEP), a program that provides free meals to eligible schools, has found positive effects on student outcomes. For example, Gordanier et al. (2020), in Free Lunch for All!, found that CEP was associated with an approximately 0.06 standard deviation increase in mathematics test scores among elementary school students. However, the existing literature often focuses on specific programs or geographic areas, leaving room to investigate the predictive value of a broader range of socioeconomic characteristics across multiple states.
This study examines whether incorporating additional socioeconomic variables improves the prediction of school-level ACT scores beyond a baseline model using the percentage of students eligible for free or reduced-price lunch. Specifically, five variables are considered: unemployment rate, housing price, household income, the percentage of children living in married-couple families, and the percentage of adults with a college degree. The central research question is whether these additional socioeconomic variables improve the predictive performance of the baseline model.


- **Key Techniques:**
regression analysis

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

- **Source:**
- EdGap, https://www.edgap.org/#4/37.68/-95.98
- National Center for Education Statistics, https://nces.ed.gov/ccd/pubschuniv.asp
- Zillow, https://www.zillow.com/research/data/

- **Description:**

- Three datasets are used in this project. The first is the EdGap dataset (EdGap) from EdGap.org. It includes average ACT scores for schools, using SAT-based scores where ACT scores were unavailable, and several socioeconomic characteristics of the school district from 2016. Key variables include unemployment rate, adults with a college degree, children in married-couple families, percentage of students at the school eligible for free or reduced-price lunch, and household income. The second dataset provides school-level information (School Info) from the National Center for Education Statistics (NCES). It includes basic school information such as address, school type, school level, and charter school indicator. The last dataset is housing price data containing monthly housing prices by ZIP code from Zillow.

---

## Analysis
- First, a baseline regression model is constructed using the percentage of students eligible for free or reduced-price lunch to predict school-level ACT scores. Next, five additional socioeconomic variables are evaluated using three functional forms: linear, logarithmic, and quadratic. For each variable, the functional form with the best performance is selected based on the model evaluation results.
- Each selected variable is then added individually to the baseline model to construct an extended model. The baseline and extended models are evaluated using theR^2 and MAE. An extended model is considered to improve predictive performance only if it achieves both a higher R^2 and a lower MAE than the baseline model. If only one metric improves, the extended model is not considered better under this criterion.
- Next, scatter plots and regression curves are examined to visualize the relationships between the socioeconomic variables and ACT scores and to identify potential opportunities for model improvement. Based on these visual observations, additional model specifications are developed and evaluated. The resulting models are compared using R^2 and MAE, and the model that demonstrates the best performance under the evaluation criteria is selected as the final model.

---

## Results

- This study examined whether socioeconomic variables improve the prediction of school-level ACT scores beyond a baseline model using the percentage of students eligible for free or reduced-price lunch (FRPL). Among the five additional variables evaluated, the percentage of adults with a college degree achieved the best performance in the initial extended models. Adding a quadratic term for this variable further increased R² from 0.6332 to 0.6407, while MAE remained at 1.1245. Compared with the baseline model (R² = 0.6230, MAE = 1.1598), the final model explained more variation in ACT scores and reduced prediction error.


---

## Authors

- Jisoo Ahn - [@jisoo-ahn](https://github.com/jisoo-ahn)


---

## Acknowledgements

- Tools/libraries used : Pandas, Numpy, Matplotlib, Scipy, Calendar, Seaborn
- Tutorials or papers referenced : Course materials from DATA 5100, Fall Quarter 2026, Seattle University
