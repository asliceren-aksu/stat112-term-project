# Data dictionary and provenance

The two source Excel workbooks and field descriptions were provided for METU STAT 112. Upstream sources and redistribution licenses are not specified in the supplied materials.

## Preparation for this repository

- Excel values exported to UTF-8 CSV; all source rows retained.
- Dates serialized as ISO timestamps. Currency strings, source fractions, blanks, and country names otherwise retained; these files are not claimed to be fully cleaned data.
- Removed from sales: CUSTOMERNAME, PHONE, ADDRESSLINE1, CITY, POSTALCODE, CONTACTLASTNAME, CONTACTFIRSTNAME. These fields are unnecessary for the documented country-level analysis.
- Sales export: 2,747 rows and 13 columns. Country export: 195 rows and 14 columns.
- This packaging was prepared for GitHub in 2026; the analysis and original report date to 2024.

## autosales-analysis.csv

| Field | Meaning |
|---|---|
| `ORDERNUMBER` | Order identifier; multiple order lines can share an order number. |
| `QUANTITYORDERED` | Number of units on the order line. |
| `PRICEEACH` | Unit selling price. |
| `ORDERLINENUMBER` | Line number within an order. |
| `SALES` | Sales amount recorded for the order line. |
| `ORDERDATE` | Order date (ISO format in this export). |
| `DAYS_SINCE_LASTORDER` | Supplied elapsed-days measure; reference date is not specified. |
| `STATUS` | Order shipping/processing status. |
| `PRODUCTLINE` | Product category. |
| `MSRP` | Manufacturer's suggested retail price; not cost. |
| `PRODUCTCODE` | Product identifier. |
| `COUNTRY` | Customer country; join key. |
| `DEALSIZE` | Small, Medium, or Large deal category. |

## world-indicators-2023.csv

| Field | Meaning |
|---|---|
| `Country` | Country name; join key. |
| `Latitude` | Country latitude. |
| `Longitude` | Country longitude. |
| `Birth Rate` | Births per 1,000 population, per supplied description. |
| `Co2-Emissions` | Country CO₂ emissions; supplied description states tons. |
| `CPI` | Consumer price index. |
| `Gasoline Price` | Gasoline price per liter; currency-formatted source values retained. |
| `GDP` | Gross domestic product; currency-formatted source values retained. |
| `Life expectancy` | Life expectancy at birth, in years. |
| `Population` | Total population count. |
| `Tax revenue (%)` | Tax revenue relative to GDP; source fractions retained. |
| `Total tax rate` | Tax burden relative to commercial profits; source fractions retained. |
| `Unemployment rate` | Unemployment proportion; source fractions retained. |
| `Urban_population` | Urban population count, used with Population to compute a ratio. |

