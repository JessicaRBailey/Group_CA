# Popular Parks

##### An analysis of why certain national parks are more popular than others 

You might be surprised to know that not all national parks are created equal. There are wild differences in size, seasonal access, activities offered, wildlife, and weather. But one of the greatest differences between the parks is the average number of visitors each year. 

Here is some of the visitor data from National Parks in 2022

### Annual Visitors Per Park
![Annual Number of Visitors Per Park - Bar chart](https://github.com/JessicaRBailey/Group_CA/assets/23018536/7c9841fb-5d04-4d37-89f8-2c88720ceff6)

### Annual Visitors Per State
![Annual Parks Visitors per State - Bar Chart](https://github.com/JessicaRBailey/Group_CA/assets/23018536/6228fa24-5030-413d-8406-74a236c91533)

### Country Map With More Popular Parks Represented By Larger Dots
![Annual Visitors per State - Map](https://github.com/JessicaRBailey/Group_CA/assets/23018536/a8fcc6a8-e0bc-4d54-a216-78eb59daba58)

### Top 5 Most Popular Parks
![Top Five Parks with Most Visitors per Year - Pie Chart](https://github.com/JessicaRBailey/Group_CA/assets/23018536/f355c864-6613-4d83-9086-c18fbb55db87)

### Top 5 Most Popular States To Visit National Parks
![Top Five States with Most Visitors per Year - Pie Chart](https://github.com/JessicaRBailey/Group_CA/assets/23018536/f7a09cad-f2e1-48a8-9a3d-c301f75ecd4f)

### In an effort to understand why some parks are more popular than others, we set out to answer the following questions:

* Does the average temperature during a park's peak season (May-Sept) affect it's anual visitors?
* Does being near major cities draw more visitors into a national park?
* Do older, more historical parks, enjoy more anual visitors?
* Do larger national parks attract more overnight stays?

### Some Caveats
The national park system is comprised of almost 500 sites across all 50 states and teritories. Battle grounds, monuments, nature preserves, etc are all *managed* by the US National Park system, but are NOT national parks. For this research, we included ONLY sites with the  **National Park** designation. There are 63 of them in total

### The Tech Stack
This project is built with Python, using the following libraries
* Pandas
* Matplotlib
* Pyplot
* Scipy
* NumPy

### Local Environment Setup
Each file in this repo has the output already built in for easy viewing. However, if you'd like to clone this repo and run the code on your local machine, here's a list of prerequisites.
1. [Clone the repository](https://github.com/JessicaRBailey/Group_CA "Clone the repository") 
2. [Download and Install Python](https://www.python.org/downloads/ "Download Python")
3. [Download and Install Anaconda](https://docs.anaconda.com/free/anaconda/getting-started/index.html "Download and Install Anaconda")
4. Run `jupyter notebook` or `jupyter lab` from bash or terminal on your machine
5. Navigate to the Group_CA directory you've cloned on your machine.

### Special Thanks and Attributions
Data for this project comes from the following sources
* Select National Park Data Comes from the stats section of the the National Parks Service (https://irma.nps.gov/Stats/)
* National Park API data comes from the National Park API. Information on that can be found at https://www.nps.gov/subjects/developer/api-documentation.htm
* Airport API data comes from the TomTom API. Information on that can be found here: https://developer.tomtom.com/
* Weather data pulled from the Visual Crossings API. Information on that can be found here: https://www.visualcrossing.com/weather-api

# Project Results

## Does the average temperature during a park's peak season (May-Sept) affect it's anual visitors?

### Results
The average summer temperature does affect a park's popularity to some degree. Visitor numbers increase from below 60º to 
80º, and then taper off as the temperature rises above 80º

![Avg_Temp_Scatter](https://github.com/JessicaRBailey/Group_CA/assets/23018536/0be815bb-66ce-4012-93f8-35c27001568b)

![Temperature_Range_Box_Plot](https://github.com/JessicaRBailey/Group_CA/assets/23018536/b9b2ed65-813d-4356-bbec-6fcef40247db)

### Further Questions
In summer, the National Parks weather is remarkably similar, with the vast majority of parks enjoying temperatures between 60º and 90º - A range which suits visitors. However, average weather during January can range from -10º to 80º. As a result, some parks are open in winter. Perhaps a stronger correlation could be drawn using winter temperatures, rather than summer temperatures.

## Does being near major cities draw more visitors into a national park?

#### Assumptions Made
It's not always straightforward to determine what "being near major cities" means. For this analysis, a major city was one which had at least one international airport. And 'near' means within 300 miles. Essentially, we thought that if a visitor could drive to a park in a day, they might be more likely to visit that park.

### Results
There does NOT appear to be any correlation between a park's proximity to international airports, and it's popularity. Rocky Mountain National Park is near only one major city (and one intl airport), but is among the most popular. On the other hand, Channel Islands National Park is near 7 major cities (7 intl airports) and is one of the least visited national parks. 

![ParkVisitorsByAirport](https://github.com/JessicaRBailey/Group_CA/assets/23018536/877734ec-5183-43b7-ace7-4215d62c67f3)

### Further Questions
There are a number of flaws in this analysis.
1. 300 miles by car is very different than 300 miles by boat. Dry Tortugas is within 300 miles of a number of major cities, but to get there requires a private charter. A better methodology would be to only include parks with 300 highway miles of big cities
2. This methodology classifies all towns with an internatinal airport as a "big city". But this equates Atlanta, GA and Reno, NV - places with very different populations.

The intent of this question is "When people live around a national park, does it enjoy more visitors." To correctly answer this question, the acutal population data for the area around a national park should be considered. 

## Do older, more historical parks, enjoy more anual visitors?

### Results
There is a slight correlation between the age of a national park, and its annual visitors. The R-Value for this correlaion is .29 - which is weak, but still a relationship.

![Innauguration_vs_Popularity](https://github.com/JessicaRBailey/Group_CA/assets/23018536/2aee2a77-bdbc-48e7-aad0-f60bf20f6a3d)

However, with a p-value of 0.386, its likely a non-representitive sample and we cannot disprove the null hypotheses

## Do larger national parks attract more overnight stays?
National Parks vary widely in size. While Gateway Arch is around 91 acres, Wrangell-St. Elias national park is over 13 million acres. 

![Total_Area_of_National_Park](https://github.com/JessicaRBailey/Group_CA/assets/23018536/d158bcee-c307-479c-a690-904944f24fcc)

But does the size of the park affect the number of overnight stays by visitors? Here are the total number of overnight stays, by park. 

![Total_Overnight_Stays_by_NP](https://github.com/JessicaRBailey/Group_CA/assets/23018536/baec0389-9803-439f-8f4e-2aac0b7509e4)

![Top10 NP with Most Overnight stays](https://github.com/JessicaRBailey/Group_CA/assets/23018536/a406fb40-5f44-442a-b980-6ac50b4c42ff)

### Results
The analysis explored the relationship between park size and overnight stays in national parks. It found some connection, between the size of a park and the number of overnight stays. However, with a correlation coefficient of 0.02, a the correlation is small. 

![Area of NP vs Total # of Overnight Stays](https://github.com/JessicaRBailey/Group_CA/assets/23018536/831f1af9-88d0-46de-ba75-b64a18341f37)

Additionally, a statistical test comparing park size and overnight stays showed a significant difference. This suggests that other factors may have a greater impact on the number of overnight stays.

![t-test and P-value](https://github.com/JessicaRBailey/Group_CA/assets/23018536/094d4b07-ae3a-4b0b-8701-bea31e118508)

In conclusion, while larger parks may have the potential to attract more overnight visitors, the relationship between park size and overnight stays is weak. It's important to consider other influential factors when aiming to attract visitors to stay overnight in national parks.

## Do More Park Activities Attract More Visitors?

In our preliminary investigation, we found that differnt parks offer different activities to visitors. Some parks offer almost no activities, while others offer camping, tours, ATVing, stargazing, nature hikes, wildlife viewing, and dozens of other activities. So does the number of activities a park offers affect its number of annual visitors? 

Here is a chart showing the number of different activities that each National Park offers:

![ActivitiesperNationlPark](https://github.com/JessicaRBailey/Group_CA/assets/23018536/54c9e786-c441-477e-b57e-259d377ee525)

### Results
There is some connection between the number of activities a park offers and the number of annual visitors. However, with an rSquared of only .2, the correlation is weak. It is possible that more activities equal more visitors. But it does not appear as though the number of activities available in the park is a major driver of popularity.

![ActivitiesperNationlPark-1](https://github.com/JessicaRBailey/Group_CA/assets/23018536/39f97977-ba69-44da-9f29-49e5dd82a28d)

### Further Questions
It occurs to us that, while there is a weak correlation between park activites and number of visitors, it's not clear which variable determines the other. It is possible that visitors are lured to parks with more activities. However, it is just as possible that more visitors ALLOWS a park to offer more activities. 

Further research could isolate which variable drives the other for better clarity on the interaction between visitors and activities. 
