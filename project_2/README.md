# Project 2 - Ames Housing Data and Kaggle Challenge

As part of a successful submission for Project 2, we are expected to make at least one (and hopefully, multiple!) submissions towards the Project 2 Regression Challenge on Kaggle.

In this challenge, you we use the well known **Ames housing data to create a regression model** that **predicts the price of houses in Ames, IA**.

For this dataset, the data dictionary can be found at this [link](https://www.kaggle.com/competitions/dsi-us-11-project-2-regression-challenge/data)

### Contents of this file

This project has been broken up into two parts.

Part 1 of the jupyter notebook consists of mainly **data cleaning**, **exploratory data analysis** and **feature engineering**.

Part 2 of the jupyter notebook consists of **model selection**, **model preprocessing**, **running models** and **model evaluation**.


### Libraries Used

1) Pandas
2) Numpy
3) Matplotlib
4) Seaborn 
5) ScikitLearn (Mainly used in part 2 for modeling, but Iterative Imputer is used to fill missing values in part 1)
6) statsmodel.api (Used to get summary of p-values of features)
7) SHAP (https://shap.readthedocs.io/en/latest/) (Used to increase explainability of machine learning models)


### Problem Statement

I am a data scientist working for an online property agency in the United States.  

This online platform allows clients to put their properties on sale. When transactions are made, the company then takes a percentage of commission. As part of a new service, the company wishes to help clients properly value their properties and prevent our clients from being low-balled. **When clients make more profits, the company also enjoys a higher commission** creating a win-win situation for both the company and its clients.  

In view of the increase in property transactions in Ames, Iowa, the company is also looking to expand into Ames to take advantage of the increase in property transactions.

As part of the Data Science team, I am tasked to build a regression model to predict sale prices of housing specifically in Ames, Iowa. Criterias given by the company includes that the model should have a **high R2 score (R-squared)** and a **low RMSE (Root Mean Squared Error)** as the cost of error can be huge to both **clients and the company**. Most importantly, the model should also be efficient and uses the **least amount of features** to predict housing prices in lieu of a cost-cutting measure.

### Conclusion & Reccomendations

**Conclusion**

In order to tackle this data science problem given to me, we first had to clean the data and decide the best imputation methods to fill them. Afterwards, we did an exploratory data analysis in which we had identified important features and also engineered some. Thereafter, we went on with the modeling process to train a regression model that beats a benchmark model.

Linking back to the problem statement, we have successfully hit all business requirements for this project. With a **model score of almost 90%**, an **RMSE of $24,741** and **requiring only 13 features**, we have essentially went over and beyond. This means that the regression is able to generalise sale price and predict an outcome with a low error term.

Through this process, we have also discovered features that contributes most to the prediction of sale price and we can use this knowledge to help clients and when clients are able to improve their housing, they will be able to fetch a higher sale price which means more commission for the company, creating a win-win situation for both clients and our company.

All in all, **I would consider this project a success**. We managed to train a regression model that exceeded expectation.

**Limitation**

External Factors such as economical push may influence housing price e.g. 2008 housing crisis in the US. These factors are out of our control and the model needs to be maintained to accomodate to such factors.

**Reccomendations**

1) Firstly, we discovered the key predictors that has an impact on sale price. The top three being overall quality, above ground living area and the year the housing was built. Although there is nothing a client can do about the living area, the client can definitely look into ways to improve its overall quality. We can take this chance to also provide services that teach and help clients to find ways they can improve its overall quality to increase sale price. Also, one might think that there is nothing they can do about the year their housing was built. But in this analysis, we have discovered that by remodelling their house, it gives an effect that the house was reborn, which increases sale price.

2) Secondly, I would reccommend that the project was open to more machine learning models as one of a disadvantage of regression is that it is sensitive to outliers. This means that outliers can have a huge impact on the output of the model. However, we have used a cuberoot transformation to deal with these outliers as explained during EDA. 

3) Lastly, I would reccomend that we can improve our data collection technique. This would result in a dataset with lesser missing values which. Since we had to impute some data using missing value imputation methods, a prediction is still a prediction. With data that were correctly recorded, we might be able to discover the true relationship between the column and our target variable.

### Personal Thoughts

I felt that this project has pushed me beyond my limits. Not only has this project taught me how to run machine learning models, I also had to do quite abit of self teaching to educate myself of the various statistical terms. Before this project, I thought that running a machine learning model was as simple as just cleaning and running but from this project, I learn that there is more than meets the eye. I had to experiment back and forth with adding and removing features while changing bits and pieces here and there to try to increase my R2 score of the model. In hindsight, I realised that there are certain processes that could help me in the future. For example, I learnt that one could use the p-value to determine whether or not a feature is statistically significant or one could also look at the correlation coefficient. I also realised that even if a feature has a high regression coefficient, it does not mean that there is a high correlation coefficient.Additionally, I realised the importance of removing features that causes multicollinearity. Other than multicollinearity, I also have to find out the hard way that I have engineered features that were not truly independent of the target variable. This caused me to have to make changes at the very last minute. By understanding these concepts, I will be able to apply them when I face upcoming data science projects.

To sum up, I am grateful that I am able to learn so much within the short deadline of two weeks for this project. And this is just the first step to achieving great things in the future in the world of data science. 
