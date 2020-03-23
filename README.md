# Topic-Modeling
## Fit K-means to the speech text of the members, comprising of the 1000 phrases

When K=5, we get the 5 clusters below. See the code for K=10, 15, 20, 25.

![Clusters](https://github.com/khaledimad/Topic-Modeling/blob/master/Images/Image04.png)

## Use AIC and the elbow curve method to identify the most optimal value of K. 
Based on the AIC method (LEFT GRAPH), we chose K = 28 clusters.
<br>Based on the elbow curve method (RIGHT GRAPH), we chose K= 24 clusters.

![Choosing K](https://github.com/khaledimad/Topic-Modeling/blob/master/Images/Image05.png)

The AIC curve seems to first flatten out around K = 28. The elbow curve seems to first flatten out
around K = 24. These two values are not exactly equal but are very close.


## Fit a topic model for the speech counts, using Bayes factors to choose number of topics
Here the max Bayes factor chooses K=10 clusters (logBF = 77508.93) because this is the largest
logBF. Here is how we interpret the topics:<br>
• Topic 1 relates mostly to Asian Pacific Americans and African Americans.<br>
• Topic 2 relates mostly to US Army veterans and their health care.<br>
• Topic 3 relates to illegal immigration.<br>
• Topic 4 relates largely to the Iraq's Oil for Food Program.<br>
• Topic 5 relates to retirement policy and taxes related to retirement.<br>
• Topic 6 relates to Tongass National Forest timber sales program.<br>
• Topic 7 relates to a US judicial court and judge confirmations.<br>
• Topic 8 relates to gun control and gun safety.<br>
• Topic 9 relates to US trade policy, free trade, and the trade deficit.<br>
• Topic 10 relates to stem cell research.<br>

## Connect the unsupervised clusters to partisanship. 

![Topic Regression on Party](https://github.com/khaledimad/Topic-Modeling/blob/master/Images/Image06.png)

Above is an extract from the code indicating coefficients from the topic regression on party. Topics
6, 7, and 10 have no coefficients which suggests that these topics are non-partisan. Whereas, the
other topics have negative or positive coefficients indicating correlation with partisanship. Topic
6 is mixed but mainly about climate and environment; 7 is about the judicial system; 10 is mostly
about stem cell research. See the top 10 words in each of these topics below:

![Topic Regression on repshare](https://github.com/khaledimad/Topic-Modeling/blob/master/Images/Image07.png)

Above is an extract from the code indicating coefficients from the topic regression on repshare.
Representatives who discussed Topics 1, 2, 8, and 9 had more voters who did NOT vote for Bush
in 2004. By contrast, those who spoke about 3 and 5 had a higher percentage of people who did
vote for Bush.

![Regression on Party](https://github.com/khaledimad/Topic-Modeling/blob/master/Images/Image08.png)

Based on the above, we see that the topic model does better than the regression onto words.

![Regression on Repshare](https://github.com/khaledimad/Topic-Modeling/blob/master/Images/Image09.png)

Based on the above, we see that the topic model does better than the regression onto words
