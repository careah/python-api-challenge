# python-api-challenge


# VacationPy & WeatherPy

---

## VacationPy Overview

VacationPy is a Python script designed to assist users in planning their ideal vacation destinations based on preferred weather conditions. It utilizes weather data from the OpenWeatherMap API and geographical coordinates from the Geoapify API to create a customized map of cities with markers corresponding to their humidity levels. Additionally, VacationPy searches for nearby hotels using the Geoapify API and displays them on the map along with city information.

## WeatherPy Overview

WeatherPy is a Python script that analyzes the relationship between weather variables and latitude across various cities worldwide. It fetches weather data from the OpenWeatherMap API and uses matplotlib to create scatter plots comparing latitude with variables like temperature, humidity, cloudiness, and wind speed. The script also performs linear regression analysis for each relationship to determine the correlation strength.

## Prerequisites

To run VacationPy and WeatherPy successfully, ensure you have the following dependencies installed:

- `hvplot`
- `matplotlib`
- `pandas`
- `numpy`
- `requests`
- `scipy`

You will need API keys for the OpenWeatherMap API and the Geoapify API. Store these keys in the appropriate files (`api_keys.py`) for authentication.

## How to Use VacationPy & WeatherPy

1. **VacationPy: Import Libraries and Load Data**

   - Start by importing the necessary libraries and loading the weather and coordinate data from Part 1 into a Pandas DataFrame.

2. **VacationPy: Create a City Map**

   - Generate a map that displays a marker for every city in the `city_data_df` DataFrame, with the marker size representing the humidity level of each city.

3. **VacationPy: Narrow Down Ideal Weather Conditions**

   - Filter the `city_data_df` DataFrame to find cities that match your desired weather conditions based on criteria like maximum temperature, cloudiness, and wind speed.

4. **VacationPy: Create a Hotel DataFrame**

   - Generate a new DataFrame named `hotel_df` to store city, country, coordinates, humidity, and hotel name information.

5. **VacationPy: Find Hotels using Geoapify API**

   - For each city, use the Geoapify API to locate the first hotel within 10,000 meters of the city's coordinates. The hotel information is then added to the `hotel_df`.

6. **VacationPy: Visualize the Map with Hotels**

   - Create a map displaying cities along with the first hotel found within 10,000 meters of their coordinates. The map will include hotel names and country information in the hover message.

7. **WeatherPy: Import Libraries and Set Up**

   - Import the required libraries and load the API key for the OpenWeatherMap.

8. **WeatherPy: Generate Cities List**

   - WeatherPy uses the `citipy` library to generate a list of random cities based on latitude and longitude coordinates.

9. **WeatherPy: Retrieve Weather Data**

   - The script makes API calls to the OpenWeatherMap API to fetch weather data for the generated cities. It retrieves information like latitude, longitude, maximum temperature, humidity, cloudiness, wind speed, country, and date.

10. **WeatherPy: Create Scatter Plots**

   - WeatherPy generates scatter plots to showcase the relationships between latitude and weather variables (temperature, humidity, cloudiness, and wind speed). The plots are saved as PNG images in the `output_data` folder.

11. **WeatherPy: Linear Regression Analysis**

   - Perform linear regression analysis for each relationship to determine the correlation strength and display the regression line on the scatter plots.

## Running the Scripts

To run the VacationPy and WeatherPy scripts:

1. Ensure you have installed the required dependencies and obtained API keys for the OpenWeatherMap and Geoapify.

2. Execute the VacationPy script to plan your ideal vacation destinations and create the map with hotels.

3. Execute the WeatherPy script to analyze the relationship between weather variables and latitude and generate scatter plots with linear regression analysis.

4. The visualizations will be saved as PNG images in the `output_data` folder.
