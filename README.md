# 🌍 Live Weather AI Forecast System

A real-time weather prediction application combining live API data with AI-powered forecasting.

## 🆕 What's New (Improvements)

### ✅ Live Real-Time Weather Data
- Integrated **Open-Meteo API** for live weather data (no API key needed!)
- Current conditions: temperature, humidity, wind speed, precipitation
- 24-hour hourly forecast
- 7-day weather forecast

### ✅ AI-Enhanced Predictions
- VAE+LSTM model trained on historical NOAA weather data
- 7-day trend analysis powered by AI
- 30-day average forecasts
- Multi-step ahead predictions

### ✅ Better Accuracy
- Live current conditions as baseline for predictions
- Combining real-time API data with historical patterns
- Intelligent fallback to historical data if API unavailable
- Better weather condition classification
- Weather alerts and health advisories

### ✅ Improved User Interface
- Dark theme interface for easy viewing
- Scrollable text area for detailed information
- Two-button system: "Get Live Weather" + "AI Forecast"
- Real-time status updates
- Comprehensive weather insights and alerts

## 📋 Requirements

Install dependencies:
```bash
pip install -r requirements.txt
```

### Required Libraries:
- `torch` - AI model framework
- `numpy` - Numerical computations
- `pandas` - Data handling
- `scikit-learn` - Data preprocessing
- `requests` - API calls for live weather
- `tqdm` - Progress bars

## 🚀 How to Run

```bash
python demo.py
```

## 🎯 Features

### Live Weather Display
1. Click **"🔄 Get Live Weather"** button
2. Select your city from dropdown
3. View:
   - Current conditions with temperature, humidity, wind
   - 7-day forecast with temperature ranges and precipitation
   - 24-hour hourly breakdown
   - Weather alerts and health advisories

### AI Forecast
1. Click **"🔮 AI Forecast"** button
2. View:
   - Next period predictions based on AI model
   - 7-day trend analysis
   - 30-day average forecast
   - Health and safety warnings
   - Detailed weather condition descriptions

## 🌍 Supported Cities

The system supports these Tamil Nadu cities:
- Chennai
- Salem
- Coimbatore
- Madurai
- Erode
- Trichy
- Vellore
- Tirunelveli

## 🤖 AI Model Details

- **Architecture**: VAE (Variational Autoencoder) + LSTM
- **Input Features**: Temperature, Dew Point, Sea Level Pressure, Wind Speed, Precipitation, Visibility
- **Trained on**: 50,000+ sequences from NOAA weather stations
- **Prediction Horizon**: Multi-step ahead (hours to days)

## 🔌 Data Sources

### Live Data
- **Provider**: Open-Meteo (https://open-meteo.com/)
- **Free**: Yes, no API key required
- **Coverage**: Global with high accuracy
- **Update Frequency**: Real-time

### Historical Data
- **Source**: NOAA National Centers for Environmental Information
- **Format**: CSV files in `2025/` folder
- **Features**: Temperature, Dew Point, Pressure, Wind Speed, Precipitation, Visibility

## 💡 Key Improvements Over Previous Version

| Feature | Before | After |
|---------|--------|-------|
| Data Source | Only local CSV files | Live API + Local data |
| Current Weather | Simulated | Real-time from Open-Meteo API |
| Forecast Accuracy | Lower (no live baseline) | Higher (AI calibrated to real conditions) |
| Update Frequency | Manual | Real-time on demand |
| User Interface | Basic label widget | Advanced scrolled text with formatting |
| Alerts | Generic | Weather-specific with health advisory |
| Data Fallback | None | Automatic fallback to historical data |

## ⚠️ Alerts & Advisories

The system provides intelligent alerts for:
- 🔥 **Heat**: High temperature warnings
- 🌧️ **Rain**: Precipitation alerts
- 💨 **Wind**: Strong wind warnings
- 🌫️ **Visibility**: Poor visibility alerts
- 💧 **Humidity**: High humidity warnings

## 🛠️ Troubleshooting

### "Error fetching weather data"
- Check internet connection
- Open-Meteo API might be temporarily unavailable
- Try again in a few moments

### "No weather data available"
- Ensure historical CSV files are in `2025/` folder
- Or ensure you have internet for live API
- Check city name spelling

### "Model loading failed"
- System will train a new model on first run
- Training takes 1-2 minutes depending on dataset size
- Model will be saved for future use

## 📊 Data Format

### Weather Features (6 parameters)
1. **TEMP** - Temperature (°C)
2. **DEWP** - Dew Point (°C)
3. **SLP** - Sea Level Pressure (hPa)
4. **WDSP** - Wind Speed (m/s)
5. **PRCP** - Precipitation (mm)
6. **VISIB** - Visibility (km)

## 🔐 Privacy & Data

- **No personal data** is collected or stored
- **API calls** to Open-Meteo are anonymous
- **Local CSV data** is only used for model training
- **Forecasts** are computed locally, not uploaded

## 📝 License

This project is for educational and personal use.

## 👨‍💻 Credits

- **Weather Data**: Open-Meteo API (https://open-meteo.com/)
- **Historical Data**: NOAA (https://www.noaa.gov/)
- **AI Framework**: PyTorch
- **Data Processing**: Pandas & Scikit-learn

---

**Last Updated**: March 2026  
**Version**: 2.0 (Live Weather Enhanced)
