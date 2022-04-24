# Movies-ETL

## Overview
In this project, the purpose is to create an ETL pipeline to extract, Transform and Load from various sources and integrate them to a single well-formatted dataset and Load it on a table in PostgreSQL.

Tow sources have been used in this project, one from [Wikipedia movies](https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-online/module_8/wikipedia-movies.json) with JSON format. And one from Kaggle. The [Kaggle dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset/download) pulls from the MovieLens dataset of over 20 million reviews and contains a metadata file with details about the movies from The Movie Database (TMDb).


## Procedure
First, a function has been written that reads in the three data files and creates three separate DataFrames. Then another function is used to extract and transform the Wikipedia data so you can merge it with the Kaggle metadata. At the same time, the IMDb IDs were pulled using a regular expression string and dropping duplicates, converting the transformed data into separate DataFrames. Next,  the Kaggle metadata DataFrame merged with the Wikipedia movies DataFrame to create the movies_df DataFrame. Finally, the MovieLens rating data DataFrame is joined with the movies_df DataFrame to create the movies_with_ratings_df. In the end, These three data sets were added to a SQL database.

![This is an image](/Resources/movies_query.png)
![This is an image](/Resources/ratings_query.png)
