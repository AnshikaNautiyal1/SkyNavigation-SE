# Sky Navigation ✈️

A modern, interactive web application for aviation route planning and weather visualization built with React and Leaflet. This application provides real-time flight route calculations, air traffic visualization, weather information, and shortest path algorithms for optimal flight planning.

![Sky Navigation](https://img.shields.io/badge/React-19.0.0-blue)
![Vite](https://img.shields.io/badge/Vite-6.3.5-purple)
![Leaflet](https://img.shields.io/badge/Leaflet-1.9.4-green)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4.1.4-cyan)

## 🌟 Features

### 🗺️ Interactive Map

- **Leaflet-based mapping** with smooth zoom and pan controls
- Real-time airport location visualization
- Interactive markers for airports worldwide
- Custom map layers and overlays

### ✈️ Distance Calculator

- Calculate distances between any two airports
- Get estimated flight times
- Visual route display on the map
- Support for thousands of airports globally

### 🛫 Air Traffic Visualization

- Real-time air traffic monitoring
- Flight path tracking
- Airport congestion analysis
- Interactive flight information display

### 🌤️ Weather Information

- Current weather conditions at airports
- Weather forecasting for flight planning
- Integration with weather APIs
- Visual weather overlays on map

### 🛤️ Shortest Route Finder

- Dijkstra's algorithm implementation for optimal path finding
- Multi-stop route optimization
- Fuel-efficient route suggestions
- Alternative route calculations

### 📞 Contact & Support

- User feedback system
- Support contact information
- Feature request submission

## 🚀 Technologies Used

### Frontend Framework

- **React 19.0.0** - Modern UI library with latest features
- **Vite 6.3.5** - Lightning-fast build tool and dev server
- **React Router** - Client-side routing (if applicable)

### Styling & UI

- **TailwindCSS 4.1.4** - Utility-first CSS framework
- **Framer Motion 12.11.0** - Smooth animations and transitions
- **React Icons 5.5.0** - Comprehensive icon library
- **FontAwesome 6.7.2** - Additional icon sets
- **Lucide React 0.509.0** - Modern icon system

### Mapping & Visualization

- **Leaflet 1.9.4** - Interactive map library
- Custom map components for aviation data

### Data Processing

- **Papa Parse 5.5.2** - CSV parsing for airport data
- **Axios 1.9.0** - HTTP client for API requests
- Custom data utilities for airport information

### Development Tools

- **ESLint 9.22.0** - Code linting and quality
- **PostCSS 8.5.3** - CSS processing
- **Autoprefixer 10.4.21** - CSS vendor prefixing

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (version 16.x or higher recommended)
- **npm** (version 8.x or higher) or **yarn**
- A modern web browser (Chrome, Firefox, Safari, or Edge)

## 🛠️ Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/Achyut-shekhar/skyNavigation.git
   cd skyNavigation/skynavigation
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

   or if you prefer yarn:

   ```bash
   yarn install
   ```

3. **Verify installation**
   ```bash
   npm list
   ```

## 🏃‍♂️ How to Run

### Development Mode

Start the development server with hot module replacement (HMR):

```bash
npm run dev
```

The application will be available at:

```
http://localhost:5173
```

The dev server will automatically:

- Open your default browser
- Watch for file changes
- Hot reload when you save files
- Show compilation errors in the browser

### Production Build

Create an optimized production build:

```bash
npm run build
```

This will:

- Bundle all assets
- Minify JavaScript and CSS
- Optimize images
- Generate source maps
- Output files to the `dist/` directory

### Preview Production Build

Preview the production build locally:

```bash
npm run preview
```

This serves the built files from `dist/` directory at:

```
http://localhost:4173
```

### Linting

Run ESLint to check code quality:

```bash
npm run lint
```

Fix auto-fixable linting issues:

```bash
npm run lint -- --fix
```

## 📁 Project Structure

```
skynavigation/
├── public/                    # Static assets
│   └── images/               # Image files
├── src/
│   ├── assets/               # Project assets (fonts, images, etc.)
│   ├── components/           # Reusable React components
│   │   ├── ControlPanel.jsx  # Flight control interface
│   │   ├── FadeTransition.jsx # Animation wrapper
│   │   ├── Header.jsx        # Navigation header
│   │   └── Map.jsx          # Leaflet map component
│   ├── data/                 # Data files and utilities
│   │   ├── airports.csv      # Airport database
│   │   ├── airportsData.js   # Processed airport data
│   │   ├── DangerZone.js     # Restricted airspace data
│   │   └── transformed_airports_with_new_id.csv
│   ├── pages/                # Page components
│   │   ├── air_traffic.jsx   # Air traffic visualization
│   │   ├── Contact.jsx       # Contact page
│   │   ├── shortest_route.jsx # Route optimization
│   │   └── weather.jsx       # Weather information
│   ├── utils/                # Utility functions
│   │   ├── airportUtils.js   # Airport data helpers
│   │   └── dijkstra.js       # Shortest path algorithm
│   ├── App.jsx               # Main application component
│   ├── App.css               # Application styles
│   ├── main.jsx              # Application entry point
│   ├── index.css             # Global styles
│   └── animations.css        # Animation definitions
├── index.html                # HTML template
├── package.json              # Project dependencies
├── vite.config.js            # Vite configuration
├── eslint.config.js          # ESLint configuration
└── README.md                 # This file
```

## 🎯 Usage Guide

### 1. Distance Calculator

- Click on the "Distance Calculator" section
- Select source airport from the dropdown
- Select destination airport
- View calculated distance and estimated flight time
- See the route visualized on the map

### 2. Air Traffic Monitor

- Navigate to "Air Traffic" section
- View real-time flight positions
- Click on flights for detailed information
- Monitor airport congestion

### 3. Weather Information

- Go to "Weather" section
- Select an airport to view current conditions
- Check weather forecasts
- Plan flights based on weather data

### 4. Shortest Route Finder

- Access "Shortest Route" section
- Enter source and destination airports
- Optionally add waypoints
- Get optimized route suggestions
- View alternative routes

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the root directory for API keys:

```env
VITE_WEATHER_API_KEY=your_weather_api_key
VITE_FLIGHT_API_KEY=your_flight_api_key
```

### Vite Configuration

Modify `vite.config.js` for custom build settings:

```javascript
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";

export default defineConfig({
  plugins: [react()],
  // Your custom configuration
});
```

## 🐛 Troubleshooting

### Port Already in Use

If port 5173 is already in use, Vite will automatically use the next available port. You can specify a custom port:

```bash
npm run dev -- --port 3000
```

### Build Errors

Clear the cache and reinstall dependencies:

```bash
rm -rf node_modules dist
npm install
```

### Map Not Loading

Ensure you have a stable internet connection for Leaflet tile layers. Check browser console for errors.

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

**Achyut Shekhar**

- GitHub: [@Achyut-shekhar](https://github.com/Achyut-shekhar)

## 🙏 Acknowledgments

- [Leaflet](https://leafletjs.com/) for the amazing mapping library
- [React](https://react.dev/) team for the excellent framework
- [Vite](https://vitejs.dev/) for the blazing-fast build tool
- Airport data providers
- Weather API providers

## 📮 Support

For support, email achyut.shekhar@example.com or open an issue in the GitHub repository.

---

**Happy Flying! ✈️🌍**
