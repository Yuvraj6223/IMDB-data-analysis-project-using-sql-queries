IMDB Data Analysis Project
Overview
This project involves analyzing the IMDB movie dataset using SQL queries. The goal is to extract meaningful insights and trends from the dataset, such as the highest-rated movies, most prolific actors, and common genres over the years.

Table of Contents
Project Overview
Data Source
Installation
Usage
SQL Queries
Results
Contributing
License
Data Source
The dataset used in this project is obtained from Kaggle, which contains detailed information about movies, including titles, genres, directors, actors, ratings, and more.

Installation
To run this project, you need to have the following installed:

Python 3.x
Jupyter Notebook
SQLite3
SQL Queries
The following are some of the SQL queries used in this project:

Highest Rated Movies:

sql
Copy code
SELECT title, rating
FROM movies
WHERE rating IS NOT NULL
ORDER BY rating DESC
LIMIT 10;
Most Prolific Actors:

sql
Copy code
SELECT actor, COUNT(*) as movie_count
FROM movie_actors
GROUP BY actor
ORDER BY movie_count DESC
LIMIT 10;
Common Genres Over the Years:

sql
Copy code
SELECT genre, COUNT(*) as genre_count
FROM movie_genres
GROUP BY genre
ORDER BY genre_count DESC;
Results
The analysis provides various insights, such as:

The top 10 highest-rated movies in the dataset.
The actors who have appeared in the most movies.
The most common genres in the dataset.
Contributing
Contributions are welcome! If you have any suggestions or improvements, feel free to open an issue or submit a pull request.

License
This project is licensed under the MIT License - see the LICENSE file for details.
