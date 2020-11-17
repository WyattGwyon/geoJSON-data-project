Order of files

1- **First-Step-Using-Mongo.ipynb**
2- **Google_API_GeoCoding_Places.ipynb**
3- **geoJSON_and_Folium.ipynb**


# geoJSON Data Project

This project is going to take us through a search of possible locations for a new office for our avatar tech company. The company has provided certain guidelines for us to keep in mind for their ideal location. 


### Objective
We want to make the highest percentage of people happy. We have separated the company profile into three categories: 
- **Leadership:** CEO and Execs 
- **Work Force:** Desingers, Developers, and Engineers
- **Morale:** Maintenance worker and "Pepe" the office dog


## Priorities
Each sphere of interests needs to be given a different level of priority.

First, the "Leadership" have invested individually much more in the company than anyone else. They need to have a majority of their intersts met before making arrangements for the rest.

Second, and equally important, is the "Work Force". Leadership should express an interst in keep their workers happy. We are going to count their intersts parallel to Leadership's interests. Again, we want to make a majority of them happy.

Lastly, we consider "Morale" as the general attitude of everyone working involved. Considering that an unhappy maintance worker and absence of the office pet both would have considerable affect on the attitudes the everyone else, we have decided to treat them as representative of office moral which takes a very desirable but not necesary third place in our considerations.

# Break Down of percentages
## Sphere 1: ***Leadership***

- 10 Executives: 
    - **60%** of leadership
    - like Starbucks, A LOT!
- 1 CEO/President: 
    - **40%** of leadership
    - is Vegan

*(60% + 40% = 100%)*

---------

## Sphere 2: ***Work Force***

- 20 Designers
    - ***26.7%*** of work force
    - want design companies nearby
- 20 Account Managers
    - ***26.7%*** like to travel a lot .... near airport

- 15 Developers(Frontend and Backend)
    - ***20%*** like to be near tech startups that have raised at least 1 Million dollars<br>
    - 10 Frontend Developers
        - ***11.5%*** of work force
    - 5 Backend Developers
        - ***5.7%*** or work force
- 15 Data Engineers
    - ***20%***

- 5 UI/UX Engineers
    - ***6.7%*** of work force

---------

*(26.7% + 26.7% + 20% + 20% + 6.7% = 100%)*

## Sphere 3: ***Morale***
*(Bonus)*
- 1 Maintenance guy that loves basketball
    - wants to be 10 km near a basketball court
- Pepe, the office dog needs a haircut once a month
---------
---------


# First-Step: Use `companies` database to narrow down a location  
We want to look throug the "companies" database for the tech startups that have raised more than 1 Million dollars and then group them by city so that we can see what city has the highest number of successful tech companies. 

There is a a small problem with that because the field contains a string and not an integer. We might avoid trying to clean all data for the moment. 

We will first find U.S. companies and group them by city. Then count the instances of each category business which was founded in the las 10 years and have raised more than a million.

This should lay the ground work to limit the use of our APIs.

# Second Step: APIs are your `friend`.

We made a decision between San Fran, New York, and Los Angeles. All are great places, that could possibly meet our requirements. But we found a higher percentage of startups in Los Angeles. Two were E-commerce companies and another was a video-game company like ourselves. This gives us some good competition to take down!! And all three had raised significantly more than the start-ups in the other two cities.
 
Based on this and the fame of LA's Vegan friendly culture, we have determined to investigate prospects there. Now, we must get more specific with addresses and API requests to find the most convient place.



Our first API search is for a Starbucks. In our trials and tribulations, we discovered that was not a problem. The next requirement was a vegan restuarant and there were a great variety of options. The boss is gonna live that! 

Now with the needs satisfied *100%* for ***Leadership*** and *25%* for ***Work Force***, 
we decided it was high time to stop dilly-dallying and make a visulization of it all, on Folium.

# Further Investigation
To go beyond the work done here, we need to locate less numerous buildings such as schools for young'uns, distance to the airport for the bean counters, and maybe Design company or two nearby for the doodlers in the office who occasionaly like to stop wasting time in their place of work to go waste time in another's place of work. 

For this, we would have to modify our Google API formula. We read something somewhere about lazy progamming.... can't be bothered. 

Also, if we made deeper comparisons with other cities we might find more options to propose.

# Lessons Learned and Bumps in the Road

A few rudimentary debugging issues held up the process consedierably. They have been highlighted in the jupyter notebooks for posteriety. 


# Read Documentation
Start with First Step [here](/notebooks/First-Step-Using-Mongo.ipynb#Let's-go-to-LA-for-our-API-search.-There-should-be-no-problem-finding-some-vegan-restaurants-and-Starubucks-around-there!!!).

Next see the APIs [here](/notebooks/Google_API_GeoCoding_Places.ipynb)

Finish with the Visualization [here](/notebooks/geoJSON_and_Folium.ipynb)
