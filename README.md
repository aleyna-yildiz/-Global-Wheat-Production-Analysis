# Agricultural Energy Use and Emissions Analysis

## Research Question

How has energy use in agriculture and the resulting greenhouse gas emissions changed across countries and fuel types over time?

Which countries have increased agricultural energy use while reducing their emissions intensity between 2000 and 2022?

## Objective

This project aims to analyze agricultural energy use and energy-related greenhouse gas emissions across countries from 2000 to 2023.

The analysis focuses on:

- Trends in agricultural energy consumption
- CO2, CH4, and N2O emissions
- Changes in the composition of agricultural energy use by fuel type
- Differences between countries and regions
- Emissions intensity per unit of energy use
- The relationship between increasing energy use and changes in emissions
- Identifying countries showing signs of decoupling between energy use and emissions intensity

## Primary Data Source

### FAOSTAT — Emissions from Energy Use in Agriculture (GN)

The primary dataset contains agricultural energy-use and emissions data for:

- 178 countries and regions
- 2000–2023
- 5 fuel types:
  - Petroleum products
  - Electricity
  - Natural gas
  - Heat
  - Coal
- 4 elements:
  - Energy use in agriculture (TJ)
  - CO2 emissions (kt)
  - CH4 emissions (kt)
  - N2O emissions (kt)

The original dataset is provided in long (tidy) format, where each observation represents a country × fuel × year × element combination.

## Data Quality Considerations

Several data-quality issues must be considered before analysis.

### 1. Mixed measurement units

Energy use is measured in TJ, while emissions are measured in kt.

Therefore, values from different elements must not be aggregated without first separating the measurement types.

### 2. Estimated and imputed observations

The dataset contains observation-status flags indicating whether values are official, estimated, or imputed.

According to the initial data inspection:

- Emission observations are marked as estimated.
- Energy-use observations contain a mixture of official, estimated, and imputed values.
- The proportion of official observations decreases substantially in the most recent year.

These flags will therefore be retained throughout the analysis.

### 3. Potential carry-forward values in 2023

The 2023 observations require particular caution.

A large proportion of country–fuel combinations have exactly the same value in 2023 as in 2022, suggesting that some observations may have been carried forward or imputed.

Therefore:

- 2000–2022 will be treated as the primary analytical period.
- 2023 will be retained for descriptive purposes but analyzed separately and clearly flagged.

### 4. Geographic aggregation

The dataset contains both individual territories and aggregate or historical geographic entities.

Examples include:

- China and China, mainland
- China, Hong Kong SAR
- China, Taiwan Province of
- Sudan and South Sudan
- Historical entities such as Sudan (former)
- Serbia and Montenegro

These entities must be standardized before country-level comparisons or rankings are performed in order to avoid double counting.

### 5. Unbalanced panel structure

Not every country or region has observations for every year or every fuel type.

Therefore, country comparisons must account for differences in:

- Time coverage
- Fuel coverage
- Geographic coverage

A balanced subset of countries may be created for selected longitudinal analyses.

### 6. Zero values

Some observations contain exact zero values.

These values cannot automatically be interpreted as either true zero emissions or missing information.

Zero values will therefore be investigated before calculating:

- Growth rates
- Ratios
- Log transformations
- Emissions intensity

## Analytical Strategy

The analysis will proceed in the following stages:

1. Load and inspect the raw FAOSTAT dataset
2. Validate its structure, dimensions, and data types
3. Remove redundant columns
4. Standardize country and geographic entities
5. Reshape the data from long to wide format
6. Separate energy-use and emissions variables by unit
7. Preserve and analyze observation-status flags
8. Evaluate panel completeness and fuel coverage
9. Explore global and country-level trends
10. Analyze the contribution of different fuel types
11. Calculate emissions intensity
12. Investigate changes in energy use versus emissions intensity
13. Identify potential decoupling patterns
14. Visualize the main findings
15. Document limitations and uncertainty

## Key Metrics

### Energy Use

Agricultural energy consumption by country, year, and fuel type.

### Emissions

CO2, CH4, and N2O emissions associated with agricultural energy use.

### Emissions Intensity

Emissions per unit of energy consumed:

Emissions Intensity = Emissions / Energy Use

This metric will help distinguish increases in total emissions caused by higher energy demand from changes in emissions intensity.

### Fuel Share

The contribution of each fuel type to total agricultural energy use.

### Decoupling

The analysis will investigate countries where agricultural energy use increased while emissions intensity decreased.

These cases may indicate improvements in the emissions efficiency of agricultural energy use, although they will not automatically be interpreted as evidence of technological improvement without further investigation.

## Limitations

The dataset does not necessarily represent direct measurements of all emissions.

Emission values and their estimation methodology must therefore be interpreted according to FAOSTAT's metadata and methodological documentation.

In addition, changes in fuel coverage, imputation, geographic definitions, and data availability may affect observed trends.

Therefore, unusual increases or decreases will be investigated before being interpreted as real-world changes.

## Expected Outcomes

The project aims to identify:

- Global trends in agricultural energy use and emissions
- The changing role of different fuel types
- Countries with high and low emissions intensity
- Countries showing potential decoupling between energy use and emissions intensity
- Major data-quality and coverage limitations affecting international comparisons