# Recommendation-system-on-movielen_dataset
Used different recommendation system in this project.
 The link of dataset is https://www.kaggle.com/datasets/grouplens/movielens-20m-dataset.
 
 The recommender system is fundamentally based on the MovieLens20M dataset. This consists, as the name suggests, of 20 million ratings performed by 38,000
users on 27,000 movies. In addition, a total of 465,000 tags were placed on the
content of the individual movies. The GroupLens Research Project has developed and made available various versions of the MovieLens dataset, but the
largest (20 million ratings) seems to make the most sense for this recommendation system, since the larger the datasets and thus ultimately the larger the
test set, the more precise and accurate the algorithms can be trained. In general, MovieLens datasets are one of the most used datasets to implement movie
recommender systems. This means that various results and their evaluations are
already available, which makes it easier to compare the results of this hybrid
approach at the end. The advantage of this dataset over other movie ratings
datasets is that it has the highest density of ratings. For example, if you have a
user with only one rating for a movie, it is difficult for the recommender system
to make a suitable prediction (due to the cold start problem). The movieLens
dataset will only include users if the user has rated at least 20 different movies.
It consists of the following seven files:
– movies.csv: This file contains information related to one movie in the following format: movieId, title, genres.
– ratings.csv: The rating file shows the ratings of one user according to one
movie. The format is: userId, movieId, rating, timestamp.
– tags.csv: Represents the single tags that an user has given to one movie.
– links.csv: This data can be used to link the dataset with the so called IMDb
dataset or the Movie Db dataset to add additional features to the MovieLens
data.
– genome-scores.csv: The file shows how relevant the given movie-tags are.
– genome-tags.csv: Provides the tag descriptions for the tag IDs.
One disadvantage of the MovieLens dataset is that it does not contain very
much information beyond the actual ratings. Therefore, only few features in
content-based filtering can be implemented for this dataset. For this reason we
supplemented the dataset with the IMDb [3] dataset using the link.csv file. The
IMDb dataset is a collection of different subsets in TSV format. Following subsets are contained: title.akas.tvs, title.basics.tsv, title.crew.tsv, title.episode.tsv,
title.principals.tsv, title.ratings.tsv, name.basics.tsv. In this project, only the files
title.crew.tsv and title.principals.tsv were used to implement additional contentbased features. The file title.crew.tsv contains information about the directors
and writers of a movie with its identifier tconst. The title.principals.tsv file, on
the other hand, provides details about the crew and the cast of the single movies.
To better understand how the individual data points of the movieLens dataset
are distributed, it is useful to first look at the visual representation of the data.
The first figure shows the distribution of the individual ratings from 0 to 5. The
left-hand side shows the entire dataset with 20 million entries. On the right-hand
side is a much smaller dataset with around 7.5 million entries. How this dataset
was created and why it is relevant to the project is explained in the preprocessing chapter. As can be seen from the graph, apart from the total amount, the
distribution of ratings is very similar across the entire datasets.
