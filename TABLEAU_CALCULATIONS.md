# Tableau calculations

These formulas document the approach described in the December 2024 report. Field labels in Tableau may differ from the CSV headers.

## GDP per capita

```tableau
[GDP] / [Population]
```

Convert GDP to a numeric value first. Do not calculate with missing or zero population values.

## Urbanization ratio

```tableau
[Urban_population] / [Population]
```

`Urban_population` is treated as an urban population count, despite the supplied description calling it a percentage.

## Urbanization categories used in the original project

```tableau
IF [urban ratio] < 0.815 THEN "Low"
ELSEIF [urban ratio] < 0.827 THEN "Medium"
ELSE "High"
END
```

These are project-specific thresholds, not internationally defined urbanization categories.

## Country-level average price difference

```tableau
{ FIXED [Country] : AVG([Priceeach] - [Msrp]) }
```

## Original dashboard labels

```tableau
IF [price-msrp for each country] > 0 THEN "profit"
ELSE "loss"
END
```

The original labels include a zero difference in “loss.” For a new analysis, use “Above MSRP,” “At MSRP,” and “Below MSRP,” and handle missing values explicitly. MSRP does not represent the seller's cost, so these categories do not measure profitability.
