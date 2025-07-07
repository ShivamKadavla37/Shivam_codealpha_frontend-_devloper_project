# Air Quality Visualizer & Forecast App - Setup Guide

## 🚀 Quick Start

### Step 1: Download Files
1. Download all files to your local directory:
   - `air.html` - Main application file
   - `api-simulation.js` - API simulation for testing
   - `README.md` - Complete documentation
   - `SETUP_GUIDE.md` - This setup guide

### Step 2: Open the Application
1. Open `air.html` in your web browser
2. The app will load immediately with simulated data
3. You'll see the beautiful interface with real-time AQI display

### Step 3: Test Features
1. **Location Services**: Click "Current Location" to use GPS
2. **City Search**: Type a city name and click "Search"
3. **Interactive Map**: View the Google Maps integration
4. **Historical Trends**: See the 7-day AQI chart
5. **Forecast**: Check the 72-hour predictions
6. **Health Tips**: Read personalized recommendations
7. **Notifications**: Click the bell icon to enable alerts

## 🔧 Advanced Setup (Optional)

### Google Maps API Integration
For full map functionality:

1. **Get API Key**:
   - Go to [Google Cloud Console](https://console.cloud.google.com/)
   - Create a new project
   - Enable "Maps JavaScript API" and "Geocoding API"
   - Create credentials (API key)

2. **Update the Code**:
   ```html
   <!-- In air.html, line 7, replace YOUR_GOOGLE_MAPS_API_KEY -->
   <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_ACTUAL_API_KEY&libraries=places"></script>
   ```

### Real Data Integration
To connect with actual air quality APIs:

1. **CPCB API** (Central Pollution Control Board):
   ```javascript
   // Replace simulated data in air.html with real API calls
   const cpcbResponse = await fetch('https://api.cpcb.gov.in/aqi/current');
   ```

2. **Weather API** (OpenWeatherMap):
   ```javascript
   // Add weather data for better forecasting
   const weatherResponse = await fetch(`https://api.openweathermap.org/data/2.5/weather?lat=${lat}&lon=${lng}&appid=YOUR_WEATHER_API_KEY`);
   ```

3. **ISRO Satellite Data**:
   ```javascript
   // Integrate satellite imagery for pollution mapping
   const satelliteResponse = await fetch('https://api.isro.gov.in/satellite/aerosol');
   ```

## 📱 Mobile Testing

### Local Development Server
For testing on mobile devices:

1. **Using Python**:
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   ```

2. **Using Node.js**:
   ```bash
   # Install http-server globally
   npm install -g http-server
   
   # Run server
   http-server -p 8000
   ```

3. **Access on Mobile**:
   - Find your computer's IP address
   - On mobile, go to: `http://YOUR_IP:8000/air.html`

## 🎯 Features Testing Checklist

### ✅ Basic Features
- [ ] App loads without errors
- [ ] Real-time AQI display shows data
- [ ] Color-coded AQI indicators work
- [ ] Pollutant details are displayed
- [ ] Interactive map loads
- [ ] Historical chart renders
- [ ] Forecast data shows
- [ ] Health recommendations display

### ✅ Interactive Features
- [ ] Current location button works
- [ ] City search functionality
- [ ] Map markers appear
- [ ] Chart interactions work
- [ ] Notification toggle functions
- [ ] Responsive design on mobile

### ✅ Advanced Features
- [ ] Auto-refresh every 5 minutes
- [ ] High AQI notifications
- [ ] Smooth animations
- [ ] Loading states
- [ ] Error handling

## 🚨 Troubleshooting

### Common Issues

1. **Maps Not Loading**:
   - Check internet connection
   - Verify Google Maps API key
   - Check browser console for errors

2. **Location Not Working**:
   - Ensure HTTPS or localhost
   - Check browser permissions
   - Try refreshing the page

3. **Notifications Blocked**:
   - Check browser notification settings
   - Allow notifications when prompted
   - Test in different browsers

4. **Slow Loading**:
   - Check internet speed
   - Clear browser cache
   - Disable browser extensions

### Browser Compatibility
- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+
- ⚠️ Internet Explorer (not supported)

## 🔄 Data Refresh

### Automatic Updates
- Real-time AQI: Every 5 minutes
- Historical data: On location change
- Forecast data: Every hour
- Notifications: Every 10 minutes

### Manual Refresh
- Click "Current Location" or "Search" buttons
- Refresh browser page
- Wait for automatic updates

## 📊 Data Sources

### Current Implementation (Simulated)
- AQI values: Random generation (50-350 range)
- Location data: Google Maps Geocoding
- Historical data: Simulated 7-day trends
- Forecast data: Predictive modeling simulation

### Real Implementation (Future)
- CPCB (Central Pollution Control Board)
- IMD (India Meteorological Department)
- ISRO Satellite Data
- OpenWeatherMap API
- Local air quality sensors

## 🎨 Customization

### Styling Changes
Edit CSS variables in `air.html`:
```css
:root {
    --primary-color: #667eea;
    --secondary-color: #764ba2;
    --success-color: #00e676;
    --warning-color: #ffeb3b;
    --danger-color: #f44336;
}
```

### Adding Features
1. **New Data Sources**: Modify `api-simulation.js`
2. **Additional Charts**: Add Chart.js configurations
3. **More Pollutants**: Extend the AQI display
4. **Custom Alerts**: Modify notification thresholds

## 📞 Support

### Getting Help
1. Check browser console for errors
2. Verify all files are in the same directory
3. Test with different browsers
4. Check internet connection

### File Structure
```
vision-gallery/
├── air.html              # Main application
├── api-simulation.js     # API simulation
├── README.md            # Complete documentation
├── SETUP_GUIDE.md       # This setup guide
└── logo.jpeg            # App logo
```

### Next Steps
1. Test all features thoroughly
2. Customize styling if needed
3. Integrate real APIs for production
4. Deploy to web server
5. Share with users

---

**Happy Coding! 🚀**

The Air Quality Visualizer & Forecast App is now ready to use. Enjoy monitoring air quality and staying healthy! 🌬️ 