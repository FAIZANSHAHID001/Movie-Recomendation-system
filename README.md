# Movie-Recomendation-system
The following are the steps followed for this Movie Recomendation system
# Movie Recommendation System

# Step 1: Import Necessary Libraries
import numpy as np
import pandas as pd
import ast  **# Helps work with data in JSON-like format**
import nltk  **# A toolkit for natural language processing**
from nltk.stem import PorterStemmer  **# Helps simplify words to their root form**
from sklearn.feature_extraction.text import CountVectorizer  **# Converts text data into numerical form**
from sklearn.metrics.pairwise import cosine_similarity  **# Measures similarity between items**

# Step 2: Read and Merge Data
# We start by reading two CSV files containing movie information and credits.
film = pd.read_csv("tmdb_5000_movies.csv")
credits = pd.read_csv("tmdb_5000_credits.csv")

# Merging these datasets based on movie titles to create a comprehensive movie dataset.


# Step 3: Select Relevant Columns
 I choose the important columns from the merged dataset that we will use for recommendations.

# Step 4: Handle Missing Data
 I remove any rows with missing data to ensure our analysis is accurate.

# Step 5: Clean Data
 I clean and prepare specific columns like keywords, genres, and production companies for better processing.

# Step 6: Extract Directors
 I extract the director names from the crew information for later use.

# Step 7: Tokenize and Clean Text Data
Tokenize (split into words) and remove spaces from text data like overviews, genres, cast, crew, and production companies.

# Step 8: Combine Text Attributes
Combine various text attributes (overviews, genres, cast, crew, and production companies) into a single 'tags' attribute.

# Step 9: Apply Stemming
Reduce words to their root form using stemming to simplify text data.

# Step 10: Create a Main DataFrame
I create a main DataFrame with essential columns like movie ID, title, and 'tags' (the combined and processed text data).

# Step 11: Vectorize Text Data
I convert the 'tags' text data into numerical form using Count Vectorization, which represents words as numbers.

# Step 12: Calculate Cosine Similarity
Calculate cosine similarity between movies using the vectorized 'tags' data to find similar movies.

# Step 13: Recommendation Function
Create a recommendation function that takes a movie title and suggests similar movies based on cosine similarity.

# Step 14: Usage Example
Provide an example of how to use the recommendation function to find similar movies to 'Harry Potter and the Half-Blood Prince'.

# Step 15: Display Recommendations
Display the recommended movies for the given example.

# This code helps you build a basic movie recommendation system based on movie descriptions and other attributes.
