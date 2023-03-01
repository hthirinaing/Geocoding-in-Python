# Geocoding-in-Python
Geocoding in Python with geopy

**Geocoding** is the process of converting addresses (e.g. a street or place address) into geographic coordinates (like latitude and longitude). You can geocode ***by providing a single place description at a time or multiple of them simultaneously in a table***. The output locations are geographic features with attributes that can be used for mapping or spatial analysis.

You can quickly find various kinds of locations through geocoding. The types of locations that you can search for include points of interest or names from a gazetteer, like mountains, bridges, and stores and addresses, which can come in a variety of styles and formats, including street intersections, house numbers with street names, and postal codes.

![Locations](https://nascenia.com/wp-content/uploads/2021/02/google-maps-track13.png)

In this tutorial, I will show you how to perform **geocoding in Python** with the help of Geopy library. Let's install these libraries with **Pip** if you have already Anaconda environment setup.

```
pip install geopandas
pip install geopy
```

**Geopy python library** can be used to geolocate a signle address.  Geopy has different Geocoding services that you can choose from, including Google Maps, ArcGIS, AzureMaps, Bing, etc. Some of them require API keys, while others do not need.

![This is image](https://user-images.githubusercontent.com/112382236/222022804-51ced65a-52d5-4214-bb4d-53a6fc016cd4.png)

### Geocoding single address

We will use Nominatim Geocoding service, which is built on top of OpenStreetMap data. Let's Geocode a single address, London Eye in London.

```
from geopy.geocoders import Nominatim
geolocator = geolocator = Nominatim(user_agent="myGeocoder")
location = geolocator.geocode("London Eye, London, UK")
```
```
print("Latitude = {}, Longitude = {}".format(location.latitude, location.longitude))
Latitude = 51.5033416, Longitude = -0.11967649999999999
```
