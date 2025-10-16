# demographic-forecast-data
# 📊 Demographic and Socioeconomic Dataset for Population Forecasting Models

## 📘 Overview
This repository provides a harmonized demographic–socioeconomic dataset covering **Germany**, **Norway**, and **Portugal**, intended for **population projection, demographic modeling, and machine learning–based forecasting**.  
It integrates official demographic statistics (population, births, deaths, migration) with macroeconomic indicators (GDP, health expenditure, unemployment) to support robust population forecasting under diverse conditions.

---

## 🧭 Data Sources
All data were collected from **official or publicly accessible databases** between **May–June 2025**.

| Source | Description | URL |
|:--|:--|:--|
| **National Statistical Offices** | Population by age and sex, births, deaths, international migration. | Country-specific portals (see `/sources.md`). |
| **World Bank Open Data** | GDP per capita, health expenditure, and unemployment rate indicators. | [https://data.worldbank.org](https://data.worldbank.org) |

For details and citations, see [`sources.md`](./sources.md).

---

## 🧾 Dataset Structure
Each record corresponds to a unique `(Country, Year, Age, Sex)` combination.

| Column | Description |
|:--|:--|
| **Year** | Calendar year of observation |
| **Age** | Age group (in years) |
| **Sex** | `Male` or `Female` |
| **Population** | Mid-year population estimate |
| **Births / Deaths / Migration** | Demographic flows by age–sex group |
| **GDP_per_capita** | Constant 2015 USD |
| **Health_expenditure_pct_GDP** | % of GDP |
| **Unemployment** | % of total labor force |

Data are provided as CSV files:  
`data/[Country]_Processed_With_Predictors.csv`

---

## 🌍 Coverage
- **Countries:** Germany, Norway, Portugal  
- **Time:** Germany (2001–2023), Norway (2001–2024), Portugal (2008–2023)  
- **Age:** Country dependent (0–80+ to 0–100+)  

---

## 📄 License & Citation
Released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.

**Cite as:**
> Politis M., Christakis N., Pana Z. D., and Drikakis D. (2025).  
> *Demographic and Socioeconomic Dataset for Population Forecasting Models*, v1.0.  
> [https://github.com/nchrkis/demographic-forecast-data](https://github.com/nchrkis/demographic-forecast-data)

For derived research:
> Politis *et al.* (2025). *Integrating Machine Learning and Scenario Modelling for Robust Population Forecasting Under Crisis and Data Scarcity.* *Submitted to Mathematics.*

---

## 📬 Contact
```
Nicholas Christakis
Institute for Advanced Modelling and Simulation, University of Nicosia, Cyprus
Email: nchrkis@gmail.com
GitHub: @nchrkis
```
