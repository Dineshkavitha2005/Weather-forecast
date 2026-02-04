# WeatherWise - AI-Powered Weather Forecast

A modern, feature-rich weather forecast application with interactive maps, multi-language support, and AI-powered chatbot assistance.

## Features

- 🌤️ Real-time weather data from OpenWeatherMap
- 🗺️ Interactive weather maps with multiple layers (Temperature, Precipitation, Clouds, Wind, Pressure)
- 🌍 Multi-language support (10+ languages)
- 🎙️ Voice search capability
- 💬 AI-powered weather chatbot
- 📱 Responsive design for all devices
- 🌓 Dark/Light theme toggle
- 📍 Geolocation support

## Setup Instructions

### 1. Get Your OpenWeatherMap API Key

1. Visit [OpenWeatherMap](https://openweathermap.org/api)
2. Sign up for a free account
3. Navigate to your API keys section
4. Copy your API key

### 2. Configure the Application

1. Copy the example configuration file:
   ```bash
   cp config.example.js config.js
   ```

2. Open `config.js` in your text editor

3. Replace `YOUR_API_KEY_HERE` with your actual OpenWeatherMap API key:
   ```javascript
   const CONFIG = {
       OPENWEATHER_API_KEY: 'your_actual_api_key_here'
   };
   ```

4. Save the file

**Important:** The `config.js` file is already added to `.gitignore` and will not be committed to version control, keeping your API key secure.

### 3. Run the Application

Simply open `index.html` in your web browser. No build process or server is required!

```bash
# Option 1: Open directly
open index.html

# Option 2: Use a simple HTTP server (recommended)
python -m http.server 8000
# Then visit http://localhost:8000 in your browser
```

## Security Best Practices

### API Key Security

- ✅ **Never commit `config.js`** - This file contains your API key and is git-ignored
- ✅ **Use environment variables** - For production deployments, consider using environment variables
- ✅ **Rotate keys regularly** - Periodically regenerate your API key on OpenWeatherMap
- ✅ **Set up usage limits** - Configure API rate limits on your OpenWeatherMap account

### File Structure

```
Weather-forecast/
├── index.html          # Main HTML file
├── app.js             # Main application logic
├── weatherMap.js      # Interactive map functionality
├── auth.js            # Authentication logic
├── auth.html          # Authentication page
├── auth.css           # Authentication styles
├── styles.css         # Main stylesheet
├── translations.js    # Multi-language support
├── cities.js          # City database
├── config.js          # Your API configuration (gitignored)
├── config.example.js  # Configuration template
├── .gitignore         # Git ignore rules
└── README.md          # This file
```

## Usage

### Searching for Weather

1. **Text Search**: Type a city name in the search bar
2. **Voice Search**: Click the microphone icon and speak the city name
3. **Geolocation**: Click the location icon to get weather for your current location
4. **Map Search**: Use the interactive map to search and explore weather worldwide

### Chatbot Commands

The AI chatbot can help you with:
- Current weather queries: "What's the weather in Tokyo?"
- Weather comparisons: "Compare weather in Paris and London"
- Forecast questions: "Will it rain tomorrow?"
- Weather advice: "Should I bring an umbrella?"

### Language Support

Select your preferred language from the dropdown menu. Supported languages:
- English, Spanish, French, German, Hindi, Tamil, Chinese, Arabic, Portuguese, Japanese

## Troubleshooting

### API Key Issues

**Problem**: Application shows "API Key not configured" or weather data doesn't load

**Solution**: 
1. Ensure `config.js` exists (copy from `config.example.js`)
2. Verify your API key is correctly entered in `config.js`
3. Check that your API key is activated on OpenWeatherMap (can take a few minutes)
4. Confirm the `config.js` script is loaded before other scripts in `index.html`

### CORS Issues

**Problem**: Browser console shows CORS errors

**Solution**: 
- Run the application through a web server (not `file://` protocol)
- Use `python -m http.server` or similar local server

### Map Not Loading

**Problem**: Weather map doesn't display

**Solution**:
1. Check browser console for JavaScript errors
2. Ensure you have an internet connection
3. Verify your API key has access to map tiles
4. Try refreshing the page

## Contributing

Contributions are welcome! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

**Security Note**: Never include actual API keys in pull requests. Always use placeholder values.

## License

This project is open source and available under the MIT License.

## Credits

- Weather data provided by [OpenWeatherMap](https://openweathermap.org/)
- Maps powered by [Leaflet](https://leafletjs.com/) and [OpenStreetMap](https://www.openstreetmap.org/)
- Icons from [Font Awesome](https://fontawesome.com/)

## Support

For issues or questions:
1. Check the Troubleshooting section above
2. Review the OpenWeatherMap API documentation
3. Open an issue on GitHub

---

**⚠️ Security Reminder**: Always keep your `config.js` file private and never share your API key publicly!
