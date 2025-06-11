# Data Analysis for a New Movie Studio Venture


![pexels-tima-miroshnichenko-7991579](https://github.com/user-attachments/assets/194591e7-9016-4062-b58c-4ed93fd149bd)

## Overview
This project was a collaborative effort from group 6 members in the Moringa School part-time data science bootcamp to ensure successful phase 2 completion.
The members are: 
* Charity Mwangangi
* Edna Maina
* Keith Tongi
* Jacob Abuon
* Edgar Muturi
  
This repository contains files pertaining to a Box Office Movie Analysis to advise in the creation of a new movie studio. The analysis conducted within explores what types of films are doing best at the box office and uses these underlying traits to inform actionable insights for a new movie studio head.
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

## Data Understanding and Analysis
### Data Source
To perform our analysis, we unzipped the Box Office Mojo, The Numbers (TN), and the IMDB database files and placed them in the same folder as the notebook to be worked on. These datasets were most relevant to answering our research questions because they included the following information:
* Box Office Mojo - title, studio, domestic_gross, worldwide_gross, year
* IMDB Database - Movie basics table:  primary_title, runtime_minutes
                - Movie ratings table: movie_id, average_rating, num_votes
* The Numbers (TN) - movie, release_date, production_budget, worldwide_gross

### Data Description
The following packages were imported to aid in this analysis:

* import pandas as pd
* import sqlite3
* import seaborn as sns
* import matplotlib.pyplot as plt
* import numpy as np
* from scipy import stats
* from scipy.stats import pearsonr

The data chosen detailed the movie names, the revenue they earned domestically and worlwide, the year released, movie length, their average audience rating, and release data. 
We loaded the 3 datasets using pandas and sqlite3 as shown:
![Screenshot (296)](https://github.com/user-attachments/assets/bfc0f234-57e4-41f0-8f01-fc1228f8cc50)

After cleaning and dropping null values, we merged all three datasets to form a combined dataframe for easier analysis, as shown below.

![cropped](https://github.com/user-attachments/assets/a6c16d9f-9bc0-4922-9461-b1faa70747a3)

This dataframe, created by the pandas package and the merge function was the main dataset that drove our visualizations and analysis. 

## Three visualizations (the same visualizations presented in the slides and notebook)
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

### Answering Research Question 4: Do movies with different content ratings have significantly different average ROI?
By plotting genres against average ROI we obtained the following plot:
![Boxplot of ROI by Movie Genre](https://github.com/user-attachments/assets/6c7f4aae-8f01-4d65-84d7-dc17b311c3cf)

We derived the following insight:
The boxplot reveals one genre that a much wider ROI range and higher median with many outliers(likely Comedy or Horror), while most genres cluster with low ROI, indicating limite profitability or higher risk.

## Conclusion
Despite being a competitive market, a new studio can make headway into the movie business by understanding release trends regarding year and dates, genres, and their impact on revenue. This notebook aids in that analysis by utilizing a jupyter notebook and Python in a clear and distinctive way that is easily reproducible.
Based on our analysis, we recommend:

1. Investing in the Horror genre because it has a much wider ROI range and is statistically significant compared to other genres
2. Releasing movies in the second quarter of the year (April to June) since the studio is likely to earn ore worldwide gross
3. Making movies in the Horror, Mystery, and Thriller genres because they generate more ticket sales and have higher average profit margins

If there are any questions regarding the coding steps, data sources, or analysis, feel free to reach out to our group leader or any of the other members through the following emails or individual github accounts:
* [Keith Tongi](https://github.com/Tkei-54) - keith.tongi@student.moringaschool.com
* [Kevin Karanja](https://github.com/tingly-amua) -  kevin.karanja@student.moringaschool.com
* [Jacob Abuon](https://github.com/abuonodindo2030) - jacob.abuon@student.moringaschool.com
* [Edna Maina](https://github.com/Julie-t) - edna.maina@student.moringaschool.com
* [Edgar Muturi](https://github.com/edgarmuturi) - edgar.muturi@student.moringaschool.com
* [Charity Mwangangi](https://github.com/CharityPM) - charity.mwangangi@student.moringaschool.com



