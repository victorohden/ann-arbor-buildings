In this repository we are going to show how to geocoding.

The pourpuse here is translate a list of address to coordinates and plot it.

We used a list of the historical building in Ann Arbor, Michigan, USA. This list is in the Book XXXX ().

1- First: we create a venv and with all the dependencies.
2- We need to clean the [list](./list_buildings.txt) to build the address. This part is important to avoid the lose of create any wrong address.
3- We used geopy package to translate the address to coordinates. In our code we tested the use of Google, Nominatim and Photon. Some address did not appear in Nominatim and Photon. Not sure the reason, but could be some lack of updata. For google, you need create a project in Google 
    Obtain an API Key: You need to obtain an API key from the Google Cloud Console. Here's a quick guide on how to get started:

    Go to the Google Cloud Console.
    Create a new project or select an existing project.
    Enable the Google Maps Geocoding API for your project.
    Create an API key and restrict its usage to the Google Maps Geocoding AP
4- Create a Folium map to share the data in html