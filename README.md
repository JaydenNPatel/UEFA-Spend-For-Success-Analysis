On February 14, 2020, Manchester City, a world class soccer team were given a 2 year ban from UEFA European Club competition for 2 years. UEFA is the prestigious governing body of European Soccer. Similarly to FIFA, they provide international club competitions including the UEFA Champions League, UEFA Europa League, UEFA European Championship, UEFA Nations League, UEFA Conference League, and UEFA Super Cup. They also control the prize money, media rights, and regulations for all of these competitions and club compeititors. UEFA's revenue per year during last years campaign was 4.3 Billion Euros, displaying how significant this orginizations fiscal value is. With all of this immense money flowing in, teams have been spending significantly more and more every year. The chart below shows how spending on buying players has severly increased over time:


<img src="https://cdn.statcdn.com/Infographic/images/normal/20595.jpeg" alt="Global Soccer Transfer Fees" width="300"/>
(Source: Statista)


90% of Manchester City was bought in 2008 by Sheikh Mansour’s Abu Dhabi United Group (ADUG). In the last 10 years, since 2013-2014, they have spent over $1.48 billion on transfer fees for players, making thm among the top spenders in the world for players. Many other teams have joined this trend, Chelsea even spending $1.42 Billion in the last 10 years, moreso recently. Manchester City did, however, get the 2 year ban charges dropped after they were accused of commiting serious breaches of UEFA's club licensing and financial fair play regulations. 

With tons of money being pumped into the world of soccer to the top teams, this raises questions of if this method directly relates to success. To do this, I will conduct a regression analysis in Python using the Pandas Data Analysis Library built in to Python. I will also visualize a teams spending vs. their success in UEFA. 

All of the top European Soccer Clubs compete in these competitions, and are members of UEFA. UEFA gives clubs a metric of success in their competition called the UEFA Coefficient. These UEFA Coefficients are calculated based on a team success in UEFA events, which is indicative of their European International success. The awardance of points can be described and shown in this link below from UEFA's website-
https://www.uefa.com/nationalassociations/uefarankings/club/about/

My method will see if a clubs spending on transfers correlate to a clubs UEFA success (Their UEFA Coefficient)
I decided to use spending from the last 4 years since 2020. Using this decades information makes the most sense because success and spending differs per year, so using the most recent time period is essential. In addition to this, this method ensures that COVID-19 does not affect any analysis.

First I gathered the top 50 teams that had the highest UEFA rankings from the UEFA site, and inputted them into a csv, as there is no downloadable site with this information. There is also no downloadbale csv on transfer expenditures from these teams so I used Transfermarkt, which is one of the most reputable sights that detail information all teams spendning and income regarding players. I inputted a teams expenditures since 2020, as well as their income from transfers and balance. 
The csv that I made is linked in this repository.
I used Python Pandas to clean my dataset, and that Jupyter Notebook file is also linked in this repository, along with all of the regression that I conducted, which is titled "UEFATeamsSpend.ipynb"




First, just to see the distribution for UEFA spending, I created a graph for that. 
![image](https://github.com/user-attachments/assets/59810a44-40db-41cc-9b50-e47687e7f4c8)

It seems like high expenditures are rare among teams. Most teams appear to tend to spend below 500 million per year.



I then conducted regression to see if Transfer Expenditures correlated to UEFA Coefficient. The results are below
![image](https://github.com/user-attachments/assets/ac1710ad-aa25-4af3-ba3e-011257e6c59f)
![image](https://github.com/user-attachments/assets/e1ea605c-9ede-4f8f-8f21-91476b338a0a)

Based off of the plotted points, it looks like it is helpful to have more expenditures. Teams with super low expenditures tends to not have high UEFA Coefficients, but there are far more than enough cases to conclude that spending is not really correlated to UEFA success. Far more than enough teams with high spending have low UEFA sucess, and many teams have low spending with a very high success rate in UEFA. In addition to this, the r-squared is also significantly weak, concluding that this correlation is very weak.

I did the same regression analysis with income per club and balance per club. They had even lower r-squared values, displaying how the correlation of income or balance to UEFA Coefficient is not strong. 
I also conducted a heatmap of these correlations, more simply displaying these correlations on one plot:


![image](https://github.com/user-attachments/assets/3b31743e-e05e-403d-bdf2-9aa913418e29)





Sources:

        BBC Sport-
          https://www.bbc.com/sport/football/51511036
          https://www.bbc.com/sport/football/53387306
          
        Academia-
          https://www.academia.edu/89730712/UEFA_and_the_European_Union_From_Confrontation_to_Co_operation
        
        Wikipedia-
          https://en.wikipedia.org/wiki/UEFA
          
        Statista-
          https://www.statista.com/chart/20595/global-spending-on-soccer-transfer-fees/

        City A.M.
          https://www.cityam.com/who-owns-manchester-city-now-how-much-did-sheikh-mansour-pay-thaksin-shinawatra-in-2008/ 
