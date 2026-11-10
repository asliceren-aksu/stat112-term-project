# Auto Sales & Economic Indicators — STAT 112 Term Project

**Tableau dashboard · Exploratory data analysis · METU STAT 112 · 2024**

An exploratory study of sales patterns across product lines and countries, combining transaction records with demographic and economic indicators. Created by **Aslı Ceren Aksu** for *Introduction to Data Processing and Visualization* at Middle East Technical University.

**[Explore the interactive dashboard →](https://public.tableau.com/app/profile/asl.ceren.aksu/viz/Book1_17336894255420/Dashboard1)** · **[Download the original report](STAT112-Original-Report-2024.docx)**

## Project at a glance

| | Details |
|---|---|
| Tools | Tableau, Excel source files |
| Sales dataset | 2,747 records; 20 original fields |
| Country dataset | 195 countries; 14 fields |
| Analysis | Country-level join, calculated fields, descriptive comparisons, interactive visualization |
| Completed | December 2024 |

## Questions explored

1. How are sales distributed across product lines and shipping statuses?
2. How do country-level CO₂ emissions relate to sales and MSRP?
3. How do sales compare across countries selling above or below MSRP?
4. How do sales vary across product lines and urbanization categories?
5. How do GDP per capita and MSRP vary across countries?

## What I worked on

- Combined the two datasets using country as the join key.
- Reviewed missing values and field types, including currency-formatted indicators.
- Created calculated fields for GDP per capita, urbanization ratio, and country-level average price differences relative to MSRP.
- Built treemaps, bubble charts, and stacked bars, then brought them together in an interactive dashboard with shipping-status filters.
- Documented the workflow and interpretation in a written report.

## Selected observations

The original analysis identifies Classic Cars as the largest product line by total sales. Sales composition differs across urbanization groups, while the country comparisons explore how pricing and economic indicators vary together. These are descriptive observations from the supplied sample, not estimates of the global automobile market.

## Read the results with these limitations

- **Different time periods:** the sales records cover 2018–2020, while the country dataset is labeled 2023. The combined views are exploratory and do not establish time-aligned relationships or causation.
- **MSRP is not cost:** the original dashboard uses “profit” and “loss” for prices above and below MSRP. These labels describe a price difference, not accounting profit or loss.
- **Aggregation matters:** country indicators are repeated after joining to transaction rows. Use an appropriate country-level aggregation rather than summing repeated GDP or population values.
- **Outlier handling:** the original CO₂ chart excludes the USA for readability. Conclusions from that chart therefore do not describe the full sample.
- **Original coursework:** the report and live dashboard preserve the 2024 submission. Some wording and interpretations are preliminary; no formal significance tests or causal models are presented.

## Repository contents

| File | Purpose |
|---|---|
| [STAT112-Original-Report-2024.docx](STAT112-Original-Report-2024.docx) | Original coursework report |
| [autosales-analysis.csv](autosales-analysis.csv) | Sales data with unnecessary customer contact/location fields removed |
| [world-indicators-2023.csv](world-indicators-2023.csv) | Country indicator data exported from the supplied workbook |
| [DATA_DICTIONARY.md](DATA_DICTIONARY.md) | Field definitions, preparation notes, and source attribution |
| [TABLEAU_CALCULATIONS.md](TABLEAU_CALCULATIONS.md) | Documented calculations and interpretation notes |

## Explore or rebuild

1. Open the **[live dashboard](https://public.tableau.com/app/profile/asl.ceren.aksu/viz/Book1_17336894255420/Dashboard1)** to explore the published analysis without installing Tableau.
2. To build your own version, connect Tableau to the two CSV files in this repository. Parse `ORDERDATE` as a date and check numeric fields containing currency symbols or separators.
3. Inspect country names before joining `COUNTRY` to `Country`; document any name mappings and unmatched countries. The original report describes 19 matched countries.
4. Recreate the fields in [TABLEAU_CALCULATIONS.md](TABLEAU_CALCULATIONS.md), then build the views above. The CSVs support rebuilding; they are not a packaged Tableau workbook or a byte-for-byte export of the published dashboard's extract.

## Data provenance

The source spreadsheets were supplied for METU STAT 112 coursework as `autosale.xlsx` and `world-data-2023.xlsx`, with a course data-description document. The supplied materials do not identify an upstream publisher or license. No new license is assigned to third-party data in this repository. See [data notes](DATA_DICTIONARY.md) for the exact changes made to the shared copies.

---

**Aslı Ceren Aksu** · [LinkedIn](https://www.linkedin.com/in/aslicerenaksu/) · [GitHub](https://github.com/asliceren-aksu)
