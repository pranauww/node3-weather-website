# Weather Website

## Overview
This is a simple **Weather Application** built using **Node.js**, **Express**, and **Handlebars** (hbs). The app allows users to input a location and retrieve real-time weather data, including temperature, feels-like temperature, humidity, and weather description.

The app uses two external APIs:
- **Weatherstack API** for fetching weather data.
- **Mapbox API** for converting location names to geographical coordinates (latitude and longitude).

## Features
- Get weather information for any location.
- Displays temperature, feels-like temperature, humidity, and weather description.
- Responsive user interface.
- Error handling for missing or incorrect locations.
  
## Getting Started

### Prerequisites
Make sure you have the following installed:
- **Node.js** (v12 or above)
  
### Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/weather-app.git
   cd weather-app
   ```

2. **Install the required dependencies**:
   ```bash
   npm install
   ```

3. **Create API keys**:
   - Sign up for a free API key at [Weatherstack](https://weatherstack.com/) for weather data.
   - Sign up for a free API key at [Mapbox](https://www.mapbox.com/) for geocoding services.
   
4. **Configure API keys**:
   Update the API keys in the `forecast.js` and `geocode.js` files

### Running the Application
1. **Start the server**:
   ```bash
   npm start
   ```

2. **Open your browser** and go to `http://localhost:3000`.

## APIs Used

### 1. Weatherstack API
Used to fetch real-time weather data.
- **Endpoint**: `http://api.weatherstack.com/current`
- **Parameters**:
  - `access_key`: Your Weatherstack API key.
  - `query`: Latitude and longitude of the location.

### 2. Mapbox API
Used to fetch the coordinates (latitude and longitude) of a location.
- **Endpoint**: `https://api.mapbox.com/geocoding/v5/mapbox.places`
- **Parameters**:
  - `access_token`: Your Mapbox API key.
  - `query`: Name or address of the location.

## Application Flow
1. **User Input**: The user enters a location (city, zip code, etc.) on the front-end.
2. **Geocoding**: The `geocode.js` script sends a request to the Mapbox API to get the latitude and longitude of the location.
3. **Weather Data**: The `forecast.js` script sends a request to the Weatherstack API using the obtained coordinates to fetch weather data.
4. **Response**: The weather data is displayed to the user, including the current temperature, feels-like temperature, and weather description.
