# Data Dictionary

Put the 4 CSV files from `Global_Causes_of_Death_PowerBI.zip` in this folder.

## Fact_Deaths.csv
One row per country, year and cause (long format, about 190k rows).

| Column | Type | Description |
|---|---|---|
| Country | Text | Country name |
| Code | Text | ISO 3-letter country code (key) |
| Year | Whole number | 1990–2019 |
| Cause | Text | Cause of death (key to Dim_Cause) |
| Deaths | Whole number | Number of deaths |

## Dim_Cause.csv
| Column | Description |
|---|---|
| Cause | Cause of death (31 causes) |
| Category | Communicable, Maternal, Neonatal & Nutritional / Non-Communicable Diseases / Injuries |
| Category_Short | Communicable / Non-Communicable / Injuries |
| Include_In_Total | "No" for Protein-Energy Malnutrition (a subset of Nutritional Deficiencies) |
| Note | Explanation for excluded causes |

## Dim_Country.csv
| Column | Description |
|---|---|
| Code | ISO 3-letter code (key) |
| Country | Country name |
| Region | World Bank region |
| Income_Group | World Bank income group |
| Latitude / Longitude | Capital-city coordinates (for maps) |

## Country_Indicators.csv
One row per country and year. Source: World Bank WDI.

| Column | Description |
|---|---|
| Code, Year | Keys |
| Population | Total population |
| Life_Expectancy | Life expectancy at birth (years) |
| GDP_per_Capita_USD | GDP per person (current US$) |
| Health_Exp_per_Capita_USD | Current health expenditure per person (US$), from 2000 |
| Health_Exp_pct_GDP | Health expenditure as % of GDP, from 2000 |
| Basic_Water_Access_pct | % of people using at least basic drinking water, from 2000 |
| Total_Deaths | Total deaths, all causes in the dataset (excl. PEM) |
| Deaths_per_100k | Total_Deaths / Population × 100,000 |

## Sources
- IHME Global Burden of Disease 2019, via Kaggle: "Cause of Deaths around the World (Historical Data)"
- World Bank World Development Indicators API
