--> Project Overview
This project performs an Exploratory Data Analysis (EDA) on the South-East Brazil Hourly Weather Dataset from Kaggle.  
The dataset includes weather variables such as temperature, rainfall, humidity, wind, pressure, and solar radiation across multiple stations in the region.

--> Goal:
- Understand temporal and spatial weather patterns.  
- Detect anomalies, missing values, and extreme events.  
- Prepare the dataset for visualization, reporting, and predictive modeling.

--> Tools & Libraries
- Python: `pandas`, `numpy`, `matplotlib`, `seaborn`  
- Kaggle environment for data handling  


==> Dataset Description

The dataset contains information about weather, including:
-'index': 'index',
    'data': 'date',
    'hora': 'hour',
    'precipitação_total_horário_(mm)': 'total precipitation',
    'pressao_atmosferica_ao_nivel_da_estacao_horaria_(mb)': 'atmospheric pressure at station height',
    'pressão_atmosferica_max.na_hora_ant._(aut)_(mb)': 'atmospheric pressure max. in the previous hour',
    'pressão_atmosferica_min._na_hora_ant._(aut)_(mb)': 'atmospheric pressure min. in the previous hour',
    'radiacao_global_(kj/m²)': 'solar_radiation',
    'temperatura_do_ar_-_bulbo_seco_horaria_(°c)': 'air temperature - dry bulb',
    'temperatura_do_ponto_de_orvalho_(°c)': 'dew point temperature',
    'temperatura_máxima_na_hora_ant._(aut)_(°c)': 'max. temperature in the previous hour',
    'temperatura_mínima_na_hora_ant._(aut)_(°c)': 'min. temperature in the previous hour',
    'temperatura_orvalho_max._na_hora_ant._(aut)_(°c)': 'dew temperature max. in the previous hour',
    'temperatura_orvalho_min._na_hora_ant._(aut)_(°c)': 'dew temperature min. in the previous hour',
    'umidade_rel._max._na_hora_ant._(aut)_(%)': 'relative humidity max. in the previous hour',
    'umidade_rel._min._na_hora_ant._(aut)_(%)': 'relative humidity min. in the previous hour',
    'umidade_relativa_do_ar_horaria_(%)': 'air relative humidity',
    'vento_direção_horaria_(gr)_(°_(gr))': 'wind direction',
    'vento_rajada_maxima_(m/s)': 'wind rajada maxima',
    'vento_velocidade_horaria_(m/s)': 'wind speed',
    'region': 'region',
    'state': 'state',
    'station': 'station',
    'station_code': 'station_code',
    'latitude': 'latitude',
    'longitude': 'longitude',
    'height': 'height'

1. Data Cleaning & Preparation
-- Column Renaming: 
   Long Portuguese column names were renamed to short, English, snake_case for easier analysis.
   
-- Datetime Handling:
   - `date` + `hour` combined into a single `datetime` column  
   - Sorted chronologically  
   - Ensures proper time-series analysis

2. Exploratory Data Analysis (EDA)

-- Univariate Analysis
- Temperature: Normal distribution with seasonal and daily cycles  
- Rainfall: Highly right-skewed, event-based  
- Humidity: Mostly high values, correlates with rainfall  
- Wind & Pressure: Extreme values retained for event analysis

-- Bivariate Analysis
- Rainfall occurs at lower pressure
- Temperature correlates with solar radiation  
- Humidity positively correlates with rainfall  
- Wind largely independent of temperature

-- Time-Series Analysis
- Daily, monthly, and yearly trends analyzed  
- 30-day rolling averages applied to remove noise  
- Hourly patterns reveal diurnal cycles  
- Seasonal rainfall and temperature trends visualized

-- Location-Based Analysis
- Regional comparison across `state` and `station`  
- Coastal vs inland temperature differences observed  
- Rainfall variability across stations identified  


3. SQL Analysis
- Month wise rainfall
- hour wise temp.
- Top 5 hotest place
- state wise temp.
