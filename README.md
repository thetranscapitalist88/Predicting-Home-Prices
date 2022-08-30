**Technical Report**

**Problem Statement**:
    Ames, IA, is revamping the diversity within their city and would like to focus on increasing the LGBT community within their town. Ames realized the buying power of the LGBT community, which is 1.7 trillion. Convincing the LGBT community to settle down in Ames, IA, can help the city rebuild its infrastructure and put the extra money into schools and other programs within the town.

	The Mayor of Ames, IA, has reached out to my company to be a consultant as we work together to figure out to answer the question, "How to increase LGBT homeownership within the city of Ames, IA?" 

	To do my job efficiently, I will be focusing on housing prices. Although the LGBT has the largest buying power collectively, they make less money than their cisgender heterosexual counterparts. Therefore, we must reinforce how housing prices are crucial to this community.  

**Background**
    Real estate trends are essential to a cities profile as they try to attract long-term buyers. As a result, the city can grow while the homeowners gain equity. It seems like a win-win for everyone. Besides the home location is vital to a home buyer, another important factor is how diverse a city can be—the more diversity, the better for everyone in the town. 

	The best way to increase diversity is to focus on marginalized communities. The LGBT community should be the primary focus because they currently hold immense buying power, which is 1.7 trillion. Also, according to preliminary research, the LGBT population in Iowa is only 3.7% compared to other states. This statistic shows how eager Ames, IA would like to improve.

	Research reveals LGBT people have faced discrimination in the home buying process. LGBT communities often result in high denied mortgage loans or accepting mortgages with higher interest than their heterosexual counterparts. 

**Data Dictionary**
|Feature|Type|Dataset|Description|
|---|---|---|---|
|Testing|DataFrame|test|This is required data given to test models|
|Training|DataFrame|train|This is required data given to train models|
|Sample Sub|DataFrame|sample_sub|This is required data to help design models|
|Basic Linear Regression (LR)|DataFrame|LR|LR Model created to predict Sales Price|
|Basic Lasso Regression (lass)|DataFrame|Lass|Lass Model with GridSearch(gs) created to predict Sales Price|
|Basic Ridge Regression (Ridge)|DataFrame|Ridge|Ridge Model with GridSearch(gs) created to predict Sales Price|
|Null Model (null)|DataFrame|Null|Null Model with GridSearch(gs) created to predict Sales Price|

**Summary Statistics**
For the Basic Linear Regression Model:
    From the LR model, Beta0 is 36,214 in dollars while the mean of coefficients is $-3,887. This means for every one unit change in price of X, y will decrease in sale price. This is not a good model prediction because as time increases, the housing pricing will increase too.

    Using the root mean squared error (RMSE) to be a metric to determine the use of my model. The RMSE that is stated above, shows we are off the sale price by $47,215 which is an increase from the baseline model but still not good enough for predicting sale price.

For the Lasso Regression Model:
    The Lasso model with gridsearchcv, pipeline, polynomial features have proved to be my best model yet. The RMSE on testing_filled data is $30,357 which is my lowest prediction yet. 

For the Ridge Model:
    Using ridge was able to cut down the the error down to $26,800 to reduce variation and try to prevent overfitting. Using the ridge 100, was able to shrink coefficients.

**Recommendations**
The recommendations I have for the Mayor, their staff, and the people of Ames, IA, is:

1. Take the time to focus on basic housing features, aka the "bare minimum," to help the LGBT community afford such housing. Then, as I compressed the given data into a smaller correlation matrix that demonstrates the best features in a house, it will help in getting LGBT people to increase homeownership within Ames, IA.

2. Adopt the Lasso Linear Regression model with the lowest error of $26,773 to help predict homes' current and future sale prices in Ames, IA.

3. Increase the mortgage loans acceptance rate for LGBT applicants. Make an incentive for bankers to increase their outreach to find and accept LGBT applicants. One of the sources below states no correlation between LGBT applicants and heterosexual applicants who have the highest chance of defaulting on their loans. So, either way, LGBT candidates are just as good as their cisgender heterosexual counterparts. 

**Conclusion**
To answer the question above, the city of Ames can quickly increase LGBT homeownership by selling homes that are fixer-uppers with basic features and improve the approval of mortgage loans to the marginalized community. In addition, following the recommendations above can stop the many foreclosures that banks stress over in Ames while giving LGBT applicants the chance to build equity. It's truly a win-win situation. 

Lastly, creating different linear regression models to help predict home sale prices have great benefits. It can give the LGBT community time to save money for such large purchases on lower salaries, improve their credit score to ensure mortgage approval, and give the city of Ames the chance to increase diversity. 

**Sources**
https://news.yahoo.com/data-lgbtq-buyers-opt-for-cheaper-homes-that-need-tlc-over-pricier-digs-222825893.html?guccounter=1&guce_referrer=aHR0cHM6Ly93d3cuZ29vZ2xlLmNvbS8&guce_referrer_sig=AQAAAG1zKNPQeX327EVfnzrJ7RnUlYqJd6OcKzEeQE7ZQu9phtwgZAayadaXQzMJi7bHq4kJ11mapBkfEKP4CGRzvXbLCkjWiWxzINkB0exOlTgIPM0xEiD1PV1M9c7fRH2prXoZMZA7xX4sT2ZpvK5JBbP4a380iXK-t-l7NvTi5ZJR
https://www.nar.realtor/newsroom/nar-report-finds-lgbtq-buyers-purchasing-older-smaller-homes-than-other-americans
https://www.realtor.com/news/trends/lgbtq-report/
https://www.lgbtmap.org/equality-maps/non_discrimination_laws
https://www.news.iastate.edu/news/2019/04/16/samesexmortgage
https://www.statista.com/topics/5423/lgbt-homeownership-in-the-us/#dossierKeyfigures