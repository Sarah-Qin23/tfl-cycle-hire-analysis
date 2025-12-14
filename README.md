## Data Source
The data used in this project are the Transport for London (TfL) Cycle Hire Trip Data.
Four representative months from 2024 were selected to capture seasonal variation:
January, April, August and October.

## Data Preparation
For each selected month, the raw TfL data were provided as two extracts
(1–14 and 15–end of month). These files were concatenated to form a single
monthly raw dataset.

Data cleaning was applied consistently across all months. Column names were
standardised, datetime fields were parsed for trip start and end times, and trip
duration was converted to numeric format. Records with missing values in key
fields (start time, end time, duration) were removed. Trips with non-positive
durations or durations longer than 24 hours were excluded to remove obvious
errors. Additional time-based variables (date, hour, weekday) were derived for
analysis.

## Analysis Data
Due to file size constraints, the original raw TfL datasets are not uploaded to
this repository. Instead, the cleaned and analysis-ready datasets are provided,
together with all scripts used to transform the raw data into the final analysis
datasets. This ensures transparency and reproducibility of the data preparation
process.

## Repository Structure
- `data/analysis/` – cleaned datasets used for analysis  
- `scripts/merge/` – scripts used to merge raw data files  
- `scripts/clean/` – scripts used to clean and prepare the data
