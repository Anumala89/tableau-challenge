# citi-bike-analysis

Visualize the phenomena found in the Citi Bike Trip History logs

(The visualizations are available [here](https://public.tableau.com/profile/anumala1700#!/vizhome/Citibike_Data_Visualization/UsagebyAge?publish=yes).)


### Purpose

For this assignment I decided to focus on the use of Citi Bike in New York City at the beginning of the pandemic. Like any other means if transportation, the pandemic has affected Citi Bike in one way or another. But unlike other means of transportation, bike riding is an individual activity that prevents riders from close proximity. Keeping this advantage in mind, the citi bike has an upper hand in the transportation industry. According to the website [fortune](https://fortune.com/2020/06/15/bicycles-coronavirus-cities-lime-citi-bike/), the ride volume grew by 67% in early March. This suggests the potential of growth at larger scale in the future. Therefore, the time between March of 2020 to April of 2020 will be of main focus for my analysis with answers to the following questions:

* What stations were the most active (start and end) in New York City during the month of March-April 2020?

* What was the most common start-end stations in New York City during the month of March-April 2020?

* Which age groups and gender were the most active in New York City  during the month of March-April 2020?

* What was the busiest hours in New York City during the month of March-April 2020?


### Extracting

The very first step is to extract the data from the source. One way to do it is to download the files (csv files in this case) and the other way is using pandas and python. For this assignment the data were extracted from [Citi Bike Data](https://www.citibikenyc.com/system-data). All the process of extracting is described along with the code in the Data_Extracting.ipynb of this repo. 


### Cleaning

The next step was to clean the data so that any missing data or errors can be omitted for better results. For my analysis I first combined the logs for the month of March and April of 2020 into one file and then considering the facts of NYC traffic and assumptions based on those facts, I removed some of the rows and columns. At the end of the cleaning and sorting, I was able to reduce the number of rows by almost 24000 which was close to approx. 1.35% of the original data. All the process of data cleaning has been described along with the code in the Data_Cleaning.ipynb of this repo.


### Analysis

For the visualization we were to use [Tableau](https://www.tableau.com/), a software that makes it easier to create interactive visual analytics. Though the software is very efficient, it can be challenging if we are not familiar with the tools it provides. 

Citi Bike first launced its services on May of 2013 with 6000 bikes and has been growing ever since. By July of 2020 there were 100 Millionth trip recorded. The timeline of Citi Bike can be found [here](https://www.citibikenyc.com/about#:~:text=Citi%20Bike%20launches%20with%206000,stations%20throughout%20Manhattan%20and%20Brooklyn.). With the help of information provided by Citi Bike logs and Tableau, I was able to answer some of the queries that I had:

* **What stations were the most active (start and end) in New York City during the month of March-April 2020?**

During the month of March-April 2020, the station at West St & Chambers St was the most active station in New York City with over 10000 trips. The station at 12 Ave & W 40 St was the second most active station during that period. These places are close to some of the busiest area in the city. For example, the World Trade Center is within walking distance from the staion on West St & Chambers St. There is also the Metropolitian College, parks like the Hudson Park and the City Hall. Whereas, the station on 12 Ave & W 40 St is close to Lincoln Tunnel and Ferry that connects the city with New Jersey. 

Even during the time of lockdown, these places are hardly likely to slow down and being so close to the Hudson River people are likely to go there even for a breathe of fresh air. 

![Image](https://github.com/Anumala89/tableau-challenge/blob/main/Images/Start_station.png)

![Image](https://github.com/Anumala89/tableau-challenge/blob/main/Images/End_station.png)

* **What was the most common start-end stations in New York City during the month of March-April 2020?**

Not surprisingly the most active stations were also the most common origin-destination combinaion that riders took. There were more than 400 trips going to and fro from West St & Chambers St and 12 Ave & W 40 St. I would guess them being so close to the piers was one of the reason for it to be busy even during the lockdown when most of the businesses were shut down. 

![Image](https://github.com/Anumala89/tableau-challenge/blob/main/Images/Routes.png)

* **Which age groups and gender were the most active in New York City during the month of March-April 2020?**

64.88% of the riders were male, 26.01% were female and the rest 9.10% sex unknown. Among them, male in their early 30s were the most active riders followed by unkown in their early 50s. Female riders in their early 30s were also among the active ones. So the majority of the riders were in their early 30s (18.76%). A lot of people do not want to share their birth year for the reasons of privacy and also because of the growth of gender fluidity the data may not give us a defined age groups and gender of the riders.

![Image](https://github.com/Anumala89/tableau-challenge/blob/main/Images/Usage_Gender_Age.png)

* **What was the busiest hours in New York City during the month of March-April 2020?**

The busiest time was between 3pm to 6pm for most of the active age group (30 to 35). A lot of them were also riding during the lunch hours, though most of them were speeding during the early hours. Since the whole month of April was on lockdown, I believe the majority of the people going for ride after 3 pm were mostly for exercise. The other reason that might be is to avoid the crowd in the subway when a lot people are rushing to get back home from work. 

![Image](https://github.com/Anumala89/tableau-challenge/blob/main/Images/Usage_Age_by_hour.png)


### Limitations and Challenges

Even though with all the resources available it can still be a challenge to get an accurate outcome when working with such large data. The data itself can have some limitations which can either work in the favor of the user or against. While working on this assignment I came to realize that it is very easy to manipulate the information according to the user. 

* Data Limitations

One of the main limitation of the data was how the information of the rider was recorded. When I tried to create a visualization I came across various outliers like an 85 year old speeding at more than 20 miles per hour and number of 67 years old starting and ending at the same stations. It was pretty clear that people did not like sharing their personal informations.
There is a fluctuation on the rate of speed on my line graph because of the misleading ages of the riders. Even though there is an age restriction I doubt that it is being regulated efficiently. And also some of the repairs and maintenance were also recorded as trips. 

* Personal Challenge

The personal challenge that I faced were trivial but it was challenge nonetheless. There were memory issues on my personal computer and also I have a slow processing unit. The free account on tableau also limited the number of rows that I could work on which took sometime for the graphs and charts to load. One other challenges for me was to figure out what information to keep for the best result possible and what to omit. 