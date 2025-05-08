World Cup Scoring Through the Years
================
by Taylor Curyto

## Summary

Write-up of your project and findings go here. Think of this as the text
of your presentation. The length should be roughly 5 minutes when read
out loud. Although pacing varies, a 5-minute speech is roughly 750
words. To use the word count addin, select the text you want to count
the words of (probably this is the Summary section of this document, go
to Addins, and select the `Word count` addin). This addin counts words
using two different algorithms, but the results should be similar and as
long as you’re in the ballpark of 750 words, you’re good! The addin will
ignore code chunks and only count the words in prose.

You can also load your data here and present any analysis results /
plots, but I strongly urge you to keep that to a minimum (maybe only the
most important graphic, if you have one you can choose). And make sure
to hide your code with `echo = FALSE` unless the point you are trying to
make is about the code itself. Your results with proper output and
graphics go in your presentation, this space is for a brief summary of
your project.

Dataset Description:
The dataset used comes from the TidyTuesday data project, specifically from the release dated November 29, 2022. The data was compiled from official FIFA records and other historical football match trackers. Each row in the dataset represents a single match played during a FIFA World Cup tournament. The dataset includes variables such as the year the match was played, the two teams involved, the number of goals scored by each team, the winning team, and additional contextual information such as location, tournament stage, and date. Key variables used for this analysis were year, home_team, away_team, home_score, and away_score.

To start the analysis, the dataset was transformed to a team-level format. This was achieved by creating a version of the data where each row represents a single team's performance in a match, including the number of goals scored. This restructuring allowed for comparison of total goals scored by individual teams across all tournaments, as well as year-by-year goal counts for each team.

Research Questions
The two central research questions that guided this project were:

Which team has scored the most goals in FIFA World Cup history?

How has scoring behavior evolved over the history of the tournament? Specifically, has there been a significant trend in total goals scored across tournaments?

Methodology
To answer the first question, total goals scored by each team across all matches were calculated by summing goals from both home and away performances. These totals were then sorted to identify the team with the highest cumulative goal count.

To address the second question, the total number of goals scored in each World Cup year was aggregated, and the data was visualized using a time series plot. Additionally, a linear regression model was fitted to evaluate whether there was a statistically significant trend in total goals scored over time. 

The regression output was then interpreted to assess whether the coefficient for year was statistically significant, indicating a meaningful upward or downward trend in goal scoring.

Findings
The results of the analysis clearly show that Brazil is the team that has scored the most goals in FIFA World Cup history, with a commanding lead of nearly 100 goals more than the next closest team. This confirms Brazil’s historical reputation as one of the most dominant footballing nations in the world. Their consistent presence in the tournament, long tournament runs, and high-scoring matches have all contributed to their record-breaking total.

To explore how scoring has changed over time, a linear regression analysis was performed on the total goals scored per tournament year. The regression results were statistically significant and are summarized below:

Year coefficient (β₁): 1.08

p-value for year coefficient: 1.15e-06

R-squared (R²): 0.72

The p-value for the year coefficient is less than 0.001, indicating a highly statistically significant result. The positive coefficient of 1.08 means that, on average, each subsequent tournament year is associated with approximately 1.08 more goals being scored. The R-squared value of 0.72 suggests that 72% of the variation in total goals can be explained by the year, further confirming the strength of the trend. Thus, this analysis supports the hypothesis that scoring in the World Cup has increased over time.

However, when examining goals scored over time by the top goal-scoring teams individually, including Brazil, the data did not show a clear or consistent trend. Instead, the number of goals scored by each team in each tournament fluctuated considerably, going up and down with no visible pattern. This suggests that while total scoring in the tournament overall has increased, individual team performance in terms of goal-scoring varies more significantly from year to year. These fluctuations are likely influenced by factors such as tournament format changes, team dynamics, player rosters, and strength of opposition.

Conclusion
In summary, this analysis demonstrates that Brazil is the highest scoring team in FIFA World Cup history, with nearly 100 more goals than any other nation. Additionally, there is a statistically significant trend of increasing goal totals across tournaments over time, with evidence pointing to a long-term rise in overall scoring behavior. However, this upward trend does not appear to hold consistently when evaluating individual teams, whose goal tallies fluctuate from tournament to tournament. These findings underscore the importance of examining both aggregate trends and team-level variation when studying historical performance in sports. This analysis provides meaningful insight into the continuation of the World Cup and offers a foundation for future studies on international football performance metrics.

## Presentation

My presentation can be found [here](presentation/presentation.html).

## Data

Include a citation for your data here. See
<http://libraryguides.vu.edu.au/c.php?g=386501&p=4347840> for guidance
on proper citation for datasets. If you got your data off the web, make
sure to note the retrieval date.

Rfordatascience. (2022, November 29). TidyTuesday: FIFA World Cup Matches Dataset [Data set]. GitHub. https://github.com/rfordatascience/tidytuesday/blob/master/data/2022/2022-11-29/wcmatches.csv

## References

Tidy Tuesday Project
