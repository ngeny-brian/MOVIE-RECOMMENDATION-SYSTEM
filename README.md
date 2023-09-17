# MOVIE-RECOMMENDATION-SYSTEM

> ### __Introduction.__
The movie industry has grown to be a multi-billion industry within the last century and with the advent of technology, It is expected to accelerate in growth. To date, there have been thousands of movies produced and released, meaning that there are so many options to choose from in terms of the genres, release periods and even just personal prefrences.

 This project is aimed at developing a movie recommendation system that will provide recommendations of movies specific to users based on their rating of other movies. This should help in eradicating the hurdle of choosing and deciding on their own what to watch from the numerous amounts of movies on offer today.

 > ### __Business understanding__.
The dataset was provided by GroupLens which is a research group in the Department of Computer Science and Engineering at the University of Minnesota. The dataset provides information necessary for developing and training a recommendation system that will be used for recommending movies to users based on their rating of other movies.

This project's target audiences are, streaming sites and movie enthusiasts who will nolonger have to worry about what to watch next because the resulting system will be able to recommend movies they might be interested in watching based on their rating of other movies. Streaming sites will also be able to attract more clients because of their competetive edge in being able to predict what a client might be interested in watching and recommending it to them.

> ### __Problem statement.__
With so many movies being released, the challenge now is to select what to watch. These has prompted me to come up with a solution in the form of a recommendation system for movies. By so doing, I hope to solve the problem faced by movie enthusiasts and online streaming companies by developing a system that recommends movies based on the rating given to other movies by users.   

> ### __Objectives.__
These primary objective of these project was to come up with a system that would be able to recommend movies to a user based on the ratings they have given to other movies. I explored the data provided and formated it approprietly so as to come up with a functioning system that could recommend five movies that a user is likely to be interested in.

The secondary objective was to build a model that uses content based recommendation to recommend movies to a user that are simillar to a particular movie within the dataset. These was a tentative solution for the cold-start problem whereby a user had not rated any movies yet but had an idea of the type of movies they are interested in. 

> ### __Data Understanding.__
This datasets contained in the ml-latest-small folder describes 5-star rating and free-text tagging activity from [MovieLens](http://movielens.org), a movie recommendation service. It contains 100836 ratings and 3683 tag applications across 9742 movies. These data were created by 610 users between March 29, 1996 and September 24, 2018. This dataset was generated on September 26, 2018. The folder contains `ratings.csv`, `tags.csv`, `movies.csv`, and `links.csv`.

> __Ratings.csv__<br>
These data file contains all the ratings of all the movies and has the following format;<br>
___userId,movieId,rating,timestamp___<br>

> __tags.csv__<br>
These data file contains all the tags applied to each movie by a user and has the following format;<br> 
___userId,movieId,tag,timestamp___<br> 
Tags are user-generated metadata about movies. Each tag is typically a single word or short phrase. The meaning, value, and purpose of a particular tag is determined by the user.<br>

> __movies.csv__<br>
These data file contains all the information about the movies and has the following format;<br> 
___movieId,title,genres___<br>

> __links.csv__<br>
These dtata file contains all the identifiers that can be used to link to other sources of movie data. It has the following format;<br> 
___movieId,imdbId,tmdbId___

> ### __Data cleaning.__

The next step was to clean the data acquired by digging deeper into each of the datasets so as to;

> I) Drop the columns we din't need.<br>
> II) Identify any missing values and drop the rows.<br>
> III) Engineer features or new columns where necessary.<br>
> IV) Merge datasets if necessary.

> ### __Exploratory Data Analysis.__
For these project, I utilised the ___movie_data___ and ___rating_data___ dataframes because they contain all the information necessary to build a recommendation system.

First, I analyzeed the ___movie_data___ dataset to discover the top ten genres of movies that are most prevalent within the dataset and the average rating of these genres of movies.

![Alt text](<Images/image.png>)

Finally, I analyse the ___rating_data___ data frame to determine the top ten highest rated movies that have been rated by atleast a hundred users.

![Alt text](<Images/image-1.png>)

> ### __Modelling.__

> ### __Model 1.__
The first model aimed to give recommendations of movies simillar to a given movie. I used the weighted avg of the ratings using cosine similarity as the weights. The movies which were more similar to the given movie will had a higher weight in the rating computation for the movie.
Overall the model appeared to perform well by recommending movies that were closely related to the given movie.

> ### __Model 2.__
The second model was going to give movie recommendations to specific users based on the movies viewed and rated by that user. The user was identified by their ___userId___. For these particular task, I used the pearsons correlation coefficients to determine the most suitable movies for the user. The model performed well and had the following scores;

* RMSE: 3.20
* MAE: 2.96

> ### __Conclusions.__
* Through the use of content based filtering, I was able to come up with a model that recommends ten movies to users that are simillar to a particular movie that a user chooses. These model is useful in recommending movies to users who are yet to make their prefrences known but are interested in specific movies and would like recommendations of simillar movies.

* In the second model, by using collaborative filtering, I was able to come up with a model that recommends five movies to a user based on the ratings that he/she has given other movies. These was the main objective of these project and it has been achieved with ___RMSE___ and ___MAE___ as the  evaluation metrics.

* The Exploratory Data Analysis revealed some useful trends pertaining to how people rate movies. Most of the users give a rating of between 2.5 and 3.5 to movies leading to an average of around the rating for very popular movies.

> ### __Recommendations.__
* Based on the ___RMSE___ and ___MAE___ values obtained, the next step I recommended with regards to building a better recommendation system, was to broaden the scope of analysis. A deeper dive beyond the rating of the movies is neccesary in order to better understand the preferences of individual users. 