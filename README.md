# 🌍 Climate-Change-Forecasting-using-Deep-Learning
A deep learning project focused on modeling and forecasting maximum daily temperature (Tmax) using satellite climate data. This project leverages time series models like LSTM, TCN, and GRU to understand temperature trends, support agricultural planning, and provide insights into climate change impacts.
![temperature_animation](https://github.com/user-attachments/assets/78b33613-abe4-4612-85ba-22ff339c5c4b)

## Models Used
We implemented and compared three deep learning models:
- LSTM (Long Short-Term Memory)
- TCN (Temporal Convolutional Network)
- GRU (Gated Recurrent Unit)

All models were trained on normalized time-series data with early stopping to avoid overfitting.

## 🌐 Dataset: AgCFSR
AgCFSR (Agricultural Climate Forcing Dataset)
- Provided by NASA GISS in collaboration with AgMIP
- Time Range: 1980–2010 (daily resolution)
- Spatial Resolution: 0.25° × 0.25°
- Format: .nc4 (NetCDF4)
- Variables Used:
-   Maximum Temperature (Tmax)
-   Precipitation
-   Solar Radiation
-   Relative Humidity
-   Wind Speed

📦 **Source:** NASA GISS AgMIP Climate Data 





