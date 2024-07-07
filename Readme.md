In this repository, we are going to show how to perform geocoding. Geocoding is a process of translating an address into coordinates.

We used a list of historical buildings in Ann Arbor, Michigan, USA. This list is in the book **[Historic buildings, Ann Arbor, Michigan](https://quod.lib.umich.edu/cgi/t/text/text-idx?c=moaatxt;idno=ANW1745.0001.001)**, by Marjorie Reade and Susan Wineberg.

To recreate this script, you should:

1. Create a virtual environment with all the dependencies. You can use the [requirements.txt](./requirements.txt) file.
2. Clean up and organize the [list](./list_buildings.txt). This part is important to avoid losing or creating any wrong address. The [first notebook](./1-list-buildings-organize-dataset.ipynb) has all the steps to do it.
3. Convert the addresses into coordinates. We used the geopy package to translate the addresses into coordinates. This part is in the [second notebook](./2-get-coordinates.ipynb). In our code, we tested the use of Google, Nominatim, and Photon. Some addresses did not appear in Nominatim and Photon. The reason is unclear, but it could be due to a lack of updates. For Google, you need to create a project in Google:
    - Obtain an API Key: You need to obtain an API key from the Google Cloud Console. Here's a quick guide on how to get started:
      - Go to the Google Cloud Console.
      - Create a new project or select an existing project.
      - Enable the Google Maps Geocoding API for your project.
      - Create an API key and restrict its usage to the Google Maps Geocoding API.
      - Be careful with the amount of data.
4. Create a Folium map to share the data in `.html`. All the steps are in the [third notebook](./3-plot-map.ipynb).
