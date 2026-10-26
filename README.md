# AISE 4010 — Group 4 Project

## Dataset
Open Power System Data (OPSD)

## Forecasting Task
Forecast Germany's hourly electricity load.

- Target: `DE_load_actual_entsoe_transparency`
- Unit: MW
- Native frequency: 1 hour
- Lookback: 168 hours (7 days)
- Forecast horizon: 24 hours

## Stage 1
Stage 1 includes:

- Data audit and exploratory analysis
- Chronological 60/20/20 train-validation-test split
- Training-only standardization
- Daily persistence baseline
- Weekly seasonal naive baseline
- MLP model
- 1D CNN model
- Validation-only grid search
- Final controlled model comparison

## Stage 1 Results

Best simple baseline:
- Weekly seasonal naive
- Test RMSE: 3886.99 MW

Best model:
- Tuned 1D CNN
- Filters: 16
- Kernel size: 7
- Test MAE: 2266.02 MW
- Test RMSE: 3145.41 MW
- RMSE improvement over best baseline: 19.08%

## Data Access
The raw dataset is not committed because of its size.

Source:
https://data.open-power-system-data.org/time_series/

Required file:
`time_series_60min_singleindex.csv`

## Author
Jaspreet Singh Saini
