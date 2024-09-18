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
### Text Preprocessing:
- Applying Stemming  
- Converting Tags into Vectors   
### performed Cosine Similarity
Calculate cosine similarity between movies based on their genres, keywords, and overview to recommend the most similar ones.
![image](https://github.com/user-attachments/assets/daa9a5d0-d0c6-4217-82c3-fab608b2a20e)

**Logic to find the similar movies**
 1. First, we will find the index of the given movie.
 2. Then we will fetch the cosine similarity of that movie with others movies from similarity (array of array).
 3. we will short the cosine similarity valuee in Desc order by keeping the index intact and fetch top 5 values. 
    Movies corresponding to those values will be our output.
## RESULT:
![image](https://github.com/user-attachments/assets/1720db82-20bc-42dd-a573-e14adf8eb5a2)

### Converting our model into a website
Used the pickle module to serialize and save essential objects like the preprocessed movie data and the similarity matrix, which are key components of the recommendation system
![image](https://github.com/user-attachments/assets/5897a8d4-093e-40d8-a005-f075a1cf8e24)


    

