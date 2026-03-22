Movie Match
---
The Problem: "Choice Paralysis":
We’ve all been there—sitting on the couch for 30 minutes scrolling through Netflix, only to end up watching nothing because there are too many options. This project was born out of my own frustration with "Choice Paralysis." I wanted to build a tool that doesn't need a massive database of millions of users to work, but instead just looks at the DNA of a movie (its genre, plot, and director) to suggest something similar.

The Solution:
I built a Content-Based Recommendation System. Unlike "Collaborative Filtering" (which needs data from other people), this system focuses entirely on the item itself.
If you tell the program you liked Interstellar, it looks for other movies with tags like "Sci-Fi," "Space," and "Christopher Nolan" and calculates a Similarity Score to give you the best matches.

How It Works:
Instead of guessing what you like based on other users, this system uses Natural Language Processing (NLP) and Machine Learning to find similar items:
Feature Extraction: Combines Movie Tags, Genres, and Directors into a single text "profile."
Vectorization: Uses CountVectorizer to turn those text profiles into mathematical vectors.
Cosine Similarity: Calculates the "distance" between your favorite movie and the rest of the database. The closer the distance, the better the match.

Quick Start:
1. Requirements
Python 3.x
Pandas & Scikit-Learn

2. Setup
Bash
pip install pandas scikit-learn
3. Usage
Run python main.py and enter a movie title when prompted. The system will return the Top 5 most similar films.

Reflection:
The Challenge: Handling user typos. I had to implement a basic string-matching check to ensure the program didn't crash if a title was misspelled.
The Lesson: Data cleaning is 80% of the work. Ensuring the "Genres" and "Keywords" were formatted correctly was key to getting accurate recommendations.
