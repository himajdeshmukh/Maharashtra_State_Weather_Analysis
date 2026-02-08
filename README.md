# Maharashtra_State_Weather_Analysis
Long-term (≈40 years) district-level weather data analysis for Maharashtra, using NASA POWER daily AG datasets which contains 4,96,741 rows and 12 parameters, with region-wise and scenario-wise statistical summaries and visualizations.
# Maharashtra Weather Data Analysis (40+ Years)

This repository contains a complete pipeline for extracting, processing, analyzing,
and visualizing long-term district-level weather data for Maharashtra, India.

Daily weather data are sourced from the NASA POWER AG dataset and analyzed at
district, regional, and state scales.

## Key Features
- 40+ years of daily weather data
- District-level spatial coverage of Maharashtra
- Region-wise aggregation and comparison
- Separate analysis for:
  - All regions of Maharashtra
  - Maharashtra excluding Konkan region
- Scalable handling of large datasets
- Clean separation of extraction, analysis, and visualization

## Data Source
NASA POWER (Prediction of Worldwide Energy Resources) – Daily AG datasets

## Repository Structure
- `data_extraction/` – Data download and preprocessing
- `analysis/` – Statistical analysis scripts
- `visualisation/` – Plotting and visualization scripts
- `output/` – Generated results (not tracked)
- `utils/` – Shared helper functions

## Notes
- All scripts use anonymized and non-proprietary data
- No hard-coded file paths or outputs
- Outputs are generated only when scripts are executed
