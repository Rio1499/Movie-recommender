# Movie Recommender System

This repository contains code for a Movie Recommender System implemented in Python using collaborative filtering techniques.

## Overview

The Movie Recommender System uses data from the 'tmdb_5000_movies.csv' and 'tmdb_5000_credits.csv' files to suggest movies based on user preferences and movie features.

## Steps

1. **Data Preparation:** 
    - Read and merge the movie details and credits datasets.
    - Clean the dataset by handling missing values and duplicates.

2. **Feature Selection:**
    - Select essential columns like 'movie_id', 'title', 'overview', 'genres', 'keywords', 'cast', and 'crew'.

3. **Data Transformation:**
    - Convert stringified lists in columns like 'genres', 'keywords', 'cast', and 'crew' into actual lists.
    - Extract relevant information from columns like 'cast' and 'crew' to retain top actors and directors.

4. **Tag Creation:**
    - Create a 'tags' column by combining movie features like 'overview', 'genres', 'keywords', 'cast', and 'crew'.
    - Stem words and convert the 'tags' column to lowercase.

5. **Vectorization:**
    - Use CountVectorizer to convert 'tags' into numerical vectors to prepare for similarity calculation.

6. **Similarity Calculation:**
    - Utilize cosine similarity to calculate similarity scores between movies based on their 'tags'.

7. **Recommendation Function:**
    - Create a function to provide movie recommendations based on user input (e.g., 'Batman Begins').
    - Utilize the similarity scores to suggest similar movies.

8. **Saving Model:**
    - Save the processed data and similarity matrix using pickle for future use.

## Usage

To use the Movie Recommender System:
- Ensure the required dataset files are available ('tmdb_5000_movies.csv' and 'tmdb_5000_credits.csv').
- Execute the code provided in the Jupyter Notebook 'movie-recommender-system.ipynb' to generate recommendations.

## Files Included

- `movie-recommender-system.ipynb`: Jupyter Notebook containing the Python code for the Movie Recommender System.
- `movie_dict.pkl`: Pickle file containing processed movie data.
- `similarity.pkl`: Pickle file containing similarity matrix.

## Note

- The code provided here covers the data preprocessing, transformation, model creation, and recommendation functionalities.
- Modify and expand the code as needed to enhance the recommender system or adapt it to different datasets.

