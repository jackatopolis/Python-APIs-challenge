# Python-APIs-challenge
### By: Jack Cohen

## WeatherPy

#### Purpose
The purpose of this python script is to visualize the weather of 500+ cities across the world of varying distance from the equator. The goal is to model weather patterns as they relate to latitude. Data is extracted from OpenWeatherMap API and citipy library is used to find nearest cities.

The script creates a .csv file with the data from each city and creates/saves plots for the following relationships:
* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

The script separates weather data into Northern and Souther Hemispheres and creates/saves plots with linear regressions for the following relationships:
* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

#### Observable Trends
plus reasoning
1. adf
2. df
3. df

## VacationPy

#### Purpose
The purpose of this python script is to use the weather data from WeatherPy to plan future vacations. The ideal vacation spot is found by narrowing down the options with given conditions.

The script creates a heat map that displays the humidity for every city from WeatherPy, then narrows down the weather data with the following conditions:
  * A max temperature lower than 80 degrees but higher than 70
  * Wind speed less than 10 mph
  * Zero cloudiness
Then the script uses the Google Places API to find the first hotel for each city located within 5000 meters of the coordinates and plots the hotels on top of the humidity heatmap, each with a pin.

