
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