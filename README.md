# Assignment 2 – Cleaned Datasets
**Student ID:** 23L0993

This repository contains the cleaned Netflix Movies and TV Shows dataset and Supermarket Sales dataset for AI Assignment 2. These datasets will also be used in Assignment 3 to ensure consistent and reproducible results.

**Version:** v1.0  
**Publication date:** 19 October 2026

## Part A – Netflix Movies and TV Shows

- **Original source:** https://www.kaggle.com/datasets/shivamb/netflix
- **Cleaned file:** `netflix_cleaned.csv`
- **Version:** v1.0

### Cleaning decisions

1. Corrected 3 rating values that were actually movie durations. Moved them to the duration column and left their ratings empty.
2. Filled missing director, cast, and country values with `Unknown`.
3. Left the 10 missing `date_added` values empty because their dates could not be determined.
4. Standardized `NR` and `UR` ratings as `Unrated` and cleaned spaces in dates and extra commas in country values.
5. Split duration into separate numeric columns: `movie_minutes` and `seasons`.
6. Created additional features, including `gap_years`, `year_added`, `month_added`, `rating_group`, `num_genres`, `num_cast`, `primary_genre`, and `primary_country`.
7. Kept unusually long movies, titles with many seasons, and titles added before their release year because they were not confirmed data errors.

### Dataset information

The original dataset contains 8,807 titles and 12 columns. It includes information about title type, release year, ratings, cast, directors, countries, genres, duration, and descriptions.

## Part B – Supermarket Sales

- **Original source:** Instructor-provided Supermarket Sales CSV file.
- **Cleaned file:** `supermarket_sales_cleaned.csv`
- **Version:** v1.0

### Cleaning decisions

1. Checked for missing values, duplicate rows, and invalid values. No issues requiring data correction were found.
2. Converted `Date` from text to a date data type and extracted the hour from `Time`.
3. Created additional features: `month`, `day_of_week`, `is_weekend`, `hour`, and `time_period`.
4. Kept the original columns, including repeated information between Branch and City and between the monetary columns, for reference.
5. Kept the 9 high-total sales records because they were considered valid purchases rather than confirmed errors.

### Dataset information

The dataset contains 1,000 sales records and 17 original columns. It covers three supermarket branches in Yangon, Mandalay, and Naypyitaw from January to March 2019.

## Versioning and reproducibility

Version v1.0 represents the published cleaned datasets used for Assignment 2 and intended for Assignment 3.

The files are kept unchanged after publication so that future analysis can use the same data. Any changes to either dataset will be published under a new version.

For Assignment 3, use the CSV files from the published v1.0 release rather than an unversioned or subsequently modified copy.
