# Demographic Data Analyzer

A Python project that analyzes demographic data from the Adult Census Income dataset to extract insights about race distribution, education levels, income patterns, and occupation trends.

## Overview

This project processes census data to answer key demographic questions including:

- Race representation in the dataset
- Average age of men
- Educational attainment (Bachelor's degree percentage)
- Income distribution by education level
- Work hours and income correlation
- International income patterns and occupations

## Features

- **Race Distribution Analysis**: Count of people represented by each race
- **Education Analysis**: Percentage of people with Bachelor's degrees and advanced education
- **Income Analysis**: Income distribution across different education and work hour groups
- **Geographic Insights**: Country-specific income percentages and occupation data
- **Demographic Statistics**: Average age, work hours, and occupation trends

## Requirements

- Python 3.x
- pandas

## Usage

```python
from demographic_data_analyzer import calculate_demographic_data

# Run analysis with printed output
results = calculate_demographic_data(print_data=True)

# Or run without printing
results = calculate_demographic_data(print_data=False)
```

## Data

The project expects an `adult.data.csv` file containing census data with columns including:

- age
- race
- sex
- education
- salary
- hours-per-week
- native-country
- occupation

## Output

The function returns a dictionary containing:

- `race_count`: Value counts of races
- `average_age_men`: Average age of male subjects
- `percentage_bachelors`: Percentage with Bachelor's degrees
- `higher_education_rich`: Percentage earning >50K with advanced education
- `lower_education_rich`: Percentage earning >50K without advanced education
- `min_work_hours`: Minimum hours worked per week
- `rich_percentage`: Percentage earning >50K among minimum workers
- `highest_earning_country`: Country with highest percentage of >50K earners
- `highest_earning_country_percentage`: Percentage of rich in top earning country
- `top_IN_occupation`: Most common occupation for >50K earners in India
