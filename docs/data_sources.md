
# Data Sources

This document records the datasets used in the Healthcare Operations Intelligence Ireland project, including their origins, coverage, indicators, formats and known limitations.

---

## Source HC02 — HSE Parliamentary Questions 15085/26 and 15086/26

- **Institution:** Health Service Executive (HSE), Ireland
- **Publication date:** 6 March 2026
- **Data period:** January–December 2025
- **Format:** PDF
- **Analysis area:** Home Care Operations
- **Appendix 1:** Number of people waiting for new Home Support packages and additional Home Support hours, by health region and month.
- **Appendix 2:** Direct and indirect Home Support hours delivered, by month, at national level.
- **Geographic coverage:** Regional for waiting lists; national for hours delivered.
- **Known limitations:**
  - The document does not provide regional breakdowns for hours delivered.
  - Waiting list figures do not provide individual waiting times.
  - New packages and additional hours represent different waiting list categories.
- **Document:** HSE Parliamentary Questions PQ 15085/26 and PQ 15086/26.
- **Status:** Source obtained and initial analysis completed.

---

## Source HC03 — CSO Population Estimates (PEA01)

- **Institution:** Central Statistics Office (CSO), Ireland
- **Dataset:** PEA01 — Population Estimates by Age Group, Sex and Year
- **Official URL:** https://data.cso.ie/table/PEA01
- **Analysis area:** Home Care / Demographic Analysis
- **Indicators:** Estimated population by age group
- **Analysis period:** 2020–2025
- **Original extract coverage:** 2020–2026
- **Geographic coverage:** National
- **Format:** CSV
- **Reference date:** April of each year
- **Sex:** Both sexes
- **Original age groups:**
  - 65–69 years
  - 70–74 years
  - 75–79 years
  - 80–84 years
  - 85 years and over
- **Age groups used in the analysis:**
  - 65–74 years
  - 75–84 years
  - 85 years and over
- **Known limitations:**
  - Population estimates for 2023–2025 are preliminary and subject to revision.
  - The original extract includes 2026, which is outside the project's selected analysis period.
  - The age groups used in the analysis require aggregation of the original CSO categories.
- **Raw file:** `data/raw/cso_population_age_2020_2025.csv`
- **Status:** Source identified, CSV downloaded and initial structural inspection completed. Data cleaning and validation are still in progress.

---

## Source HC04 — Eurostat Functional Limitations

- **Institution:** Eurostat, European Commission
- **Dataset:** Health — Self-reported limitations in usual activities due to health problems (GALI).
- **Analysis area:** Home Care / Functional Limitations
- **Analysis period:** 2020–2025
- **Geographic coverage:** Ireland
- **Unit:** Percentage
- **Sex:** Total
- **Urbanisation:** Total
- **Age groups:**
  - 65–74 years
  - 75–84 years
  - 85 years or over
- **Functional limitation categories:**
  - NONE — No activity limitations
  - SOME — Some limitations
  - SEV — Severe limitations
- **Raw file:** `data/raw/eurostat_functional_limitations_2020_2025.csv`
- **Known limitations:**
  - GALI measures self-reported limitations in usual activities; it does not directly measure the need for Home Care or residential care.
  - The exported description field for the NONE category is blank; the category is identified through its code.
  - The 2020 observations contain a break-in-series flag, which requires caution when comparing results over time.
- **Status:** Source obtained, CSV downloaded and initial structural inspection completed. Data cleaning and validation are still in progress.

---

## General Notes

- Original datasets are preserved in `data/raw/`.
- Data cleaning and transformations will be performed separately, without modifying the original files.
- Source-specific limitations must be considered when interpreting results.
- Population estimates and functional limitation percentages measure different aspects of the population and should not be treated as equivalent indicators.