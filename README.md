The spread of COVID-19 in the whole world has put the humanity at risk. The resources of some of the largest economies are stressed out due to the large infectivity and transmissibility of this disease. Due to the growing magnitude of number of cases and its subsequent stress on the administration and health professionals, some prediction methods would be required to predict the number of cases in future.
When will the coronavirus pandemic come to an end? The question is on everyone’s mind, and while astrologers and politicians have answers, few scientists want to be drawn into hazarding a prediction.
The challenge of the Covid-19 prediction is the most crucial component for countries and global health institutions. A successful and accurate prediction to the future covid cases ultimately results in better management of the pandemic.

Problem Statement- 
The objective of the first part of the problem statement is to predict the Covid Cases of a City on 1st September 2020. The output file 01 should contain only City and the respective Covid Cases for the test data.

Data preprocessing- 
In intial phase to find a correlation between different features and no. of patients we need to deal with the "NaN" values. Since the train dataset available is very less we need to replace "NaN" with most appropriate value for different features rather then just skipping row with "NaN".
By using sex-ratio and female population we calculated population 2020, and dropped population 2001 & 2011 by replacing them with average rate of population growth over a year. 
We considered "H-index", "Toilets available", "No. of hospitals" and "Foreign visitors" as a feature of city type, city population growth, city population 2020 and city sex ratio. Thus making clusters using k-means we replaced "NaN" by average of that particular cluster.

Data Exploration-
We tried to find coorelation betwween various features and covid patients by using various plots and dropped many columns that appeared to be irrelevant.

Model Preparation-
Label and one hot encoding of categorical variables was done before traing the model. Various models were tried and tested using 50-fold cross validation method keeping scoring as "neg rmse".
After trying several models Gradient Boosting Regression gave desired results of lower rmse.
Then hyperparameter tuning gave the optimal parameter which drastically improved the accuracy.
Dimensionality reduction methods were employed to further remove the underired or lower relevant features.
Finally the results were stored in y_pred array.
