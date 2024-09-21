BACKGROUND: <br>
On February 14, 2020, Manchester City, a world class soccer team was given a 2 year ban from UEFA European Club competition because of their excessive spending, breaking regulations that try to maintain fair play. UEFA is the prestigious governing body of European Soccer. Similarly to FIFA, they provide international club competitions including the UEFA Champions League, UEFA Europa League, UEFA European Championship, UEFA Nations League, UEFA Conference League, and UEFA Super Cup. They also control the prize money, media rights, and regulations for all of these competitions and club competitors.

UEFA's revenue per year during last year's campaign was 4.3 Billion Euros, displaying how significant this organization's fiscal value is. With all of this immense money flowing in, teams have been spending significantly more and more every year. The chart below shows how spending on buying players has severely increased over time:


<img src="https://cdn.statcdn.com/Infographic/images/normal/20595.jpeg" alt="Global Soccer Transfer Fees" width="300"/>
(Source: Statista)


90% of Manchester City was bought in 2008 by Sheikh Mansour’s Abu Dhabi United Group (ADUG). In the last 10 years, since 2013-2014, they have spent over $1.48 billion on transfer fees for players, making them among the top spenders in the world for players. Many other teams have joined this trend, Chelsea even spending $1.42 Billion in the last 10 years, moreso recently. Manchester City did, however, get the 2 year ban charges dropped after they were accused of committing serious breaches of UEFA's club licensing and financial fair play regulations. 

With tons of money being pumped into the world of soccer to the top teams, this raises questions of if this method directly relates to success. To do this, I will conduct a regression analysis in Python using the Pandas Data Analysis Library built into Python. I will also visualize a team's spending vs. their success in UEFA. 

All of the top European Soccer Clubs compete in these competitions, and are members of UEFA. UEFA gives clubs a metric of success in their competition called the UEFA Coefficient. These UEFA Coefficients are calculated based on a team's success in UEFA events, which is indicative of their European International success. The awardance of points can be described and shown in this link below from UEFA's website-
https://www.uefa.com/nationalassociations/uefarankings/club/about/

METHOD:<br>
My method will see if a clubs spending on transfers correlate to a clubs UEFA success (Their UEFA Coefficient)
I decided to use spending from the last 4 years from 2020. Using this decade's information makes the most sense because success and spending differs per year, so using the most recent time period is essential. In addition to this, this method ensures that COVID-19 does not affect any analysis.

First I gathered the top 50 teams that had the highest UEFA rankings from the UEFA site, and inputted them into a csv, as there is no downloadable site with this information. There is also no downloadable csv on transfer expenditures from these teams so I used Transfermarkt, which is one of the most reputable sites that detail information about every teams spending and income regarding players. I inputted a team's expenditures since 2020, as well as their income from transfers and balance. 


The csv that I made is linked in this repository. Here is the link for that: ["Top50EuropeSoccerSpending.csv"](https://github.com/JaydenNPatel/UEFA-Spend-For-Success-Analysis/blob/main/Top50EuropeSoccerSpending.csv) 
I used Python Pandas to clean my dataset, and that Jupyter Notebook file is also linked in this repository, along with all of the regression that I conducted. Here is the link for that: ["UEFATeamsSpend.ipynb"](https://github.com/JaydenNPatel/UEFA-Spend-For-Success-Analysis/blob/main/UEFATeamsSpend.ipynb)



ANALYSIS: <br>
First, just to see the distribution for UEFA spending, I created a graph for that. 
![image](https://github.com/user-attachments/assets/59810a44-40db-41cc-9b50-e47687e7f4c8)

It seems like high expenditures are rare among teams. Most teams appear to tend to spend below 500 million per year.

I wanted to see all of the graphs and plotted all of the variables using the sns pairplot. Thia helped visualize any variables relationship to each other. Here it is below:

![image](https://github.com/user-attachments/assets/1466b04c-e928-4e01-ba18-21e3c7a1a16d)



I then conducted regression to see if Transfer Expenditures correlated to UEFA Coefficient. The results are below
![image](https://github.com/user-attachments/assets/ac1710ad-aa25-4af3-ba3e-011257e6c59f)
![image](https://github.com/user-attachments/assets/e1ea605c-9ede-4f8f-8f21-91476b338a0a)

Based on the plotted points, it looks like it is helpful to have more expenditures. Teams with super low expenditures tend to not have high UEFA Coefficients, but there are far more than enough cases to conclude that spending is not really correlated to UEFA success. Far more than enough teams with high spending have low UEFA success, and many teams have low spending with a very high success rate in UEFA. In addition to this, the r-squared is also significantly weak, concluding that this correlation is very weak.

I did the same regression analysis with income per club and balance per club. They had even lower r-squared values, displaying how the correlation of income or balance to UEFA Coefficient is not strong. The r-squared value for comparing Income to UEFA coefficient was 0.123. The r-squared value for comparing Income to UEFA coefficient was 0.110. So these show barely any correlation at all.


I also conducted a heatmap of these correlations, more simply displaying these correlations on one plot:


![image](https://github.com/user-attachments/assets/3b31743e-e05e-403d-bdf2-9aa913418e29)





Lastly, I wanted to see how the UEFA Coefficient lines up to every single clubs expenditues and income, in a more visually appealing way to draw insight. I used Tableau for this, and I have pasted my graphs below. 

![Expenditure](https://github.com/user-attachments/assets/5edfe9a6-6297-47be-ab84-5c81d1682911)
![Income](https://github.com/user-attachments/assets/f11d04ad-bc64-41da-bf4c-a644cc8b522f)


This graph makes it a lot clearer how teams with mid-tier spending tend to succeed just as much as teams with higher amounts of spending. Teams like Borussia Dortmund, Real Madrid, Roma, and Villareal have spend a significantly less amount this decade than teams like Chelsea, Arsenal, Manchester United, Tottenham, Juventus, Liverpool, Barcelona, PSV, Stade Rennais, and Marseille, and still have done as good as, if not better in UEFA competitions. It is important to note that there does seem to be a trend that English teams tend to spend much more collectively than other countries, which more research can be done upon.

CONCLUSION <br>
To conclude, during this decade with transfer expenditure being in the hundreds of millions and even billions over time, it is important to see if this actually pays off in terms of UEFA competition success. After running regression, and visualizing data between transfer expenditures and income, it can be pretty clear that -yes- spending money has helped teams succeed this decade, but not significantly to say that money is the driver of success. With low correlation rates, and many teams proving that money doesn't buy success, it can be concluded that transfer expenditure does not directly correlate to a higher UEFA Coefficient. 



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

        Jupyter Notebooks
        
        Tableau
