# Coursera_Capstone
Applied Data Science Capstone

# Introduction

In May 2020, Elon Musk announced that Telsa would relocate its headquarters and future programs to Texas. While not the first to announce such a move, Telsa was perhaps the most prominent in the Silicon Valley tech firm exodus. The premier destination for the corporations is Austin, Texas the capitol of the state of Texas. Austin is a city home to 950,807 (2019) residents spread over 319.94 square miles. The city is growing in terms of diversity and boasts a large technology sector. On the departure side of this movement is the heart of Silicon Valley, the city of San Jose. San Jose has been the cultural, financial and political center of Silicon Valley and is the largest city in Northern California by both population and area. San Jose’s estimated 2019 population was 1,021,795 (2019) making it the tenth most populous city in the United States. The city of San Jose encompasses 178.24 square miles.   

Part of the ongoing narrative regarding Austin, Texas is that the city is not only more accommodating for tech companies but also for employees and people in general.  This capstone project will explore the differences in the neighborhoods of both cities and make a comparison based on the common nearby venues. How much truth is there that the two cities are similar? This information would prove to be valuable for any individuals contemplating moving. 

#Data 

The data sources for this project. 

https://www.sanjose.org/neighborhoods

https://www.homecity.com/blog/best-neighborhoods-in-austin/

Foursquare API

https://www.google.com/maps

GeoPy


#Data Sourcing and Cleaning
 
 The data set used for San Jose is from the city of San Jose’s website that lists the various neighborhoods which loosely follow the city’s zip codes.  The data set used for Austin is from a real estate website which rates neighborhoods within the city limits. Beautiful soup was used to extract the neighborhood names and Geopy Nominatum was used to determine the Geo coordinates. However some of the Geo coordinates were inaccurate and need to be manually replaced. I used google maps to locate the correct Geo coordinates and update the Dataframe. Once the neighborhoods had the correct coordinates the datasets were ready to source the venue data from Foursquare.
  Austin   San Jose

#Methodology 

Once the data sets were cleaned, the neighborhoods were marked on folium maps of both cities. In doing so provided a visual context of the location of the different neighborhoods as well as confirmation that the location was correct. All neighborhoods were processed through Foursquare API to generate the nearby venues in each neighborhood. The Foursquare parameters were 500 meters and a limit of 100 venues per search (neighborhood). The data was transformed to show the top ten common venues in each neighborhood in terms of frequency. Then neighborhoods were clustered and labeled. The optimal number of clusters was determined by K-means. The elbow method was used once the points were graphed. The number of clusters seemed to be 5 clusters for San Jose and 4 clusters for Austin. The neighborhoods were mapped again this time with the color coded clusters and the maps were able present a visual of the dominant types of venues in each neighborhood.
  


#Results 

   
Five clusters were set for San Jose, 14 of 17 neighborhoods were clustered in label 1, the remaining minority clusters have one neighborhood each. The top venue for the San Jose minority clusters is Café, Park, Financial or Legal Service, and Cocktail Bar.  Label 1 was centered on food and entertainment. Four clusters were set for Austin,   14 of 18 neighborhoods were clustered on label 0, the remaining minority clusters have 1 neighborhood with one cluster having 2 neighborhoods. The top venue for the Austin minority clusters is Pizza Place, Financial or Legal Service, Food stand, Vietnamese Restaurant.

#Discussion

The largest clusters in both cities include similar venues types whose categories are centered on food and entertainment. In both cities Mexican food has a strong presence; in San Jose five neighborhoods have Mexican Food as the 2nd and 3rd most common venue. Austin has six neighborhoods with Mexican Food as the 2nd , 3rd , and 5th most common venue. In both cities, Asian food also has a nearly identical presence; two neighborhoods have Japanese and Vietnamese cuisine as 1st most common venue, then Thai, Hawaii, Chinese make appearances in the subsequent most common venues. 
Both Cities have a (1st most ) café/coffee centric neighborhoods and a light rail system (2nd and 3rd).   That Austin and San Jose would share similar venues is not unexpected. The demographics for both cities have a high percentage of Latino residents (35.1% Austin 33.2% San Jose). Interestingly is how the Japanese cuisine and Vietnamese cuisine are the most common venues in two Austin neighborhoods. While Austin’s Asian population has doubled from 3% to 6% since 1990 to 2010 is still far below San Jose’s 32%.  Both cities have similar infrastructure in having an airport, light rail station, and university. 

#Conclusion

This comparison certainly provides some insight on the nature of the neighborhoods but it definitely fails to capture all aspects of each city that one might want to factor in prior to moving.
One example is that Austin has world renowned barbeque venues. Yet this is not captured in the foursquare data.  Perhaps these venues are spread out too much to constitute a most common venue.  In contrast for San Jose, one would expect a higher number most common venues of Asian cuisines in the neighborhoods. However, there are only two San Jose neighborhoods with Asian cuisines as their 1st most common Venue and predictably enough those neighborhoods are Little Saigon and Japantown. One factor might be that most Asian venues tend to congregate next to one another. 
Lastly it is also important to point out that Silicon Valley is not just San Jose but rather the entire peninsula from San Francisco to San Jose. The entire route is populated with small suburban to mid-sized cities. Many of these cities have their own demographics that may vary from San Jose’s and result in their own unique venues. Austin maybe roughly one hour from San Antonio but the route is not as populated with cities. If one were to consider leaving the Bay Area for Austin they may want to include more cities along with San Jose in their comparison analysis.

 
