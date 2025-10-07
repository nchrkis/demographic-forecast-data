## 📚 Data Sources and Provenance

This document lists the original sources used to construct the dataset.  
All data were collected from official or publicly accessible databases between May and June of 2025 and cleaned using scripts available upon request.
Where possible, direct URLs to data portals and metadata pages are included.

---

### 🧭 1. Country Statistical Services

| Country | Statistical Office | Data Used | Access URL | Accessed |
|:--|:--|:--|:--|:--|
| **Germany** | Statistisches Bundesamt (Destatis) | Population by age and sex, births, deaths, international migration | https://www.destatis.de | *March 2025* |
| **Norway** | Statistics Norway (SSB) | Population by age and sex, births, deaths, international migration | https://www.ssb.no | *March 2025* |
| **Portugal** | Instituto Nacional de Estatística (INE) | Population by age and sex, births, deaths, international migration | https://www.ine.pt | *March 2025* |

---

### 🌍 2. World Bank Open Data

| Indicator | Code | Description | URL | Transformation |
|:--|:--|:--|:--|:--|
| **GDP per capita (constant 2015 US$)** | NY.GDP.PCAP.KD | Gross domestic product per person in 2015 constant USD | https://data.worldbank.org/indicator/NY.GDP.PCAP.KD | Direct use |
| **Health expenditure (% of GDP)** | SH.XPD.CHEX.GD.ZS | Current health expenditure as a percentage of GDP | https://data.worldbank.org/indicator/SH.XPD.CHEX.GD.ZS | Direct use |
| **Unemployment rate (% of total labor force)** | SL.UEM.TOTL.ZS | Modeled ILO estimate of unemployment | https://data.worldbank.org/indicator/SL.UEM.TOTL.ZS | Linearly interpolated to fill missing years |

---

### 🧩 3. Harmonization Notes

- All series were aligned by calendar year and merged on `Country`, `Year`, `Age`, and `Sex`.  
- For comparability, populations refer to mid-year estimates; fertility and mortality rates are based on annual occurrences.  
- Macroeconomic indicators were appended at the country-year level and broadcast across age/sex strata.

---

### 🧾 4. Citation of Sources

If redistributing or publishing analyses derived from this dataset, please cite both:
1. Each national statistical office (as primary data producers); and  
2. The World Bank Open Data platform as secondary socioeconomic data provider.

Example citation:
> Destatis (2025), *Population by age and sex, Germany 1970–2024*, Statistisches Bundesamt, Wiesbaden.  
> World Bank (2025), *World Development Indicators*, Washington, D.C.

---

### 🧠 5. Version Control

| Version | Date | Description |
|:--|:--|:--|
| **v1.0** | October 2025 | Initial release: three-country harmonized demographic–socioeconomic dataset. |