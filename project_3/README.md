## Project 3: Web APIs & NLP ( Part 2 )

This project covers three of the biggest concepts we cover in the class: Classification Modeling, Natural Language Processing and Data Wrangling/Acquisition.

For this project, we will be scraping data from two subreddits. Thereafter, we will apply Natural Language Processing to train a classifier to classify which subreddit a particular post comes from.

### Contents of this file

Part 1 of the project includes scraping data from Reddit
Part 2 of the project includes data cleaning, data pre-processing, exploratory data analysis, model pre-processing, modeling, final model selection, conclusion and recommendations.

### Libraries Used

1) Pandas
2) Numpy
3) Matplotlib
4) Seaborn
5) Sklearn
6) NLTK

### Problem Statement

According to JAMA Psychiatry, studies show that adolescents who use social media more than three hours per day may be at heightened risk of mental health problems.

Additionally, according to Bachmann S. Epidemiology of Suicide and the Psychiatric Perspective, most suicides are related to psychiatric disease, with depression, substance use disorders and psychosis being the most relevant risk factors.


In view of these statistic, as a corporate social responsibility of a newly developed social media application, Chipper, they have implemented a new feature where users are able to report other users' posts for suspected mental health issue so that they will be able to provide help to these users before it is too late.

As a data scientist working in this company, I am tasked to train a classifier that will categorise posts that were
reported for mental health issues into either Anxiety or Depression so that we are able to route these users to its appropriate helpline. The **two classifiers we will be using in this project are Logistic Regression and Naive Bayes**. To train the classifier, I will be using posts from **Reddit's r/Anxiety and r/Depression subreddits as proxy data**.

[Source 1](https://jamanetwork.com/journals/jamapsychiatry/article-abstract/2749480)

[Source 2](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6165520/#B1-ijerph-15-02028)

### Success Metrics
For this project to be considered successful, we will aim to optimise **Accuracy and Precision Score**.

`Accuracy ` refers to the ratio of the number of correct predictions and the total number of predictions. We want high accuracy as it would mean that the model has the ability to classify posts correctly to their respective categories.

`Precision score` explains how many of the correctly predicted cases actually turned out to be positive. E.g. In our case, it would mean the number of instances we predict `Depression` and it is actually `Depression`. We want to be able to correctly route as many users to their appropriate helpline and wrong classifications could mean that users were not able to receive the help they need.

With this in mind, we will be trying to hit the **target of greater than 90% for Accuracy and Precision Score**.

### Final Model Selection
|Model|Method|Accuracy (Train)|Accuracy (Test)|Precision (0)|Precision (1)|AUC|
|---|---|---|---|---|---|---|
|Logistic Regression|Bag of Words|0.9934|0.8932|0.91|0.88|0.94|
|Naive Bayes Bernouli|Bag of Words|0.9208|0.8500|0.84|0.86|0.92|
|Naive Bayes Multinomial|Bag of Words|0.9278|0.8744|0.89|0.86|0.93|
|**Logistic Regression**|**TF-IDF (Uni-Gram)**|**0.9363**|**0.9110**|**0.91**|**0.90**|**0.96**|
|Naive Bayes Bernouli|TF-IDF (Uni-Gram)|0.9208|0.8500|0.84|0.86|0.92|
|Naive Bayes Multinomial|TF-IDF (Uni-Gram)|0.9253|0.8735|0.87|0.89|0.94|
|Logistic Regression|TF-IDF (Bi-Gram)|0.9934|0.8247|0.84|0.82|0.91|
|Naive Bayes Bernouli|TF-IDF (Bi-Gram)|0.9213|0.6579|0.61|0.91|0.90|
|Naive Bayes Multinomial|TF-IDF (Bi-Gram)|0.9974|0.8379|0.81|0.88|0.92|


Based on the summary of scores above, we will select the Final Model which is Logistic Regression using TF-IDF (Uni-Gram).

It has an train accuracy of 0.9363, test accuracy of 0.9110, Precision(0) of 0.91 and Precision(1) of 0.90. It is the best model as compared to all the other models and it also meets our expectations of accuracy and precision score of greater than 0.90. As a bonus, it also has an AUC of 0.96 which is also the highest out of all the other models. 

### Conclusion

In conclusion, **we have successfully built a classifer that meets expectation of Accuracy and Precision score greater than 90%**. Other than building a successful model, some insights that I have discovered from evaluating the models is that posts in r/Depression talks more about wanting to die and feelings of hopelessness while posts in r/Anxiety talks more about panic attacks and feelings of anxiousness. This shows we should never overlook the effects of mental health issues especially depression where suicidal thoughts are involved.

Thankfully, the Chipper app now allows users to report posts that suggest that a particular user is suspected to be suffering from mental health issues. After the implementation of the final classifier model, we will be able to classify whether a user is suffering from anxiety or depression with a >90% accuracy and precision. This means that there will be an increase in accessibilty for these users to receive the help they need. 

### Limitations

1) In reality, users could suffer from both Depression and Anxiety. However, in this project, we assume that the subreddit that the users posts on is the predominant mental health issue they suffer from. For example, we assume that a user who posted on r/Depression to suffer predominantly from Depression.

2) Due to Chipper being a newly developed Social Media application, we do not have enough internal data, therefore, we are choosing to use reddit posts as our proxy data. As the application matures, we should switch to use internal data that accurately represents the type of posts users on Chippy posts.

### Reccomendations

1) As there are many more mental health issues than just Anxiety or Depression, we can expand the number of mental health issues our classifier can classify. 

2) In the future, Chipper can implement a feature that will automatically flag a post for suspected mental health issue without the need to wait for users to report such posts.

3) Chipper can work with these mental health issue helplines to come up with in-app campaigns that promote the importance of caring for these mental health issues. These campaigns could also raise awareness for mental health issues and educate users on how to identify and care for someone suffering from these mental health issues.
