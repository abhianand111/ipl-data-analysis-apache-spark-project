# IPL Data Analysis Project

## Overview
This project focuses on analyzing historical IPL (Indian Premier League) cricket data to gain insights into player performances, team strategies, and match outcomes. By leveraging PySpark and AWS S3 for data processing, along with Matplotlib and Seaborn for visualization, the project provides a detailed analysis of the IPL matches, including player statistics, team performance, and other key factors affecting the game.

## Dataset
The dataset used in this project includes multiple CSV files stored in AWS S3, comprising information on:

1. **Ball by Ball Data**: Contains details about every delivery bowled in each match, including the runs scored, extras, and wickets.
2. **Match Data**: Includes metadata about the matches, such as teams, venues, toss results, and match outcomes.
3. **Player Data**: Provides details about the players, including their names, roles, batting hand, bowling skills, and nationality.
4. **Player Match Data**: Contains match-specific player details, including performance data and age as of the match date.
5. **Team Data**: Information about the participating teams in the IPL.

## Technologies Used
- **PySpark**: For distributed data processing and analysis.
- **AWS S3**: For storing and loading data.
- **Matplotlib & Seaborn**: For visualizing results.
- **Pandas**: For data manipulation and conversions for visualization.
- **SQL**: For querying data from Spark DataFrames.

## Project Structure
The project consists of several key components:

1. **Data Loading and Cleaning**:

- Read CSV files from AWS S3.
- Define schema for the datasets (e.g., ball-by-ball, match, player data).
- Clean and preprocess data (e.g., handle missing values, filter relevant columns).
  
2. **Data Aggregation**:

- Calculate key metrics such as total and average runs per match, team scores, and player performances.
- Use PySpark SQL to perform complex queries for extracting insights.
  
3. **Feature Engineering**:

- **Running totals** for runs scored per over using window functions.
- **High impact events**: Identify impactful balls (e.g., boundaries, wickets).
- **Time-based analysis**: Extract and analyze data based on year, month, and day.
  
4. **Analysis and Visualizations**:

- **Top Scoring Batsmen per Season**: Identify the top scorers across different IPL seasons.
- **Economical Bowlers in Powerplay**: Analyze bowlers who performed best in the first six overs.
- **Impact of Toss on Match Outcomes**: Determine how winning the toss impacts match results.
- **Venue Performance**: Compare venues based on average and highest scores.
- **Dismissal Types**: Analyze the most frequent types of dismissals.
- **Team Performance After Toss**: Compare how well teams performed after winning the toss.

## Key Insights
- **Top Scorers**: Identified the leading batsmen in terms of total runs scored across various IPL seasons.
- **Economical Bowlers in Powerplay**: The analysis revealed the most economical bowlers during the first 6 overs of the game.
- **Impact of Toss**: Matches showed a clear correlation between winning the toss and winning the match.
- **Venue Analysis**: Certain venues were found to consistently produce higher scores compared to others.
- **Team Performance**: Teams like **CSK** showed significant performance improvements after winning the toss.

## Visualizations
The project also includes several visualizations for better understanding the data:

- **Economical Bowlers in Powerplay**: A bar plot showcasing bowlers with the lowest runs per ball in powerplay overs.
- **Toss Impact**: A count plot illustrating match outcomes based on toss winners.
- **Average Runs in Winning Matches**: A bar plot showing the average runs scored by top batsmen in winning matches.
- **Scores by Venue**: A bar plot comparing average scores at different venues.
- **Dismissal Types**: A bar plot showing the frequency of different dismissal types.
- **Team Toss Win Performance**: A bar plot showing how teams performed after winning the toss.

## Conclusion
This project successfully analyzes and visualizes IPL data, providing valuable insights into player and team performances. By using distributed data processing with PySpark, the project handles large datasets efficiently, making it a robust solution for sports analytics.
