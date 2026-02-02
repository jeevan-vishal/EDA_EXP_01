### Name : Jeevan Vishal.G.D.
### Reg.No: 212224240062

## Experiment 1: EDA in IPL Dataset
## Aim:
To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.

## Algorithm / Procedure:

## 1.Import Libraries
  Import pandas for data handling.
  Import matplotlib and seaborn for visualization.
  
## 2.Load Dataset
  Use pd.read_csv() to load the IPL matches dataset.
  Check dataset shape using .shape.
  View first 5 rows using .head().
  
## 3.Matches per Season (Univariate Analysis)
  Group data by season and count matches.
  Plot a bar chart to visualize growth/decline in matches.
  
## 4.Top Winning Teams (Univariate Analysis)
  Use value_counts() on the winner column.
  Plot top 5 winning teams in a bar chart.
  
## 5.Toss Decisions (Univariate Analysis)
  Count toss decision preferences (bat vs field).
  Plot results using a bar chart.
  
## 6.Top Venues (Univariate Analysis)
  Count matches per venue.
  Display top 5 venues with a horizontal bar chart.
  
## 7.Draw Insights
  Observe patterns in toss decisions.
  Identify teams with consistent winning trends.
  
  
  ## Program
  ```
  ## 1.Dataset Structure  ( find the uploaded dataset matches.csv)

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
df=pd.read_csv('matches.csv')
df.head()

df.shape

matches_per_season = df['season'].value_counts().sort_index()
matches_per_season
import matplotlib.pyplot as plt

matches_per_season.plot(kind='bar')
plt.xlabel("Season")
plt.ylabel("Number of Matches")
plt.title("Matches Played per IPL Season")
plt.show()
top_teams = df['winner'].value_counts()
top_teams
top_5_teams = top_teams.head(5)

top_5_teams.plot(kind='bar')
plt.xlabel("Team")
plt.ylabel("Matches Won")
plt.title("Top 5 Winning IPL Teams")
plt.show()
toss_decision = df['toss_decision'].value_counts()
toss_decision

toss_decision.plot(kind='bar')
plt.xlabel("Toss Decision")
plt.ylabel("Count")
plt.title("Toss Decision Preference")
plt.show()
top_venues = df['venue'].value_counts()
top_venues.head(5)

top_venues.head(5).plot(kind='bar')
plt.xlabel("Venue")
plt.ylabel("Number of Matches")
plt.title("Top 5 IPL Venues")
plt.show()


df.shape

 ```
### output:

<img width="672" height="736" alt="image" src="https://github.com/user-attachments/assets/6c218d33-32f7-42d6-8f74-1c6d26341153" />
<img width="658" height="485" alt="image" src="https://github.com/user-attachments/assets/692336e0-a2a4-45ee-aa04-941f030952ce" />
<img width="638" height="616" alt="image" src="https://github.com/user-attachments/assets/823b8f32-3b5a-4295-84ff-9a8edd3f3c42" />
<img width="634" height="466" alt="image" src="https://github.com/user-attachments/assets/d2234fde-225b-416b-a340-dbb821e99e82" />




