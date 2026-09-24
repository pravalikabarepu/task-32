# COVID-19 Trends, Vaccination & Mortality Analysis

## Project Overview

This project analyzes publicly available COVID-19 data to understand how cases, deaths, vaccination rollout, and mortality varied across countries and over time.

The dashboard was developed in Power BI with a focus on presenting COVID-19 trends in a simple and interactive way for non-technical users.

## Objective


The main objectives of this project are:

* Analyze COVID-19 case and death trends over time
* Compare countries using population-normalized metrics
* Identify COVID-19 waves using 7-day rolling averages
* Track vaccination rollout over time
* Analyze reported case fatality rates
* Calculate case doubling time
* Examine the observed relationship between vaccination coverage and deaths per million

## Dataset

Source: Our World in Data COVID-19 dataset

The dataset contains country-level and date-level information about:

* COVID-19 cases
* COVID-19 deaths
* Vaccinations
* Population
* Cases per million
* Deaths per million
* Vaccination coverage

 # Dataset Link
 https://catalog.ourworldindata.org/garden/covid/latest/compact/compact.csv?utm_source=chatgpt.com

## Tools Used

* Power BI
* Power Query
* DAX
* Our World in Data COVID-19 dataset

## Data Cleaning

The dataset was prepared in Power Query before creating the dashboard.

Key cleaning steps:

* Selected relevant COVID-19 fields
* Converted date fields to Date format
* Converted numeric fields to appropriate numeric data types
* Handled blank and missing values carefully
* Excluded aggregate entities from the main country comparison
* Retained the original daily date for time-series analysis
* Created Year Month for monthly vaccination analysis

Missing values were not automatically treated as zero because a blank value can represent missing reporting rather than zero activity.

## Key Metrics

### Total Cases

Measures the latest reported cumulative COVID-19 cases for the selected country or countries.

### Total Deaths

Measures the latest reported cumulative COVID-19 deaths.

### Cases per Million

Normalizes reported cases by population to make country comparisons more meaningful.

### Deaths per Million

Normalizes reported deaths by population.

### Vaccination Coverage %

Calculated using:

```text
People Vaccinated / Population
```

This represents the share of the population that received at least one vaccination dose.

### Fully Vaccinated Coverage %

Calculated using:

```text
People Fully Vaccinated / Population
```

### 7-Day Rolling Average

Used to smooth daily reporting fluctuations and make COVID-19 waves easier to identify.

### Reported Case Fatality Rate

Calculated as:

```text
Reported Deaths / Reported Cases
```

This represents the fatality rate among reported cases and should not be interpreted as the infection fatality rate.

### Doubling Time

A 7-day-based estimate of how quickly reported cumulative cases were increasing.

A shorter doubling time indicates faster reported case growth.

## Dashboard Pages

### Page 1 — COVID-19 Global Trends & Impact

Includes:

* Total Cases
* Total Deaths
* Cases per Million
* Deaths per Million
* Vaccination Coverage
* Country, Continent and Date filters
* COVID-19 Waves — 7-Day Average Cases
* COVID-19 Death Trends
* Reported Cases per Million by Country

### Page 2 — Vaccination & Mortality Analysis

Includes:

* Vaccination Rollout Over Time
* Fully Vaccinated Coverage vs Deaths per Million
* Reported Case Fatality Rate Over Time
* COVID-19 Doubling Time
* Country, Continent and Date filters

## Key Insights

* COVID-19 case and death patterns varied considerably across countries and over different waves.
* Seven-day rolling averages provide a clearer view of major waves than daily reported values because they reduce short-term reporting fluctuations.
* Vaccination coverage increased at different speeds across countries and reached different levels.
* Deaths per million varied considerably between countries, including countries with relatively high vaccination coverage.
* The dashboard shows an observed relationship between vaccination coverage and reported deaths per million, but this analysis does not establish that vaccination coverage alone caused differences in mortality.

## Assumptions and Limitations

* COVID-19 figures represent reported data and may not capture all infections or deaths.
* Reporting practices and testing availability differed between countries and over time.
* Missing values were treated as missing rather than automatically converted to zero.
* Population-normalized measures were used for fairer country comparisons.
* Reported case fatality rate is based on reported cases and deaths and is not the same as infection fatality rate.
* The relationship between vaccination and mortality is observational and may also be affected by factors such as timing of waves, population characteristics, healthcare capacity, and reporting differences.
* Doubling time is an estimate based on reported case growth and should be interpreted with these data limitations in mind.

## Conclusion

This Power BI dashboard provides an interactive view of COVID-19 waves, mortality, vaccination rollout, and country-level differences. It combines time-series analysis, population-normalized metrics, and vaccination measures to communicate important COVID-19 trends in a clear and accessible format.
