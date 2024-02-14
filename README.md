# Yandex Weather API Analysis with Python

This repository contains scripts for fetching weather forecasts using the Yandex Weather API asynchronously and managing the data in a PostgreSQL database.

## Table of Contents

- [Scripts](#scripts)
- [Requirements](#requirements)
- [Usage](#usage)
- 
## Scripts

### 1. `fetch_weather` Function
- **Objective**: Asynchronously fetches weather forecasts for a given city from the Yandex Weather API.
- **Parameters**:
  - `session` (aiohttp.ClientSession): Session for making HTTP requests.
  - `api_key` (str): API key for accessing the Yandex Weather API.
  - `city` (dict): Dictionary containing city information (name, latitude, longitude).
- **Returns**: Tuple with the city name and a list of weather forecasts.

### 2. `get_weather_forecast` Function
- **Objective**: Asynchronously retrieves weather forecasts for multiple cities and writes the results to a CSV file.
- **Parameters**:
  - `api_key` (str): API key for accessing the Yandex Weather API.
  - `cities` (list): List of dictionaries containing information about cities.
- This function internally calls `fetch_weather` for each city and aggregates the results.

### 3. `main` Function
- **Objective**: Asynchronously executes the main program logic.
- It loads the Yandex Weather API key from environment variables, defines a list of cities, and calls `get_weather_forecast`.

### PostgreSQL Database Management Functions
- Functions for creating a Docker container with PostgreSQL, creating a database, connecting to the database, creating schemas and tables, and loading data from a CSV file into PostgreSQL.

## Requirements

- Python 3.x
- `asyncio` library
- `aiohttp` library
- `psycopg2` library
- Docker (for creating a PostgreSQL container)

Ensure you have Python installed on your machine along with the required libraries listed above.

## Usage

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/yandex-weather-api-analysis.git
