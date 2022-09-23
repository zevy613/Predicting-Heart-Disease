# Predictive Modeling For at Risk Heart Disease Patients

Author: William Borenstein


## Models used
1. Extreme Gradient Boosting (XGBClassifier)
2. Logistic Regression
3. K-Nearest Neighbors


### Business problem:
Using a data set that contains various features about patients such as Cholesterol, Blood Sugar and Chest Pain Type, I will attempt to predict if a patient is likely to get heart disease.

### Goal: 
Predict whether or not a patient is likely to have heart disease

### Data
This data set has 12 columns and 918 rows. The target column that I will try to predict is 'HeartDisease' which is classified by a 0 if the patient doesn't have heart disease and 1 if they do have heart disease.

## Methodology
First we load the data set and performe a brief inspection of the data. This includes checking for balance and creating explanatory visualizations of our data so we can learn more about the data set and note any trends that stick out.

Second, we pre-process our data. Because some columns are numeric and some categoric we need to scale and One-Hot-Encode our data.

Third, we model our data using XGBoosting. We first create a default model and then we hypertune it using a Grid Search. The parameters I tuned are 'max_depth', 'num_leaves', 'learning_rate', 'min_child_weight' and 'n_estimators'.

Fourth, we use a Logistic Rergession model. We create a default model and then we hypertune it. The patameters I tuned were 'C', 'penalty' and 'solver'.

Lastly, I used a K-Nearest Neighbors model to model my data. Unlike in the other models I used, in this model I implemented some Feature Engineering to minimize the number of columns in my data set. I also tuned the model. The parameter that I tuned was 'n_neighbors'.

The metrics used to evaluate how the models performed are precision, recall, accuracy and f1.

## Results
Visual #1

![image](https://user-images.githubusercontent.com/54513705/192050978-9da27539-0842-4672-a255-565cf1ddff88.png)

From Visual #1 above we can see that as a patient gets older thier chances of getting heart disease increase. 


Visual #2

![image](https://user-images.githubusercontent.com/54513705/192051282-cfd23be0-4b24-4efb-8b6a-52a04bb9f519.png)

From Visual #2 above we can see that people who are asymptomatic in regards to chest pain, are more at risk. This makes sense because people who don't have any symptomes don't know that there is a problem that needs to be addressed. As a result, no preventative measures are taken which leads to a higher rate of positivity. One way to avoid this is have regular check ups and frequent testing.

## Model
The final classification model that I would put in production is K-Nearest Neighbors Classifier.
       
-------------------Testing Data Scores-------------------
  
  Accuracy score :  0.878
  
  Recall score :  0.886
  
  Precision score :  0.9

The reason I chose this model was because it has the highest recall score which minamizes the number of false negatives.

## Recomondations:
I think that if more data was collected, better results could have been achieved. Specifically the samples between male and female patients could have been more even balanced. Secondly, there could have been more features so the model could be more informative.

## Limitations & Next Steps: 
One way we could enhance this model would be to add more hyper-parameter tuning on more variables. Also, other Feature Engineering could have been performed with more knowledge of the subject matter. An expert could be consulted on which what features can be modified for better results. Lastly, a more or less accurate percentage of variance could have been chosen when using PCA. Agian, a subject matter expert can be consulted for guidence.


## For further information 
zevy613@gmail.com
