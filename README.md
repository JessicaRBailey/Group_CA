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

## Do More Park Activities Attract More Visitors?
