# BreezeBuddyy

## Live Demo
[Click here to try the Weather App live](https://breezebuddyy.netlify.app/)

## Overview
A client-side web application built with vanilla JavaScript, HTML, and CSS that provides real-time weather information based on user location or searched city. It consumes the OpenWeatherMap API to fetch weather data and presents it with a clean UI.

---

## Features
- Geolocation-based weather retrieval using browser's `navigator.geolocation` API.
- City-based weather search with real-time data fetching.
- Displays detailed weather parameters:
  - Temperature (°C)
  - Wind Speed (m/s)
  - Humidity (%)
  - Cloudiness (%)
  - Weather description and icon
  - Country flag fetched from FlagCDN
- UI state management:
  - Loading indicator during API calls.
  - Error handling with user feedback.
  - Tab switching between "Your Weather" and "Search Weather".

---

## Tech Stack
- **Frontend:** HTML5, CSS3, JavaScript (ES6+)
- **APIs:**
  - OpenWeatherMap API for weather data
  - FlagCDN for country flag icons
- **Browser APIs:** Geolocation API, Fetch API

---

## Architecture & Code Flow

### 1. Tab Switching
- Two tabs: User Weather and Search Weather.
- Clicking a tab toggles UI elements (`formContainer`, `userInfoContainer`, `grantLocationContainer`).

### 2. Location Handling
- On "Your Weather" tab, app checks `sessionStorage` for saved coordinates.
- If not found, prompts user to grant location access.
- Coordinates are saved in `sessionStorage` to prevent repeated prompts.

### 3. API Interaction
- Uses `fetch` with async/await.
- Requests weather data from OpenWeatherMap by:
  - Coordinates (`lat`, `lon`) or
  - City name.
- Handles HTTP and API errors gracefully.

### 4. UI Rendering
- Updates DOM elements with fetched weather data.
- Dynamically loads weather icons and country flags.
- Shows/hides loading and error states appropriately.

---

## Setup & Usage

### Prerequisites
- Modern web browser with JavaScript enabled.
- Internet connectivity to access external APIs.

### Running Locally
1. Clone the repository:

```bash
git clone https://github.com/Aditidevdhe/WeatherApp.git
cd WeatherApp
