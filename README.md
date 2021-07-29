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
1. In Southern Hemisphere, max temperature increases with latitude increases. In NH, max temp decreases with latitude increases. As a general trend, the max temperature increases as we approach the equator. This is due to the fact the Earth is a sphere. There is a parabolic pattern for all temp vs latitude data for this same reason. The peak of this parabolic shape occurs around a latitude of 20-30 deg North because in July the Earth's Northern Hemisphere is in Summer and the Earth is tilted such that the sunlight penetrates the atmosphere more directly.
2. In Humidity vs Latitude plot, there are clear low humidity ranges centered around lats 30 and -30. This is because the North and South boundaries between the atmosphere's Hadley Cells and Mid-latitude cells, which are characterized by cool, dry, high pressure air. Hadley/ML cell boundaries occur on average at lats 30 and -30.
3. It is clear from the the cloudiness plots that there is low cloudiness range centered around lats -30 and 30. There are also high cloudiness ranges centered around lats 0 and 60. These high cloudiness ranges are correlated with the low pressure band formed at the boundaries between Polar cells and Mid-latitude cells, which occur at lat 60 and -60. There aren't many cities at lat -60 as it is mostly ocean, but if we were to look at cloudiness data for that area we would expect to see similar high cloudiness data. The existence of these cells and their boundaries makes a linear regression a poor choice for finding meaning in the cloudiness data, hence the low R-values for the regression lines.

## VacationPy

#### Purpose
The purpose of this python script is to use the weather data from WeatherPy to plan future vacations. The ideal vacation spot is found by narrowing down the options with given conditions.

The script creates a heat map that displays the humidity for every city from WeatherPy, then narrows down the weather data with the following conditions:
  * A max temperature lower than 80 degrees but higher than 70
  * Wind speed less than 10 mph
  * Zero cloudiness

Then the script uses the Google Places API to find the first hotel for each city located within 5000 meters of the coordinates and plots the hotels on top of the humidity heatmap, each with a pin.
