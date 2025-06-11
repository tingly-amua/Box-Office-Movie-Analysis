# Data Analysis for a New Movie Studio Venture

![pexels-tima-miroshnichenko-7991579](https://github.com/user-attachments/assets/194591e7-9016-4062-b58c-4ed93fd149bd)

## Overview

This repository contains files partaining to a Box Office Movie Analysis to advise in the creation of a new movie studio. The analysis conducted within explores what types of films are doing best at the box office and uses these underlying traits to inform actionable insights for a new movie studio head.
The files contained include:
* Zipped Data - contains zipped datafiles from [Box Office Mojo](https://www.boxofficemojo.com/), [IMDB](https://www.imdb.com/), [Rotten Tomatoes](https://www.rottentomatoes.com/), [The Movie DB](https://www.themoviedb.org/), and [The Numbers](https://www.the-numbers.com/).
* Project.ipynb - which is a jupyter notebook with the data analysis conducted to address the business problem
* Images - contains the pictures used in this readme file
* Readme.md - the readme file highlighting the work done and results from the analysis
  
## Business Understanding
The stakeholder for this project is a new movie head seeking to establish a new movie studio. To guide our analysis, the following research questions were considered:
1. Genre trends: Which genres are most profitable?
2. Runtime, Ratings, and Revenue: Is there a correlation between rating or length and revenue?
3. Release Seasons(quarters 1, 2, 3, or 4): Which months do movies do best? 
4. Do movies with different content ratings have significantly different average ROI?
5. What is the impact of talent(actors, actresses, directors) on revenue generated?

## Data Understanding and Analysis
### Data Source
To perform our analysis, we unzipped the Box Office Mojo, The Numbers (TN), and the IMDB database files and placed them in the same folder as the notebook to be worked on. These datasets were most relevant to answering our research questions because they included the following information:
* Box Office Mojo - title, studio, domestic_gross, worldwide_gross, year
* IMDB Database - Movie basics table:  primary_title, runtime_minutes
                - Movie ratings table: movie_id, average_rating, num_votes
* The Numbers (TN) - movie, release_date, production_budget, worldwide_gross

### Tools & Technologies
The following tools and libraries were used in the analysis:

* Python: The main programming language used for data manipulation and analysis.
* Pandas: Essential for managing and cleaning the datasets.
* Scipy: Essential for statistical operations.
* Matplotlib & Seaborn: Used for visualizing data trends and insights.
* Jupyter Notebook: Served as the environment for conducting the analysis.

The data chosen detailed the movie names, the revenue they earned domestically and worldwide, the year released, movie length, their average audience rating, and release data. 
We loaded the 3 datasets using pandas and sqlite3 as shown:
![Screenshot (296)](https://github.com/user-attachments/assets/bfc0f234-57e4-41f0-8f01-fc1228f8cc50)

After cleaning and dropping null values, we merged all three datasets to form a combined dataframe for easier analysis, as shown below.

![cropped](https://github.com/user-attachments/assets/a6c16d9f-9bc0-4922-9461-b1faa70747a3)

This dataframe, created by the pandas package and the merge function was the main dataset that drove our visualizations and analysis. 

## Steps and workflow

### 1. Exploratory Data Analysis(EDA)
- Viewed tables in the IMDb database, box office dataset, The Numbers dataset .
- Understood layout of our data

### 2. Data  Cleaning
* Dropped null values from Box Office Mojo and IMDb basics datasets.
* Standardized movie titles (lowercase, trimmed) for accurate merging.
* Merged:

  * basics_df and ratings_df → movies_df
  
  * movies_df with Box Office and TN Movie Budgets → full_df

* Joined IMDb persons, principals, and movie_basics to gather talent info.

* Removed duplicates and missing values for clean, consistent analysis

### 3. Data Analysis
- Established research questions which are handled below:

## Visualizations 
### Answering Research Question 1: Genre trends: Which genres are most profitable?
By plotting Return on Investment ((Worldwide_gross - Production_Budget)/Production_Budget), we derived the following plot:
![Average Profit Margin by Genre Plot](https://github.com/user-attachments/assets/173c00de-b4d2-42e8-a06d-c01e249095e0)

We derived the following insight:
It shows that the Horror, Animation, and Thriller genres deliver the highest return on investment, thanks to low production costs and broad or loyal audience appeal.

### Answering Research Question 3: Release Seasons(quarters 1, 2, 3, or 4): Which months do movies do best?
By plotting release quarters by Worldwide_gross we obtained the following graph:
![Release Quarter graph](https://github.com/user-attachments/assets/5b7fc64d-0317-4c7a-bf41-b6cedce4a902)

We derived the following insight:
Movies released in Q2 and Q4 generate the highest revenue, making them the best seasons for maximizing box office success.

### Answering Research Question 5: What is the impact of talent(actors, actresses, directors) on revenue generated?
By plotting talents by revenue we obtained the graph below:
![d4644ca2-011b-4e87-a18d-db7328470939](https://github.com/user-attachments/assets/d64138ad-5815-411f-9f1c-10aaadb4b59c)

We derived the following insight:
* Top-grossing talent includes directors like Colin Trevorrow and Ryan Coogler (\$1.2B+), actors such as Chris Pratt and Ty Simpkins (\$1.6B+), and actresses including Lupita Nyong’o, Bryce Dallas Howard, and Judy Greer (\$1.2B+), all featured in billion-dollar blockbusters.

## Recommendations
Based on our analysis, we recommend:
1. Hire notable talent such as Colin Trevorrow (director), Chris Pratt (actor), and Judy Greer (actress) because they are in high grossing movies that exceed 1.2 billion worldwide.
2. Releasing movies in the second quarter of the year (April to June) since the studio is likely to earn more worldwide gross
3. Making movies in the Horror, Mystery, and Thriller genres because they generate more ticket sales and have higher average profit margins

## Conclusion
Despite being a competitive market, a new studio can make headway into the movie business by understanding release trends regarding year and dates, genres, and their impact on revenue. This notebook aids in that analysis by utilizing a jupyter notebook and Python in a clear and distinctive way that is easily reproducible.


<div align="center">
  <img src="https://github.com/user-attachments/assets/49027d7c-fecd-40e9-af17-11f201c647b2" alt="Horror movies">
</div>


If there are any questions regarding the coding steps, data sources, or analysis, feel free to reach out to our group leader or any of the other members through the following emails or individual github accounts:
* [Keith Tongi](https://github.com/Tkei-54) - keith.tongi@student.moringaschool.com
* [Kevin Karanja](https://github.com/tingly-amua) -  kevin.karanja@student.moringaschool.com
* [Jacob Abuon](https://github.com/abuonodindo2030) - jacob.abuon@student.moringaschool.com
* [Edna Maina](https://github.com/Julie-t) - edna.maina@student.moringaschool.com
* [Edgar Muturi](https://github.com/edgarmuturi) - edgar.muturi@student.moringaschool.com
* [Charity Mwangangi](https://github.com/CharityPM) - charity.mwangangi@student.moringaschool.com





