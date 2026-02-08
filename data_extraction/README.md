## Data Extraction – NASA POWER (Daily)

This module handles district-wise extraction of daily weather data for Maharashtra
using the NASA POWER API.

### Spatial Coverage
- All districts of Maharashtra
- Representative latitude–longitude points per district
- Complete coverage of:
  - East Vidarbha
  - West Vidarbha
  - Marathwada
  - Western Maharashtra
  - North Maharashtra
  - Konkan

### Step-by-Step Logic

1. **Define District Coordinates**
   Each district is assigned a representative geographic coordinate to query
   gridded NASA POWER data.

2. **Validate Weather Parameters**
   Only parameters officially supported by NASA POWER AG daily datasets
   are queried to avoid API failures.

3. **Estimate Dataset Size**
   The expected number of records is calculated before download to:
   - Warn about Excel row limits
   - Prevent accidental generation of unusable files

4. **District-wise Data Fetch**
   Data are fetched individually for each district using:
   - Latitude
   - Longitude
   - User-defined time range
   - Selected parameters

5. **Region Classification**
   Each district is mapped to a corrected agro-climatic region for
   downstream regional analysis.

6. **Error Handling**
   API timeouts, network errors, and malformed responses are caught
   without stopping the entire pipeline.

7. **Data Consolidation**
   District-level data are combined into a single time-indexed dataset
   with standardized column ordering.

8. **Large Dataset Optimization**
   When Excel limits are exceeded:
   - Year-wise Excel files are generated
   - CSV format is saved
   - Parquet format is saved for efficient analytics

9. **Configuration-driven Execution**
   Weather parameters are controlled via `config.yaml`, keeping the
   code flexible and reproducible.

### Output
Raw, analysis-ready datasets saved in multiple formats depending on size.
