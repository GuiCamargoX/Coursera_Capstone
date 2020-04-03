# The Battle of the Neighborhoods
### Applied Data Science Capstone by IBM/Coursera

## Table of contents
* [Introduction: Business Problem](#introduction)
* [Data](#data)
* [Methodology](#methodology)
* [Analysis](#analysis)
* [Results and Discussion](#results)
* [Conclusion](#conclusion)


## Introduction: Business Problem <a name="introduction"></a>

**Compare the neighborhoods of Sao Paulo, Rio de Janeiro, Vitoria, Belo Horizonte cities** and determine how similar or dissimilar they are. After clustered their neighborhoods, we cluster once more grouping the cities. Therewith, it is possible to **compare which city is similar**. 

This project proposes helps foreign people to visit Brazil and also helps Brazilian people to move to similar neighborhoods.


## Data <a name="data"></a>

Based on the definition of our problem, factors that will influence our decision are the categories of each neighborhood using **Foursquare API**.

Following data sources will be needed to extract/generate the required information:
* explore each neighborhood city

## Methodology <a name="methodology"></a>

This project can be divided into 2 parts.

The first part is made of analyzing neighborhoods, following these steps:
1. Extract neighborhood from wikipedia - web scraping
2. Get the location of each neighborhood, using geocoder
3. Explore the points in a map - Folium
4. Now that we have our location, let's use Foursquare API to get info in each neighborhood.
5. Analyze each neighborhood - group rows by neighborhood and by taking the mean of the frequency of occurrence of each category
6. Save the new DataFrame into Folder Dataset. This will be used in part 2 of this project which will be to analyze the cities
7. Display the top 10 venues for each neighborhood
8. Run k-means to cluster the neighborhood into 5 clusters
9. Includes the cluster as well as the top 10 venues for each neighborhood
10. Compare the neighborhood by each cluster


Repeat the steps above for each city. The following notebook represents:
* DataBH - analyze neighborhood of Belo Horizonte, Minas Gerais ,Brazil
* DataES - analyze neighborhood of Vitoria, Espirito Santo, Brazil
* DataRJ - analyze neighborhood of Rio de Janeiro, Rio de Janeiro, Brazil
* DataSP - analyze neighborhood of Sao Paulo, Sao Paulo, Brazil


Part 2 consists of comparing similar cities.
After step 10, we have all neighborhoods clustered. To finish, we just need to group these clustered neighborhoods by cities and apply AgglomerativeClustering again. Just remember, the numbers found in the clustering neighborhood step are categorical variables.


## Results and Discussion <a name="results"></a>

As we expected, our analysis shows that Rio de Janeiro, Sao Paulo, Belo Horizonte belong to the same group. They tend to be more heterogeneous group. 

**We have to remember that this resultas are biased to which Foursquare API returns.** The recommended venues system is based on your friends suggestions and the numbers of venues returned. More venues returned, more precision you will have.

To more results, please check the notebooks files.


## Conclusion <a name="conclusion"></a>

Purpose of this project was to compare similar neighbours and cities in relation with venue categories. If you think to visit Rio de Janeiro, you should also visit Sao Paulo. 
It is possible to expand this project to all cities, creating a huge dataset. Then comparing itself.
