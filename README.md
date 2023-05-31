# Weather-Extraction
This project focuses on extracting weather data from Openweather API for a few cities of Nepal and storing that information in a database table.

## Tools Used:
i. PentaHo
ii. MS SQL SERVER
iii. Openweather API

## Files use case
### city_extraction.ktr
This tranformation extracts the list of 10 cities of Nepal from a json file containing the Openweather city information. It then saves the City_name, city_id (openweather specific identifier), longitude, and latitude as a dimension table in a MS SQL SERVER database.
### json_weather_transformation.ktr
This transformation loads the city data from saved dimension table, extracts the weather info using Openweather API, formats the response in tabular format from JSON format and stores this information as a fact table in the same MS SQL SERVER database.
### json_weather_info.kjb
This is the PentaHo job file that is used to schedule extracting weather info each hour and adding the information in the database.

The files **weather_transformation.ktr** and **csv_weather_info.kjb** perform similar action as above but instead of extracting the city information from JSON format, we explicitly provied the city information as a CSV file.
