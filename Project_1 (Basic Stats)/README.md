# <div style="text-align: center;font-size: 1.5em;">Probabilities and Statistics Project 1
<div style="text-align: right"><span style="font-family: times new roman; font-size: 1.5em;">
**2012023871 경영학과 강민철**<br>
**2012023989 경영학과 김태욱**</span></div>
____

# [Question Studied]

Our research team hold a question about U.S. national competitiveness. Naturally, we thought about labor aged group population, which could be illustrated as the source of the national competitiveness. So it was quite curious that the mortality of the United States of America. We have believed that the mortality would be comparably different by the geographical location.

# [The summary of the observatory study]
## (1) Data: 
1. The data has been collected through 122 Cities Mortality Reposting System from 1962 to 2013 in the United States of America. Since the data are fairly well categorized by cities, ages and weeks, our research team didn't doubt if there would be better dataset for the population of interest.
2. The variable could be defined: The number of labor aged group death in each state of the USA.
3. We provide a .csv file.
4. Also, you can see the graphical representation('histogram' and 'stem and leaf plot') of the data below.

### Stemplot
By summing each city-level observations, we made the whole country level data. The presented data is the first 10 rows of the aggregated time series data.<br>
If you see the stemplot below, you can observe that the graph roughly follows normal distribution. Still, there are some outliers which we remove at part two. <br>
As the original data has states and cities data, we used pivot table function and processed a state ranking data. The histogram is the total death rate of each state. From the histogram we could clearly recognize the states with exceptionally high death rate of labor population; Illinois, Maryland, DC, Texas, New York and so on. 

## (2) The four-step process of the data analysis:
1. **State** : How the U.S. labor aged group mortality would appear in geographical distribution?
2. **Plan** :
  + We are going to remove outliers from the dataset. We will examine the variations through graphs and numerical summaries. It should be shown as a map plot, because this is a variable which changes by geographical location.
  + Among the entire dataset, 40, 400 and 1000 random samples picked by the 'random( )' numpy method.
3. **Solve** :
  + Provide time series plot.
  + Provide a box plot.
  + Provide a map plot.
  + Provide the mean and standard deviation of the dataset, and the five-number summary(minimum value, quartile Q1, median, quartile Q3, maximum value).
4. **Conclusion** :
  + According to Wikipedia, there was a catastrophic tornado disaster at Illinois in 1990. That explains why there were significant outliers at Illinois.
  + Texas are wellknown state for trying to deregulate guns. Maybe that's why it appears dark red. Maryland is one of the richest state in the USA. There is the Johns Hopkins hospital at Boltimore. Possibly the high mortality could have connections with the that indeed.
  + We have illustrated our specific opinions in detail at the "Discussion" section. With handling the data of the mortality, we could learn that it is quite important to figure out the reason of outliers. That is because the outliers tells us something happend in our history. Even removing some extreme outliers, there are supposed to be certain issues or special points which grab researchers attention. Our team has been fascinated those attractions of data analysis.
  
  ## (3) Discussion of the shape of your data

+ **Time Seires Plot**
> The USA Death Rate graph tends to have decreased since 1970s. Especially, these time series plot shows most of the curves are going downward as the time seires since the 1970s. On the other hand, the data of Illinois show significant outliers. 
+ **Box Plot**
> At first, we draw box plot without removing the outliers. However, the result was disappointing becasue some exploding outliers ruined the whole plot and obscured the insight. By applying outlier rejecting method that we learned at class, we could draw a well fitted box plot. <br>Mostly, boxplots of each state are seems to be right skewd. Considering four sample states' box plots, all of them are more likely to be right skewd. That is because those of Q1, Q3 are far below those of the entire USA data. Maybe the box plot of Texas is comparably balanced than that of others. In addition, the box plot of USA shows that the mean and median of distribution is almost same with the difference less than two decimal points. (mean: 119.43, median: 119.31). This means the removal of outliers resulted in the central distribution of data. 
+ **Map Plot**
>As we are handling geographical data we put extra effort and plotted map plot which can give insight which can only be obtained by watching in spatial perspective. For example, we can easily observe that the north-east area has relatively low death rate of labor population compared to other areas. Furthermore, except for the natural disaster at Illinois, it appears dark red at Texas and Marlyand, which means they have comparably high death rate. 
+ **Sampled data histogram**
> With the 40 random samples does not follow the normal distribution at all. It seems that it is left skewd. So we increase the sample size to 400 and 1000. The bigger sample size, the more it follows the normal distribution, which is quite obvious. Not only for that shape, as increasing the sample size, the mean and standard deviation value gradually move closely to those of the population. 

## (4) Calculate and report the sample mean and standard deviation
Sampling method: Among the entire dataset, 40, 400 and 1000 random samples picked by the 'random( )' numpy method.<br>
>**[Mean]** _population_: 119.40, _n=40_: 125.17 _n=400_: 120.08, _n=1000_: 120.73
<br>**[Standard deviation]** _population_: 24.65, _n=40_: 27.88 _n=400_: 24.43, _n=1000_: 24.44

## (5) References

>**Data** : http://data.gov/ <br>
>**Stem and leaf plot** : http://pyvideo.org/pydata-carolinas-2016/stemgraphic-a-stem-and-leaf-plot-for-the-age-of-big-data.html <br>
>**USA map plot frame** : http://stackoverflow.com/questions/39742305/how-to-use-basemap-python-to-plot-us-with-50-states<br>
