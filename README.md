# Crime Trail Blazers
## Satvik Ajmera, John Byun, Shaymus McTeague, Kenneth Tanaka

### The Data
Fortunately for us, the data we needed was quite readily available as CSV files. Portland Trail
Blazers data was gathered from Kaggle [NBA Team Game Stats from 2014 to 2018](https://www.kaggle.com/ionaskel/nba-games-stats-from-2014-to-2018) (one CSV file)

Portland crime data was pulled directly from the Portland crime bureau website (Police Bureau, n.d.):
[Portland Crime Data](https://www.portlandoregon.gov/police/71978) (five CSV files from 2015-2019)

### Questions & Hypothesis
We analyzed the data for answers to the following questions in order to prove our main
hypothesis:
• What trends of crime do we see during the full NBA season, specifically, on game days?
• What is the total crime count per year in Portland?
• How do crime rates on non-game days compare to those of game days?
• Does it make a difference if those games are played home or away?


Hypothesis: If a Portland Trailblazers game takes place on a given day, then there will be a decrease in the rate of crime on that day.


### Data Cleanup

The NBA csv file was complete and contained data that was not pertinent to our project. The first steps required excluding all NBA teams except for Portland (POR). 
Date was reformatted using datetime, which allowed us to create a new column for the days of the week (DOW). Removed data that was not pertinent to the project (ex: free throws, rebounds, assists, turnover, et al.). The result was a file of dates, home and away games, wins and losses for the Portland Trailblazers.

We had initially tried to merge two crime files and quickly learned that was not correct when we were left with a csv file with 57 million rows. We concatenated to combine the crime files. After some analysis, we used ReportDate included crimes in previous years and so we chose to use OccurDate and reformatted using datetime. We restricted the crime dates for the project to January 1, 2015 - December 31, 2018. (The 2019 file was included in order to capture any crimes that had occurred in prior years but were not reported till 2019.)


### Visualizations & Observations
[Visual 1](Output/TotCrimeCountForEachYear-2.png)

This visualization showed the total crime count per month during the years 2015, 2016, 2017 and 2018. During every year, the total crime counts per month varied. During 2015, January, February, March and April showed an upwards trend in crimes. However, this is due to the Portland crime reporting measures during this time.

[Visual 2](Output/TotCrimeCountForEachYearfor3NBAseasons-3.png)

This visualization shows the total crime count per month for each NBA season. The visualization allowed us to eliminate the bad data during Jan, Feb, Mar and Apr 2015 and better represent the crime count per season.

[Visual 3](Output/AverageCrimeCountperTypeofGame-1.png)


[Visual 4](Output/AverageCrimeCountperDayoftheWeek-4.png)



AverageCrimeCountperTypeofGame(#1)