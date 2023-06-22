# Business Problem

For this project, you have been hired to produce a MySQL database on Movies from a subset of IMDB's publicly available dataset. Ultimately, you will use this database to analyze what makes a movie successful and will provide recommendations to the stakeholder on how to make a successful movie.

Over the course of this project, you will:

* Part 1: Download several files from IMDB’s movie data set and filter out the subset of moves requested by the stakeholder.
* Part 2: Use an API to extract box office revenue and profit data to add to your IMDB data and perform exploratory data analysis.
* Part 3: Construct and export a MySQL database using your data.
* Part 4: Apply hypothesis testing to explore what makes a movie successful.
* Part 5 (Optional): Produce a Linear Regression model to predict movie performance. <br><br>

<img src = 'blue_long_2-9665a76b1ae401a510ec1e0ca40ddcb3b0cfe45f1d51b77a308fea0845885648.svg'>

## Part 1: Filtering

The following data has been downloaded, imported and cleaned as per the request of the stakeholder.
 
1. basics_url = 'https://datasets.imdbws.com/title.basics.tsv.gz'
2. ratings_url = 'https://datasets.imdbws.com/title.ratings.tsv.gz'
3. akas_url = 'https://datasets.imdbws.com/title.akas.tsv.gz'

## Part 2: Application Programming Interface and Exploratory data analysis

Financial data (json file) has been aded as a source 

1. tmdb = 'https://www.themoviedb.org/'

The data has been Extracted, Transform and Loaded (ETL). Finally, tested to see if the API function is working.

The following questions were answered for light EDA to show.

1. How many movies had at least some valid financial information (values > 0 for budget OR revenue)?
    - We have total of 638 data with valid financial information.
2. How many movies are there in each of the certification categories (G/PG/PG-13/R)?
<img src = 'EDA No of Movies.png'>
3. What is the average revenue per certification category?
<img src = 'EDA Average revenue.png'>
4. What is the average budget per certification category?
<img src = 'EDA Average Budget.png'>

## Part 3: MySQL

Made a MySQL database from the datas used in part 1 & 2. Transformed a total of 5 tables in my "movies" database.
1. title_basics
2. title_ratings
3. title_genres
4. genres
5. tmdb_data 

## Part 4: Hypothesis Testing

Statistics was done to answer the questions of the stakeholders. 

1. Does the MPAA rating of a movie (G/PG/PG-13/R) affect how much revenue the movie generates?

Hypothesis:
H0 (NUll Hypothesis) : MPAA rating of a movie does NOT have much effect the revenue of the movie.
H1 (Alternative Hypothesis) : MPAA rating have a significant effect on movie revenue.

2. Do movies that are over 2.5 hours (150 minutes) long earn more revenue than movies that are 1.5 hours(90 minutes) long (or less)?
3. Are some genres higher rated than others?