# Weather Analysis and Vacation Spots

- **_Weather Analysis_** - [WeatherPy.ipynb](WeatherPy/WeatherPy.ipynb) is a Jupyter Notebook that does a weather analysis on a set ~500 randomly selected cities via the citipy package (these cities are saved to a csv file for the below Vacation Spot). It uses the open weather api to collect current weather statistics on each of the cities selected. These cities are then applied to a series of scatter plots that compare latitude to 4 weather attributes, Max Temp, Humiditiy, Cloudiness, and Wind Speed. The analysis is further split into Northern and Southern Hemisphere scatter plots and then linear regression is applied on top.

- **_Vacation Spots_** - [VacationPy.ipynb](VacationPy/VacationPy.ipynb) is a Jupyter Notebook that uses the Google maps API to plot Humidity heat map for the city latitude and longitudes from the cities data file produced by the previous Weather analysis. The cities data is further filtered by a series of preferences on an ideal vacation location driven by selections based on Max Temp, Humidity, Cloudiness and Wind Speed. This filtered data is used against the Google places API to find the nearest Hotel to that target city latitude and longitude. A marker layer is then applied to the Humidity map to show those Hotels.

## Files

- Weather Analysis

  - [WeatherPy.ipynb](WeatherPy/WeatherPy.ipynb) - Jupyter Notebook for the Weather Analysis

  - [City Data](WeatherPy/output_data/cities.csv) - City data output file generate to be used by [VacationPy.ipynb](VacationPy/VacationPy.ipynb)

- Vacation Spots

  - [City Data](WeatherPy/output_data/cities.csv) - City data which was generated from [WeatherPy.ipynb](WeatherPy/WeatherPy.ipynb)

  - [VacationPy.ipynb](VacationPy/VacationPy.ipynb) - Jupyter Notebook for the Vacation Spots

## Results

- World City Max Temps

  ![Scatter Max Temp](WeatherPy/images/scatter_max_temp.png)

- World City Humidities

  ![Scatter Humidity](WeatherPy/images/scatter_humidity.png)

- World City Cloudinesses

  ![Scatter Cloudiness](WeatherPy/images/scatter_cloudiness.png)

- World City Wind Speeds

  ![Scatter Wind Speed](WeatherPy/images/scatter_wind_speed.png)

- Northern Hemisphere City Max Temp with Linear Regression

  ![Scatter Northern Hemisphere Max Temp](WeatherPy/images/scatter_nh_max_temp.png)

- Southern Hemisphere City Max Temp with Linear Regression

  ![Scatter Southern Hemisphere Max Temp](WeatherPy/images/scatter_sh_max_temp.png)

- Northern Hemisphere City Humidity with Linear Regression

  ![Scatter Northern Hemisphere Humidity](WeatherPy/images/scatter_nh_humidity.png)

- Southern Hemisphere City Humidity with Linear Regression

  ![Scatter Southern Hemisphere Humidity](WeatherPy/images/scatter_sh_humidity.png)

- Northern Hemisphere City Couldiness with Linear Regression

  ![Scatter Northern Hemisphere Cloudiness](WeatherPy/images/scatter_nh_cloudiness.png)

- Southern Hemisphere City Cloudiness with Linear Regression

  ![Scatter Southern Hemisphere Cloudiness](WeatherPy/images/scatter_sh_cloudiness.png)

- Northern Hemisphere City Wind Speed with Linear Regression

  ![Scatter Northern Hemisphere Wind Speed](WeatherPy/images/scatter_nh_wind_speed.png)

- Southern Hemisphere City Wind Speed with Linear Regression

  ![Scatter Southern Hemisphere Wind Speed](WeatherPy/images/scatter_sh_wind_speed.png)

- World City Humidity Heatmap

  ![Humidity Heatmap](VacationPy/images/heatmap_world_humidity.png)

- World City Humidity Heatmap with Hotel Marks

  ![Humidity Heatmap with Hotels](VacationPy/images/heatmap_world_humidity_marker.png)

## Analysis

## Execution

1. The assumption is that you have a working Python 3.6 environment and:

   - Jupyter Notebook 6.1.4
   - matplotlib 3.2.2
   - pandas 1.0.5
   - numpy 1.18.5
   - requests 2.24.0
   - scipy 1.5.0
   - citipy 0.0.5
   - gmaps 0.9.0

1. Clone the [`git repository`](https://github.com/jayhjman/python-api-challenge) for this project
1. Change into the [`repository directory`](https://github.com/jayhjman/python-api-challenge) and then into [`WeatherPy`](WeatherPy/)
1. In the `WeatherPy` directory create a file called `api_keys.py` and add the following 2 lines:

   - weather_api_key = "YOUR WEATHER API KEY HERE"
   - g_key = "YOUR GOOGLE MAPS API KEY HERE"

   Replace the values in the double quotes above with you version of the key you created in your source environments

1. Repeat the step above for the [`VacationPy`](VacationPy/) directory
1. Open up Jupyter Notebook now in the top level directory [`repository directory`](https://github.com/jayhjman/python-api-challenge)
   - Part I - Change directories in the Jupyter Notebook to [`WeatherPy`](WeatherPy/) and execute [`WeatherPy.ipynb`](WeatherPy/WeatherPy.ipynb) (Remember this must be done before Part II as `WeatherPy` produces a file `VacationPy` needs)
   - Part II - Change directories in the Jupyter Notebook to [`VacationPy`](VacationPy/) and execute [`VacationPy.ipynb`](VacationPy/VacationPy.ipynb)

## Author

Made by Jay with :heart: in 2020.
