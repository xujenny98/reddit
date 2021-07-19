# AMC Stock Analysis 
Report on Segment 2
<br/>1.Preliminary data preprocessing A function was defined for cleaning the headlines with following purpose:
<br/>a)Remove stop words.
<br/>b)Remove non-alphabet characters.
<br/>c)Stemming and lemmatization
<br/>2.Feature engineeringwe   try   to   use  TF-IDF   vectorizer   and   count  vectorizer   for   create   numeric   vector   whichrepresents the text.
<br/>3.train/test splittingWe firstly visualizing the distribution of each class, according to the even distribution, wechoose stratified train-Test splits, the test set accounts for 33% of total observations.
<br/>4.model evaluationAs described in sentiment 2, what we are going to solve is a classification problem.We use logistic regression, which is easy to implement, interpret, and very efficient to train forbinary classification, and it makes no assumptions about distributions of classes in feature space. Howe ever, It is difficult to obtain complex relationships, considering the number of featuresin our model is rather large, other classification model such as neural network may perform better.
<br/>Without feature engineering, the prediction accuracy is 49.68, which is not better than a randomguess, detailed metrics is listed in the figure below:
<br/><img width="548" alt="Screen Shot 2021-07-19 at 1 21 08 AM" src="https://user-images.githubusercontent.com/77771292/126106962-3363e717-c808-4031-abd8-7694cbf557b1.png">
<br/>After the data cleaning, comparing different vectorization method, the result achieved with help ofTF-IDF vectorizer is improved, the accuracy on test set is 0.52, which is slightly better thanrandom guess, the detailed performance is below:
<br/><img width="551" alt="Screen Shot 2021-07-19 at 1 21 46 AM" src="https://user-images.githubusercontent.com/77771292/126107010-68258e5d-5a3a-4087-a937-a1a29057a643.png">
<br/>Nevertheless, it is not a model with high prediction power.According to our result, we conclude that the return is not predictable with public news.
However, it is also possible that our conclusion is not correct, a further analysis may include:-better selection on data set, that is, more large data set or more specific selection on financialdata.-More deliberate feature engineering process and more complex model construction
