
<!-- HEADER -->
![Header Image](images/RT%20image.jpg)

<p align="center">
  <h1 align="center">Tomatometer Predictions:</h1>
  <p align="center">
     Predicting Tomatometer Scores with Movie Attributes
</p>

 ## Overview
This research is an attempt to help film studios in deciding which movies to green-light by using a tool that will predict the quality of a potential movie.  This tool will attempt to predict Tomatometer Rating and Tomatometer Status by using movie characteristics which would be known prior to a movie production starting.

## Data
 The final [dataset](datasets/movie_dataset.csv) used for this research was made by compiling together pieces of two different datasets found on Kaggle – [one](datasets/all_movie.csv) made from data scraped from Rottentomatoes.com and the [other](datasets/movie_metadata.csv) made from the Full MovieLens dataset.  
 
 Exclusions: All movies with a ‘Tomatometer Count’ of less than 100, meaning there are less than 100 ratings from critics for each of these movies, were excluded.  The purpose of this exclusion was to make sure that movies with very few reviews will not be counted towards the research.  Also, all movies with a null ‘Budget’ were excluded.  This reduced the count of movies in the final dataset to ~3,800 movies. 

 This final dataset will be used to research the predictability of Tomatometer Scores (ranging from 0 to 100) and Tomatometer Statuses (Certified Fresh, Fresh, and Rotten) for movies before production has begun.  This will be attempted through both Natural Language Processing and Machine Learning regression models.

 ## EDA
 The majority of the movies in the final dataset have a Rating of either ‘R’ or ‘PG-13’ and also fall into the Genre of ‘Action’, ‘Drama’, or ‘Comedy’.
 ![](images/Ratings_Genre.JPG)

 Most of the movies in the final dataset were created recently.  Using more recent data like this should help with identifying up-to-date trends in the data.
![](images/Release_Year.JPG)


Other EDA was performed to see if ‘Budget’ is an obvious predictor of either Tomatometer Rating (ratings from the critics or Audience Rating (ratings from average viewers).  However, there appears to not be much correlation:
![](images/Budget_vs_Tomatometer_rating.JPG)
![](images/Budget_vs_Audience_rating.JPG)


As would probably be expected, a strong correlation between ‘Tomatometer Rating’ and ‘Audience Rating’ can be seen:
![](images/Tomatometer_Rating_vs_Audience_rating.JPG)


When deciding whether to green-light a project, film studios consider who the leading actor/actress of the movie is.  While the ‘Cast’ data was ultimately not used in the predictive models because of very high cardinality, it is still interesting to view a breakdown of the highest and lowest rated actors/actresses in the dataset:
![](images/Top_10_highest.JPG)
![](images/Top_10_lowest.JPG)

