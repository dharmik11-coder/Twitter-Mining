# Twitter-Mining

In this project tweets from the Twitter social media platform were used to estimate the date and time of a UCL match.

The possiblity to determine the date and time of an event accurately within a few hours of the
actual occurrence using the social media data was the challenge here where our work suggested yes, it is possible. For UCL matches we were able to determine kick-off
time of 26/32 (81.25%) matches within a 3-hour window.

The most common way to tag a match in tweets is to use hashtags with 3-letter names of the teams with the home-team’s name first, e.g. OLY vs MCI will be #OLYMCI. The match date
along with the kick-off time in UTC was collected from the Official UCL website: https://www.uefa.com/uefachampionsleague/

Tweet Collection: We used the twitter API to get the tweets containing the hashtags we collected.
Filtering Data: Tweets for each match were filtered separately, minutes and seconds dropped. Clubbed tweets into 3-hour batches.
Plotting Graphs: Graphs plotted for no. of tweets vs time of tweet for analysis

Discussion :
Volume of tweets was higher towards the end of matches than during or before the match.
This is expected as results tend to be discussed after a match. For the 4 out of the 6
wrongly predicted matches, it turns out that the teams involved in are very popular.
Tweepy collects tweets starting from current time and goes back in time. The tweet-limit
we set (10,000) for these matches was encountered before the date of the match could
be reached. We believe that raising this limit will result in correct prediction for these
matches. The other 2 didn’t have enough tweets for any meaningful analysis. We believe
that this can be resolved by incorporating hashtags from other languages too.
We could accurately predict the day of the match while the match time was predicted
within a range of 3 hours overlapping with the match which lasts for about 2 hours. Further
work can be done by collecting a more comprehensive dataset and more granular analysis
of tweet times could yield even more accurate predictions. With larger dataset, manual
inspection might not be feasible, hence we believe we can use statistical methods to
identify if there is a significantly higher volume of tweets and make the predictions based
on those parameters.
