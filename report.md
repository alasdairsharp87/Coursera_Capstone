# Introduction
## The Problem
The fast paced, day-to-day grind of city living getting you down? Why not relocate to somewhere smaller?
In this project I am going to analyse the Foursquare data to compare the amenities available in Scotland's towns and villages, and compare them to the amenities available in the cities. This should allow me to cluster the towns based on which city they are most similar too.
## Target Audience
This project is aimed at providing an insight into the relative similarities between urban and rural life in and around Scotland, and would be relevant for anyone wishing to escape the cities for a quieter life in a smaller town while still enjoying similar amenities to what they are used to.
# The Data
For this project I am first going to extract the Foursquare venue data for the 6 cities (yes, we only have six) in Scotland - Dundee, Edingburgh, Glasgow, Inverness, Perth, and Stirling, and build up a profile for each city. I will then create similar profiles for the towns in Scotland with a population over 15000 [listed here](https://en.wikipedia.org/wiki/List_of_towns_and_cities_in_Scotland_by_population).
The towns will be assigned to clusters based on their similarities to the cities.
To adequately gain insight into the similarities, the venues will need to be grouped based on larger categories and the diversity within the category also calculated. For example, different types of restaurant will be grouped together but a measure will be taken based on how many different types of restaurant there are.
This can then be plotted on a Folium Map to show the distribution of the clusters across Scotland.
## Methodology
The stage of this project was to wrangle the data. The locality names, status and population were taken from [Wikipedia](https://en.wikipedia.org/wiki/List_of_towns_and_cities_in_Scotland_by_population). The latitude and longitude data was gathered from openstreetmap.org. And the venue data was extracted from Foursquare.
The venue data was then combined based on the venue type into 11 broader categories ('Locality', 'Restaurants', 'Bars', 'Entertainment', 'Culture', 'Shops', 'Transport', 'Sports', 'Nature', 'Accomodation', and 'Landmark') to allow the locailities to be more easily compared.
The dataframe was then divided into Cities and Towns, and a K Nearest Neighbour model was then created and trained on the City data. This model was then used to assign the towns to a cluster based on their similarity to a City.
These points were then plotted on a Folium map.
## Results
The 45 towns were only assigned to two of the six groups, Aberdeen and Dundee. When plotted on a map these showed more of the localitites on the west coast were in the Dundee group, and localities on the east coast were in the Aberdeen group.
## Discussion
The low distribution of the localities between the groups is likely due to the cities being significantly more diverse than the towns. The project may yeild more useful results if the analysis was based on individual factors rather than looking at all 11 categories together.
## Conclusion
The conclusions drawn from this project are project are unclear and it would likely have yeilded better results if I was to have looked at it the other way around, identifying which city was most like a town rather than the towns being like cities.
