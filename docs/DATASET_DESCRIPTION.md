## 📘 Dataset Description: Demographic and Socioeconomic Data for Population Forecasting Models

### 1. Overview
This dataset compiles harmonized demographic and socioeconomic time-series data for three countries (see repository README for details), intended for use in population projection, demographic modeling, and forecasting research.  
It integrates official demographic statistics with macro-economic indicators to provide a unified foundation for evaluating cohort-component and regression-based forecasting models.

### 2. Data Sources
| Source | Description | URL |
|:--|:--|:--|
| **National Statistical Offices** | Official demographic series (population by age and sex, births, deaths, international migration). Each country’s data were extracted directly from its official statistical portal. | Country-specific links provided in `/sources.md`. |
| **World Bank Open Data** | Macroeconomic indicators including GDP per capita (constant 2015 USD), health expenditure (% of GDP), and unemployment rate (% of labor force). | https://data.worldbank.org |

All data were accessed between May and June of 2025 and cleaned using reproducible scripts available upon request.

### 3. Structure and Variables

Each row corresponds to a unique `(Country, Year, Age, Sex)` combination.  
The dataset is provided in CSV format (`data/[Country]_Processed_With_Predictors.csv`) with the following columns:

| Column | Type | Description |
|:--|:--|:--|
| **Year** | integer | Calendar year of observation. |
| **Age** | integer | Age group (in years). |
| **Sex** | categorical | Biological sex (`Male`, `Female`). |
| **Immigrations** | numeric | Number of immigrants entering the country in that year and age–sex group. |
| **Emigrations** | numeric | Number of emigrants leaving the country. |
| **Migration_balance** | numeric | Net migration = Immigrations − Emigrations. |
| **MaleBirths** | numeric | Number of male live births to mothers of the given age group. |
| **FemaleBirths** | numeric | Number of female live births to mothers of the given age group. |
| **TotalBirths** | numeric | Total births = MaleBirths + FemaleBirths. |
| **Deaths** | numeric | Number of deaths in the given age–sex group and year. |
| **Population** | numeric | Mid-year population estimate for the age–sex group. |
| **GDP_per_capita** | numeric | Gross domestic product per capita (constant 2015 USD). |
| **Health_expenditure_pct_GDP** | numeric | Health expenditure as a percentage of GDP. |
| **Unemployment** | numeric | Unemployment rate (% of labor force). |

### 4. Units and Coverage
- **Geographical scope:** *[Country A]*, *[Country B]*, *[Country C]* 
- **Time coverage:** Country dependent. Germany: 2001-2023; Norway: 2001-2024; Portugal: 2008-2023.
- **Age coverage:** Country dependent. Germany: 0-100+; Norway: 0-80+ in groups of 5 years; Portugal: 0-85+ in groups of 10 years.


### 5. Licensing and Citation
This dataset is released under the **Creative Commons Attribution 4.0 International (CC-BY 4.0)** license.  
When using the dataset, please cite as:

> Politis M., Christakis N, Pana Z. D. nad Drikakis D.* (2025). **Demographic and Socioeconomic Dataset for Population Forecasting Models**. Version 1.0. Available at: https://github.com/nchrkis/demographic-forecast-data

### 6. Suggested Citation for Derived Works
If used in academic research, cite both this repository and the accompanying paper:
> *Politis*, *et al.* (2025). *Integrating  Machine Learning and Scenario Modelling for Robust Population Forecasting Under Crisis and Data Scarcity* *submitted to Mathematics.*

### 7. Contact
For correspondence or data issues:
```
Nicholas Christakis
Institute for Advanced Modelling and Simulation, University of Nicosia, Cyprus
Email: nchrkis@gmail.com
GitHub: @nchrkis
```
