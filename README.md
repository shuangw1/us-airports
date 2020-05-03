# Map of the US Airports
![us-airports](/assets/us-airports.JPG)
### :newspaper: Introduction

This is an interactive web map that marks all the airports in the United States. Green means there is a traffic control tower (CNTL_TWR) at this airport while black means not. I use purple-blue color (colorbrewer2.org) where darker purple indicates there are more airports in this state and lighter blue indicates there are fewer airports in this state. Users can click on the airport icon to see each airport's name and its three digit IATA code. The map can be accessed from [here](https://shuangw1.github.io/us_airports.github.io/).

### :mag_right: Data Resources
- `airports.geojson` contains all the airports in the United States. This data is converted from a shapefile, which was downloaded and unzipped from  https://catalog.data.gov/dataset/usgs-small-scale-dataset-airports-of-the-united-states-201207-shapefile.
- `us-states.geojson` is a geojson data file containing all the states' boundaries of the United States. This data is acquired from [Mike Bostock](http://bost.ocks.org/mike) of [D3](http://d3js.org/).

| **data file**      | **attribute** | **type of data** | **description** |
| ------------------ | ------------- | --------- | --------------- |
| airports.geojson   | AIRPRTX010    | Numeric    | airport tax |
| | ICAO | String | four-letter alphanumeric code designating each airport around the world, determined by International Civil Avian Organization.|
| | IATA | String | International Air Transport Association, the official trade organization for the world's airlines|
| | AIRPT_NAME | String | name of the airport in the U.S.|
| | CITY | String | the city within which the airport is located|
| | STATE | String | the state within which the airport is located |
| | COUNTY | String | the county within which the airport is located|
| | TOT_ENP | Numeric | the total number of passengers enplanned by one aircraft |
| | ELEV | Numeric | the elevation level of the airport above the sea level |
| | CNTL_TWR | Binary | the avaiilability of ATCTs where *Y* indicates availability and *N* indicates the otherwise |
| us-states.geojson | id | Numeric| identification number of the airport according to FAA. |                         |
| | name | String | name of the State where the airport is located |
| | count | Numeric | number of airports had by the state |

### :hammer: Process
- Code CNTL_TWR into two colors, for "Y" and "N"
- Code States into 7 colors.
- Add interactive element.


### :bulb: Analysis
It can be seen from the map that Alaska, California and Texas have the most number of airports. But the east coast airports have more traffic control towers, showing in green. Although Alaska has a lot of airports, but with few control towers, showing in black.

### :flags: Acknowledgement
This map is created by Shuang Wu, and is made with reference to a Web Map Design tutorial by Prof. Bo Zhao [read here](https://github.com/jakobzhao/geog458/tree/master/labs/lab03).
