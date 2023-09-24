# Project2
# Predicting Adult Income
##for DataScience Studies
**Author**: Jody Jacobs
### Business problem:
The purpose of this project is to predict whether an adult's income will be < or > 50000 based on certain demographic data.
### Data:
Data Source: https://www.kaggle.com/datasets/wenruliu/adult-income-dataset
>This data set consist of 48842 rows, and 15 columns

The data dictionary is as follows:
![image](https://github.com/Jody565/Project2/assets/138827084/c5f78995-3eef-48e7-85a7-7f392e8bb163)

## Methods

- I cleaned the data by removing any missing data and removing all duplicates and inconsistancies.
- During the exploratory Data Analysis a heatmap was done to explore the correlation between numeric features.
- A countplot was used to see at which eductaion level an adult has the highest potential of income.
- A Countplot was also done to determine the split between males and females earning < and > 50000

## Results

![image](https://github.com/Jody565/Project2/assets/138827084/a2219470-df62-4d44-99d6-d5e461f4ab35)

From the graph we can see that most adults earning less than 50k are highschool graduates or have some college education. Fore the adults earning greater than 50k the most adults have a bacholors degree.

![image](https://github.com/Jody565/Project2/assets/138827084/963eb284-f8dc-4e57-b396-05a1cf641d22)

From the graph above we can see that there are very little females earning greater than 50k with Males accounting for most of the adults earning above 50K

## Model

The following Machine Learning Model was chosen

- Tuned logistic Regression Model(without Feature Engineering)

Report the most important metrics

- Linear Regression Model (Testing Set)

-        precision    recall  f1-score   support

           0       0.95      0.73      0.82      8493
           1       0.51      0.88      0.65      2801

-   accuracy                           0.76     11294
-   macro avg       0.73      0.80      0.74     11294
-   weighted avg       0.84      0.76      0.78     11294


  ![image](https://github.com/Jody565/Project2/assets/138827084/2405e6ef-514c-431e-b66b-32fe02dcd69c)

  
Refer to the metrics to describe how well the model would solve the business problem

The Model i choose to productionize is the Tuned Logistic regression model without the Feature engineering as it has the highest AUC score 88%. However the accuracy score is a bit lower at 76%, it has the highest recall score of 88%. The model predicted false positives with an accuracy at 27% however for the model performed better when predicting false negatives with an error rate of 12% which seems to be alot more balanced than the other models.The model is howver not perfect especially shown on the recall metric where we only get about approx 88% as we could not get any score of 90%  or greater.The model was under balanced so results could be skewed to look better than they actually are..


## Recommendations:

- I can see that the model is a bit biased towards males as most of the sample size in the dataset are males in comparison 
  to females in the dataset. The percentage of males who make >5000 is much greater than the percentage of 
  females that make the same amount. This will certainly be a significant factor as gender shoould be an important 
  demographic in today's society
  
- Another demographic feature that could have been added was to better our model would have been location so we can see 
  which states offer a higher earning potential

 
