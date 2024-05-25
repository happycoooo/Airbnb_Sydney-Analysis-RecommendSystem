# Airbnb-Sydney-Analysis-RecommendSystem
# Contents
- [Visulization of maps](#visulization-of-maps)
    - [Cluster Map](#cluster-map)
    - [Average Price of Each Neighbourhood Map](#average-price-of-each-neighbourhood-map)
    - [Score Distribution Map](#score-distribution-map)
    - [Room Type Distribution Map](#room-type-distribution-map)
- [Word Clouds in Corpus of Texts](#word-clouds-in-corpus-of-texts)
	- [Word Cloud of Name](#word-cloud-of-name)
	- [Word Cloud of Description](#word-cloud-of-description)
- [Recommend System](#recommend-system)
# Visulization of maps
## Cluster Map
The map uses the Folium library to create an interactive map with markers clustered for better visualization.

The map shows that there are several high-density clusters of Airbnb listings within Sydney. Notably, the central business district (CBD) and surrounding areas show a significant concentration of listings. Besides, Bondi Beach and the surrounding suburbs show a high concentration of listings. This indicates that this area is a popular choice for travelers, likely due to its famous beach and vibrant atmosphere. 

While there are dense clusters in the central areas, the map also shows listings spread out across the greater Sydney region. This suggests a diverse range of accommodation options available to travelers, catering to different preferences for proximity to the city center or quieter suburban areas.

## Average Price of Each Neighbourhood Map
Geographic information about Airbnb neighborhoods in Sydney can be found on this website: https://citydata.be.unsw.edu.au/dataset/lgas_sydney_and_surrounds.

Based on neighborhood analysis, we've computed the average prices within each area. Interestingly, Mosman emerges as the most affluent neighborhood with the highest average price, followed closely by Woollahra in second place, and Willoughby securing the third spot. It's noteworthy that areas with missing data (NaN) have been represented transparently to ensure clarity in the comparison.

Based on neighborhood analysis, we've computed the average prices within each area. Interestingly, Mosman emerges as the most affluent neighborhood with the highest average price, followed closely by Woollahra in second place, and Willoughby securing the third spot. It's noteworthy that areas with missing data (NaN) have been represented transparently to ensure clarity in the comparison.

## Score Distribution Map
The map shows the distribution of Airbnb review scores across various areas in Sydney. Each marker represents a listing, and the color of the marker indicates the review score range according to the legend. 

#### Review Score Legend:
* Green (4.9 - 5.0): Highest ratings.
* Light Green (4.7 - 4.9): 
* Very high ratings.
* Yellowish Green (4.5 - 4.7): High ratings.
* Yellow (4.3 - 4.5): Above average ratings.
* Orange (4.0 - 4.3): Average ratings.
* Light Orange (3.0 - 4.0): Below average ratings.
* Red (Below 3.0): Low ratings.

A significant majority of listings are marked with green and light green colors, indicating that most Airbnb listings in Sydney have very high review scores (above 4.5). This suggests a generally positive experience for guests staying in Sydney.

The lower scoring listings (yellow, orange, and red) are sparsely distributed but can be found across various parts of the city.
Areas with a noticeable presence of lower scores include some parts of the inner suburbs and a few scattered in the outer suburbs.


## Room Type Distribution Map
The map shows the distribution of different types of Airbnb accommodations in Sydney, using different colored markers to represent various room types:

#### Room Types Legend:
* Green: Entire home/apartment
* Orange: Private room
* Red: Hotel room
* Blue: Shared room

The majority of room type are entire home or apartment, this may suggest that travelers prefer having an entire space to themselves, which offers more privacy and comfort. Private rooms are more evenly spread out compared to entire homes/apartments, indicating that this type of accommodation is popular in both central and suburban areas.

Shared rooms and hotel rooms are relatively uncommon on Airbnb in Sydney. Travelers may prefer the privacy of entire homes or private rooms over shared spaces.

# Word Clouds in Corpus of Texts
## Word Cloud of Name
The most frequently occurring words in the names or titles of listings include: Apartment, Studio, House, Room, Home etc. These terms suggest a variety of property types can cater to different preferences and group sizes.

Other words related to locations, such as Sydney, Beach, Harbour, and Ocean View, suggest that many properties emphasize their proximity to water or harbor views, which are appealing features for visitors.

## Word Cloud of Description

Guest expressions can be easily found as words like enjoy, perfect and beautiful etc. These words indicate that hosts focus on the overall guest experience, promoting a welcoming and enjoyable stay. Overall, the word cloud shows that Airbnb hosts in Sydney emphasize the comfort, convenience, and quality of their properties, highlighting key features and amenities.

# Recommend System
Use a Word2Vec model to process all text features appearing in reviewers' comments and the description/name/neighborhood overviews in the listings data. Combine all other features in the listings, and implement an interactive interface. Input a user ID to obtain the top five room IDs with the highest cosine similarity, and provide the corresponding room details links.