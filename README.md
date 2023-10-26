# github
This dataset is from the kaggle platform which was taken from : Zenodo
Zenodo is an open access data platform from the CERN European Organization for Nuclear Research
This dataset provides a comprehensive overview of Airbnb prices in some of the most popular European cities. This one will include 10 cities in Europe like Lisbon, London, Paris, Amsterdam etc.
To make this analysis more interesting I asked myself the following question:
Problematic: What is the best rental for a group of Parisian students going on a European vacation for 1 week.
Development:
Libraries installation / Datasets installation
I started by installing the libraries and datasets useful for my analysis
Vision of a dataset / Explanation of the columns
The dataset looks like this and I also explained the columns: we have in our possession for example the type of room, the cleanliness and satisfaction ratings, the number of rooms, the distance from the city center, and more.
I just want to add that the column ‘realSum’ is the price for 2 nights and 2 people.
Number of rentals per city
I first plotted the number of rentals per city to see how many apartments were presented in this dataset. I used a comprehension list
 (Example: there is more chances that the group of friends will find an apartment in London than Amsterdam because there are more apartments proposed in London)
Creation columns: weekdays or weekends & city / Gathering of all dataframes
I then created a week column (weekdays or weekends) and also a column of the name of the city to be able to gather all datasets together with the concat method. I also removed the datasets of Paris since we take into account the fact that they are Parisian students
So we can see that we have at the very beginning approximately 45 000 housing proposals
Prices
Here I wanted to see the distribution of housing prices in the city to determine the most likely city to have the expected housing. We do the hypothesis that students can’t pay a lot for the rent.
For this I made a histogram with price delimitation puted in a new column
Delimitation : - of 100, between 100 and 200, ... until 500 I used here the cut method
We can see here that it is Athens which proposes the most lodgings at less than 200€ that's why we will choose Athens to continue the analysis
We take Athens
I put the two datasets of Athens together: the fact that it's the weekend or the week doesn't matter because we assume that they leave 1 week
I did the median of prices in Athens and chose the rentals that are less than the median (here it’s 119€ for 2 days and 2 people.
Price < 119€

I filtered to keep only the lines where the rental price is less or equal to 119€.
Close to the city center:
I sorted the accommodations at 2km max from the city center by selecting the column "dist" and by putting less or equal to 2km
So we have now 1086 rentals
I used the same method for the rest:
Close to the metro (500 meters)
Number of people (they are 5 people)
We have now 27 recommendations
Suggest a good location (explains the graph)
I first looked at what kind of notes were given and made the average which was very high and that gave me the idea to project a graph
I used the violinplot method to have a better visualization
We can see on this graph that a lot of proposed accommodations have scores between 95 and 100 so we might as well filter to 100
So at the end we get 2 recommended homes that I represented thanks to folium
I would have liked to show the homes to you but there is nothing in the dataset to find the exact accommodations
