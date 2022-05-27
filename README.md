# Book Recommender System
* Created recommending system using **Content-Based** and **Collaborative Filtering** methods.
* Model based on dataset with 68588 ratings, 2000 users and 5007 books.
* Engineered the data for the project needs.
* Built function that prints recommended books to the console.

# Code and Resources Used
* **Python Version:** 3.9.7
* **Packages:** pandas, numpy, sklearn, matplotlib, seaborn
* **For Web Requirements Simply:** ```pip install -r requirements.txt```
* **Dataset from:** https://www.kaggle.com/datasets/ruchi798/bookcrossing-dataset

# Recommendation Examples
<img src="images/example3.PNG" width="400">  <img src="images/example1.PNG" width="500">

# Data Cleaning
After dropping columns not needed with each sample we have:
* user_id
* book_title
* rating
* book_author
* year_of_publication
* summary

The following changes to the dataset were made:
* The ratings with value of 0 were dropped as it seemed that they are supposed to be non ratings
* Calculated the number of ratings each movie received and limited the books to the ones with this value over 10.
* Calculated the number of ratings each user gave. Left top 2000 active users in the dataset.
* Some books had multiple summaries, because of several publications. That's why changed it so every sample have the same summary as it was needed for the content-base model bulding process. 

Summary of the dataset:\
<img src="images/data_summary.PNG">

## Exploratory Data Analysis

Some insights from data visualization:

**Rating Count Distribution** **Rating vs Number of Ratings**
* The most common rating give is about 8 out of 10
* There is very low number of ratings under 5    

<img src="images/rating_distt.PNG">

**Rating vs Number of Ratings**
* Very similar to the Rating Count Distribution
<img src="images/jointplot.PNG" width=400> 

**Most Frequently Rated Books** 

<img src="images/most_rated_movies.PNG">

**Top Rated Books**  

<img src="images/top_rated.PNG"> 

