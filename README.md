# 🌍 Climate-Change-Forecasting-using-Deep-Learning
A deep learning project focused on modeling and forecasting maximum daily temperature (Tmax) using satellite climate data. This project leverages time series models like LSTM, TCN, and GRU to understand temperature trends, support agricultural planning, and provide insights into climate change impacts.
![temperature_animation](https://github.com/user-attachments/assets/78b33613-abe4-4612-85ba-22ff339c5c4b)

## 🧠 Models Used
We implemented and compared three deep learning models:
- LSTM (Long Short-Term Memory)
- TCN (Temporal Convolutional Network)
- GRU (Gated Recurrent Unit)

Evaluated Using:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)

All models were trained on normalized time-series data with early stopping to avoid overfitting.

## 🌐 Dataset: AgCFSR
AgCFSR (Agricultural Climate Forcing Dataset)
- Provided by NASA GISS in collaboration with AgMIP
- Time Range: 1980–2010 (daily resolution)
- Spatial Resolution: 0.25° × 0.25°
- Format: `.nc4` (NetCDF4)
- Variables Used:
-   Maximum Temperature (Tmax)
-   Precipitation
-   Solar Radiation
-   Relative Humidity
-   Wind Speed

📦 **Source:** NASA GISS AgMIP Climate Data 

## 🛠️ Project Stages

### 1. Data Acquisition
- Programmatically downloaded yearly `.nc4` files from 1980 to 2010 using `wget`
- Stored and managed in Google Drive

### 2. Data Exploration & Cleaning
- Parsed NetCDF files using netCDF4
- Extracted `tmax`, `latitude`, `longitude`, and `time`
- Handled null/outlier values (e.g., 32767)
- Scaled and normalized data

### 3. Data Visualization
- Static maps of temperature at given dates
- GIF animations showing temporal-spatial variations
- Tools: `matplotlib`, `FuncAnimation`

### 4. Feature Engineering
- Flattened multidimensional data to tabular format:
  `Time | Latitude | Longitude | Temperature`
- Normalized temperature
- Created sliding windows for time-series learning

### 5. Evaluation & Results

| Model | Parameters | MAE (Train) |	MAE (Val) | Best Val Loss |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| LSTM  | 30,651 | 0.0087 | 0.0041 | 6.73e-05  |
| GRU  | 23,301 | 0.0086  | 0.0042  | 6.69e-05 |
| TCN  | 90,149 | 	0.0120  | 0.0052 | 7.59e-05  |



