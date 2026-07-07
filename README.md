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
- ✅ **Rotate keys regularly** - Periodically regenerate your API key on OpenWeatherMap
- ✅ **If a key was ever committed, rotate it immediately** - Removing it from the working tree does not remove it from Git history
- ✅ **Use environment variables** - For production deployments, consider using environment variables
- ✅ **Set up usage limits** - Configure API rate limits on your OpenWeatherMap account

### File Structure

```
WeatherWise/
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
# 🌤️ Weather Forecast
A modern, feature-rich weather forecast web application built with vanilla JavaScript, HTML, and CSS. This application provides real-time weather information with a beautiful user interface, authentication system, and multi-language support.
## ✨ Features

- **Real-Time Weather Data**: Get current weather conditions and forecasts for cities worldwide
- **User Authentication**: Secure login and registration system
- **Interactive Weather Map**: Visual weather map integration for enhanced weather tracking
- **Multi-Language Support**: Access the application in multiple languages
- **Comprehensive City Database**: Support for thousands of cities globally
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Modern UI**: Clean and intuitive user interface with smooth animations

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- A weather API key (if required by the implementation)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Dineshkavitha2005/Weather-forecast.git
```

2. Navigate to the project directory:
```bash
cd Weather-forecast
```

3. Open `index.html` in your web browser or use a local development server:
```bash
# Using Python
python -m http.server 8000

# Using Node.js (http-server)
npx http-server
```

4. Access the application at `http://localhost:8000` (or your server's port)

## 📹 Demo Video

https://github.com/user-attachments/assets/e1f6774c-2ffe-4eef-9e7a-9c3f995b7bc8

## 📷 Screen Shots

<img width="1868" height="907" alt="Screenshot 2026-02-26 184021" src="https://github.com/user-attachments/assets/2cfaeb7f-3898-489d-8db0-1c3975aa4f07" />
<img width="1869" height="789" alt="Screenshot 2026-02-26 183931" src="https://github.com/user-attachments/assets/02410879-ad1c-497a-8b9c-29711b9afb2d" />
<img width="1876" height="1008" alt="Screenshot 2026-02-26 183831" src="https://github.com/user-attachments/assets/5b334c6f-8acf-464c-a6f0-506ab07f38bb" />
<img width="1889" height="1032" alt="Screenshot 2026-02-14 202550" src="https://github.com/user-attachments/assets/9fbc9242-3a6b-404a-bf43-6f617e98dcdb" />
<img width="1207" height="1004" alt="Screenshot 2026-02-26 190505" src="https://github.com/user-attachments/assets/079b024c-2f60-4637-8514-4c4b2118bd70" />
<img width="1320" height="1001" alt="Screenshot 2026-02-26 190440" src="https://github.com/user-attachments/assets/9a1f2f6c-101e-434b-9ce8-6be21e1d506a" />
<img width="555" height="603" alt="Screenshot 2026-02-26 190416" src="https://github.com/user-attachments/assets/a7cfffdb-671d-4d24-ba40-85ed89bd6d9c" />
<img width="198" height="395" alt="Screenshot 2026-02-26 190402" src="https://github.com/user-attachments/assets/ddc5ff5e-a1b6-4c49-ac2b-fa62bab99670" />
<img width="1883" height="903" alt="Screenshot 2026-02-26 190344" src="https://github.com/user-attachments/assets/2b1c1e58-e292-47a6-9ed1-3b0e7252f2f1" />
<img width="1870" height="911" alt="Screenshot 2026-02-26 190320" src="https://github.com/user-attachments/assets/3211f0ad-597a-4a32-b60b-b4e3f2285978" />
<img width="1877" height="918" alt="Screenshot 2026-02-26 190157" src="https://github.com/user-attachments/assets/bfadf4cc-fd33-4eb3-bfd4-4f7a2b3a616f" />



## 📁 Project Structure

```
Weather-forecast/
│
├── index.html          # Main application page
├── auth.html           # Authentication page (login/register)
│
├── app.js              # Main application logic
├── auth.js             # Authentication functionality
├── weatherMap.js       # Weather map integration
├── cities.js           # City database
├── translations.js     # Multi-language translations
│
├── styles.css          # Main application styles
└── auth.css            # Authentication page styles
```

## 🎯 Usage

1. **Authentication**: 
   - Visit the authentication page to create an account or log in
   - Use the credentials to access personalized features

2. **Search for Weather**:
   - Enter a city name in the search bar
   - View current weather conditions, temperature, humidity, wind speed, and more

3. **Explore the Weather Map**:
   - Navigate to the interactive map to see weather patterns across different regions

4. **Change Language**:
   - Select your preferred language from the language selector

## 🛠️ Technologies Used

- **HTML5** - Semantic markup and structure
- **CSS3** - Modern styling with animations and responsive design
- **JavaScript (ES6+)** - Application logic and interactivity
- **Weather API** - Real-time weather data integration

## 📦 Key Components

### app.js
Main application logic handling weather data fetching, display, and user interactions.

### auth.js
Manages user authentication, registration, and session handling.

### weatherMap.js
Integrates interactive weather mapping functionality.

### cities.js
Contains a comprehensive database of cities for weather lookup.

### translations.js
Provides multi-language support with translation strings.

## 🎨 Features in Detail

- **Current Weather Display**: Temperature, humidity, wind speed, pressure, and weather conditions
- **Forecast**: Extended weather forecasts
- **City Search**: Smart search with autocomplete
- **Weather Icons**: Visual representation of weather conditions
- **Dark/Light Mode**: Toggle between themes (if implemented)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

**Dineshkavitha2005**

- GitHub: [@Dineshkavitha2005](https://github.com/Dineshkavitha2005)

## 🙏 Acknowledgments

- Weather data provided by [Weather API Provider]
- Icons and design inspiration from various open-source projects
- Community contributors and testers

