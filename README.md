# movie_recommendation_system
I wanted to do a kernel in which I would make a recommendation engine, and chose the TMDB 5000 Movie Dataset dataset. Kaggle has removed the original IMDB version of this dataset per a DMCA takedown request from IMDB, and replaced it with a similar set of movies from The Movie Database (TMDb).

After some data preparation (the files provided contain JSON columns) and exploration, I did the following things:

First of all, I calculated a weighted rating for all movies. I used the formula that IMDB also uses for its ratings. This formula takes both the vote average and the number of votes into account (and a few other parameters).
I created a simple recommendation function that suggests 5 movies based on a selected genre and a selected language. Based on this input, the 5 movies with the highest weighted rating are suggested.
I also made a content-based recommendation function that requires a movie as the input. The function then suggest 5 movies based on similarity of the top3 actors, top3 genres, and the director. If multiple movies have the exact same number of similarities, they are ordered on descending weighted rating.
I have also worked on making recommendations based on similarity of the plots, but it turned out that the keywords provided seem much better than TD-IDF on the plots. The plots just seem too short for this purpose.
