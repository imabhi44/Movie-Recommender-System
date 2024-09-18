# Movie-Recommender-System
This project is a Movie Recommendation System that suggests similar movies based on content-based filtering, using cosine similarity to compare features of movies. The system also integrates with the TMDb API to display movie posters, enhancing user experience.
Name - Abhishek Kumar 
- Skills - Content-based Filtering, Cosine Similarity, API Integration (TMDb), Machine Learning, Data Processing, Data Science, Web Deployment
- Tools - Streamlit, Python, Pandas, Requests, Pickle, TMDb API, Jupyter notebook
# The Dataset:
The data was taken from Kaggle site :https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata  
The TMDb (The Movie Database) is a comprehensive movie database that provides information about movies, including details like titles, ratings, release dates, revenue, genres, and much more.
This dataset contains a collection of 5000 movies from the TMDB database.
## Data Preprocessing:
![image](https://github.com/user-attachments/assets/559b3e6b-5276-42b7-a735-ab4a9708e64e)
![image](https://github.com/user-attachments/assets/bb0ae535-6e1c-45d1-a145-655f45aff621)
# Feature Engineering
Some of the Features like "Genre","Keyword","Cast","Crew" contain unnecessary keyword like id,cast_id,crew_id and some other irrelevent names which is not helpful in our TAG creation, so I have fetched Only

- names of the Genre,
- Important keyword
- top three Cast members,
- Director name from the Crew

Here genre is string of list so first convert it into list of list and for that i have used ast Module of python so Initial genre-- '[{"id": 28, "name": "Action"}, {"id": 12, "name": "Adventure"}, {"id": 14, "name": "Fantasy"}, {"id": 878, "name": "Science Fiction"}]'

final output-- ['Action',"Adventure","Fantasy","Science Fiction"]
Same thing is applied on keyword
# Tag Creation:
We concatnate Overview, Genres, keywords, Cast and Crew to creat our tags. It will be a list so we have to convert it into string to get the whole paragraph so that we can apply NLP techniques
![image](https://github.com/user-attachments/assets/5f5f54e5-1c6a-4b6f-8749-4a454d3cd6cc)
# Text Preprocessing:
Applying Stemming

Stemming is a text preprocessing technique in natural language processing (NLP). Specifically, it is the process of reducing inflected form of a word to one so-called “stem,” or root form. example:- stem (loving, loves, loved) = "love"
It will reduce the problem of repetition of same words in different form

