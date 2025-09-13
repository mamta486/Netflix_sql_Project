# Netflix Movies & TV Shows SQL Analysis

This project explores the Netflix dataset of Movies and TV Shows using PostgreSQL.
The aim is to answer real-world business problems such as popular content types, most common ratings, longest movies, top actors, and more.

📂 Dataset

The dataset used is: netflix_titles.csv

Column Name	Description
show_id	Unique ID for each show
type	Movie or TV Show
title	Title of the content
director	Director of the content
casts	Leading actors
country	Country of production
date_added	Date added on Netflix
release_year	Year of release
rating	TV rating (e.g., PG, R, TV-MA)
duration	Duration (in minutes or seasons)
listed_in	Genre
description	Short description
🛠️ Technologies Used

PostgreSQL (SQL queries)

CSV Dataset (Netflix titles)

🚀 Project Setup

Create the netflix table:

CREATE TABLE netflix(
  show_id VARCHAR(6),
  type VARCHAR(10),
  title VARCHAR(150),
  director VARCHAR(208),
  casts VARCHAR(1000),
  country VARCHAR(150),
  date_added VARCHAR(50),
  release_year INT,
  rating VARCHAR(10),
  duration VARCHAR(15),
  listed_in VARCHAR(100),
  description VARCHAR(250)
);


Load the dataset into PostgreSQL:

COPY public.netflix(
    show_id, type, title, director, casts, country,
    date_added, release_year, rating, duration,
    listed_in, description
)
FROM 'C:/temp/netflix_titles.csv'
WITH (FORMAT csv, HEADER true, DELIMITER ',', QUOTE '"', ESCAPE '"');

📌 Business Problems Solved

Count the number of Movies vs TV Shows.

Find the most common rating for Movies and TV Shows.

List all Movies released in 2020.

Find the Top 5 countries with the most Netflix content.

Identify the longest movie.

Find content added in the last 5 years.

Find all content by director Rajiv Chilaka.

List all TV Shows with more than 5 seasons.

Count number of content items in each genre.

Find each year and the average number of content releases by India (Top 5 years).

List all Movies that are Documentaries.

Find all content without a director.

Find how many Movies actor Salman Khan appeared in the last 10 years.

Find the Top 10 actors in the highest number of Indian movies.

Categorize content as Good or Bad based on keywords "kill" and "violence" in the description.

📊 Sample Insights

📈 Movies dominate Netflix compared to TV Shows.

🎭 The most common rating for Movies is TV-MA, while for TV Shows it’s TV-14.

🇮🇳 India is among the Top 5 countries with the most Netflix content.

🎬 The Irishman is one of the longest movies in the dataset.

🔎 Most content on Netflix is labeled as Good Content, with only a smaller portion flagged as Bad Content.

📌 How to Use

Clone this repo.

Import the dataset into PostgreSQL.

Run the SQL queries from the project file.

Explore insights for Movies & TV Shows.

👩‍💻 Author

Mamta Kumari

🚀 Passionate about Data Analytics, SQL, and Real-World Problem Solving
