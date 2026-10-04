# IMDB Movie-Genres-Data-Analysis-Project
This is a course based project from Analyst builder. We analyze movie genre data determining the profitability and popularity of genres while testing hypothesis.
## Table of Contents
1. [Project Overview](#project-overview)
2. [Data Source](#data-source)
3. [Tools](#tools)
4. [Data Cleaning & Preparation](#data-cleaning-&-preparation)
5. [Exploratory Data Analysis](#exploratory-data-analysis)
6. [Data Analysis](#data-analysis)
7. [Results and Findings](#results-and-findings)
8. [Recommendations](#recommendations)
9. [Limitations](#limitations)


### Project Overview
This data analysis project aims to provide insights into the movie genre performance from 1960 to 2015. BY analyzing and answering set out questions and hypothesis, we seek to identify data driven trends and patterns and gain a deeper understanding of the movie entertainment industry.
<img width="1079" height="1002" alt="genre_popularity" src="https://github.com/user-attachments/assets/c1943fb9-0a68-46f2-879c-f5ddc70cefa3" />
<img width="1076" height="723" alt="profitability_genre" src="https://github.com/user-attachments/assets/b915e808-777e-4a15-86a3-2f014101a893" />
<img width="1099" height="522" alt="genre_popularity1" src="https://github.com/user-attachments/assets/c1329c6b-bff1-4a6b-8589-3b87798887b9" />




### Data Source
The primary dataset used for this analysis is the 'imdb_movies.csv' file containing detailed information about each movie produced from 1960 to 2015.The data is uploaded as part of the repository.

### Tools
In this project, I used Pandas for data cleaning, standardization, analysis and visualization

## Data Cleaning & Preparation
In the initial data preparation phase, we performed the following tasks:
1. Data loading and inspection.
2. Checking for duplicates
3. Handling missing values
4. Data cleaning and formatting for the genre column

### Exploratory Data Analysis
EDA involved exploring the sales data to answer key questions such as:
  1. Which genres are the most common?
     The top three genres are drama, comedy and action at 22.6%, 21.4% and 14.7% respectively.

  2. Which genres have a high avg profit?
     The top three genres with the highest average profits are as follows: adventure, science fiction and animation at $84.5 million, $54.5 million and $49.9 million respectively.

  3. Which genre has a high popularity?
     The top three popular genre are adventure, science fiction and fantasy. The top two popular genres are also the top two profitable genres.

### Data Analysis
After loading the data, i had to create a profit column using the code below:
``` pandas
df['profit']=df['revenue']-df['budget']
```
Further, I had to strip the genre column and pick the genre occurring at index zero using the code below:
``` pandas
df1['genres']=df1['genres'].str.split('|').str[0]
```

### Results and Findings
The analysis was used to test the following hypothesis:
1. Hypothesis 1: Movies according to vote avg return high profit and revenue
Hypothesis is rejected. Vote average has a minimal negative correlation with revenues and profits.
Looking closely at the vote count and popularity correlation with revenues and profits, the data suggests that the number of people watching movies is marginally more the the number of people watching the movies and voting.
Further, vote_count may occur after the movie such that the data on vote count may not have much impact on future revenues hence the lower correlation coefficient.
<img width="1060" height="411" alt="hypothesis1" src="https://github.com/user-attachments/assets/f8cbb0ae-8117-4f46-ae31-8452c9bcf278" />


2. Hypothesis 2: The best movies according to popularity return high profit and revenue
   Popularity is correlated with revenues and profits; 73% and 66% respectively. This hypothesis is consistent with EDA 2 and EDA 3.
   <img width="1113" height="371" alt="hypothesis2" src="https://github.com/user-attachments/assets/2e1cbe77-1659-4d01-980a-258e25061b7f" />


3. Hypothesis 3: Highly budgeted movies return high revenue and profit.
   There is a significant positive correlation to support the hypothesis.
   It is possible highly budgeted movies spend resources marketing the movies to attract a wider audience resulting in higher profit.
   <img width="1104" height="581" alt="hypotheis3" src="https://github.com/user-attachments/assets/59bf053d-f181-4fd1-bd34-156fbad1a65a" />


### Recommendations 
The analysis and recommendations are relevant to multiple players in the movie entertainment industry, from streamers, producers and actors.Based on the analysis, we recommend the following:
1. Streaming services and production houses should acquire more drama, comedy and action content to retain customers.
2. After retention, streaming services and production houses should produce adventure,science fiction and animation to boost revenue and profits. The bled of highly popular and most profitable genres will offer a wide variety that may lead to better customer experience and satisfaction.
3. Improve data collection tools to include gender and age for improved demographic analysis and mapping.

### Limitations
In the process of data cleaning, I had to remove duplicate rows that would have affected the accuracy of my conclusion from the analysis. The data also contained zero values in numeric data type columns which ultimately affect the quality of conclusion and analysis.







