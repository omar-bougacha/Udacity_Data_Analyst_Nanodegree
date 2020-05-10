# Ford GoBike
## by Omar Bougacha


## Dataset

I choose to work with the Ford GoBike Dataset. The dataset mainly present the bike rides information from June 2017 to March 2020. I choose to work with the data from 2018 and 2019. This gives me the possibility to compare the performances of the company over these two years. Unlike classical datasets, in which we have some independent variables and one dependent variable and we try to study which variables influence the most the dependent variable, here the objective of the analysis is to **study the behavior of the bike rides user's to help taking business decisions**. I propose to analyze the data inoder to gain insights about the customers behaviour. The main question I propose are the following: 
- How the duration of the bike ride are distributed? 
- During which period(s) of the day there are more bike rides? 
- What day(s) of the week present more bike rides?
- During which month(s) have the more dense bike usage? 
- How is the flux of bike rides on some stations? 
- How did all these performances evolve between 2018 and 2019? 

To answer these questions, I did some data wrangling before starting the analysis. The dataset is presented in different csv files. Each file contains the rides of a given month. I downloaded the data files, loaded them into proper structures, and merged them into a yearly dataframe as part of the gathering step from the data wrangling process. Then, I performed some data quality and tidiness assessment to detect the present issues e.g. missing values, unaccurate data types, etc. The treatment of each detected issue is detailed and documented in the exploration file. The obtained cleaned datasets are stored into csv files joined with the study. 

The chosen dataset does not present any continuous variables except for the duration of the bike rides. Therefore, I add another dataset just to experience the multivariate analysis and the scatterplots. I propose to study some weather data (i.e. temperature and weather class) as a bonus to the original study. This weather data is obtained through a free **API** access. However, this API present a limited number of data points for each day. The API is obtained from the [Weatherbit](https://www.weatherbit.io/api) website. To obtain the access, all we have to do is create an account and choose the free plan. And this will grant us an API key that allows up to 500 historical data points per day. This dataset is put through the whole data wrangling process. Every step of the process is well explained and documented in the exploration file. Data accessed using the API are stored while keeping it's json structure into text files that are joined with the project. Then, the entries are read from the text file, and converted into dataframes. The assessment of quality and tidiness issues of these dataframe is also documented in the exploration file. All the performed operations for the cleaning part are also documented in the Define, Code, Test structure. 

I used the obtained data to analyze an example of the relationship between the duration of the rides and the temperature. Also a quick study on the distribution of the bike rides over the weather type is given. Although these analysis do not allow a great insight in the decision making process. These could help the company decide whether or not to start a new branche in another city If the weather of the new city is analyzed. 




## Summary of Findings

Here are the answers to the questions I proposed to answer: 
- The duration of the bike ride are concentrated on small durations. The distribution is skewed to the right. And the peak of duration is between 300 seconds and 1000 seconds.
- The distribution of the bike rides over the hours of the day is bimodal. We have to peaks on 8 and 17 hours which corresponds to the going to and out of work/university. This gives us an idea that most users use the bike to go to or out of work/university.
- This idea is supported by the distribution of the bike rides over the days of the week. As we observe that the number of rides is more important on working days. 
- The number of rides is more important during the months of "good weather". We also observe a peak during october which corresponds to the back to university period. 
- There is a big flux of bike rides between the major stations of transport (train and ferry stations). Also there is a big unbalance between the rides to and out of some stations. 
- Almost all the observations are the same for 2018 and 2019 except the montly distributed bike rides. For 2019, the gab between the good weathered months and the bad weather months seems to be smaller. The number of stations and consequently the number of bike rides has increased from 2018 to 2019. 
- The temperature have a curve of bell relationship with the duration of the bike. The durations are larger for temperature between 10 and 20 celsius. However, for very high or very low temperatures the bike rides are mostly of short durations. 


## Key Insights for Presentation

In the presentation, I kept the figures that answers the question I proposed to answer. However, all these visualizations are presented as subplots to allow the observer to compare between the results of 2018 and 2019. When distributions are presented I made sure to use the same bins to reduce at most the error rates. I also tried, during the exploration and the summary of findings, to keep a very high data ink ratio. 

