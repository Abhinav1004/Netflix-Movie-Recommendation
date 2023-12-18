
<img src='./images/netflix-q.jpg'>

# Netflix Movie Recommendation 


Netflix held the Netflix Prize open competition for the best algorithm to predict user ratings for films. The grand prize was $1,000,000 and here we used multiple collaborative recommendation approaches to recommend Netflix Movie Recommendation

## Problem Description

We are given a set of user with their associated moives rated by them on the netflix platform.
Develop a machine learning algorithm to predict the ratings of the movies not rated by the user so as to devise a strategy to recommend them in future to maximise the viewership of Netflix.


## Approaches 

I applied the following 8 approaches to estimate the predicted rating 

1. Self Created 13 features ---> XGBoost Regressor
2. Self Created 13 features + Surprise Baseline Predictor -----> XGBoost Regressor
3. Self Created 13 features + Surprise KNN Predictor ----> XGboost Regressor
4. Self Created 13 features + Surprise Baseline Predictor + Surprise KNN(user-user) Predictor ----> XGboost Regressor

5. Self Created 13 features + Surprise Baseline Predictor + Surprise KNN(user-user) Predictor + Surprise KNN(item-item) Predictor  ----> XGboost Regressor

6. Surprise KNN(user-user) Predictor + Surprise KNN(item-item) Predictor + Matrix Factorization(SVD)  ----> XGboost Regressor

7. Surprise KNN(user-user) Predictor + Surprise KNN(item-item) Predictor + Matrix Factorization(SVD++)  ----> XGboost Regressor

8. Self Created 13 features + Surprise Baseline Predictor + Surprise KNN(user-user) Predictor + Surprise KNN(item-item) Predictor + Matrix Factorization(SVD++)  ----> XGboost Regressor


# Results

|    | AP1   | AP2    | AP3   | AP4   | AP5    | AP6   | AP7     | AP8    |
|----|-------|--------|-------|-------|--------|-------|---------|--------|
| RMSE | 1.095 | 0.93   | 0.33  | 0.322 | 1.07   | 0.654 | 0.608   | 1.09   |
| MAPE | 36.62 | 29.375 | 9.026 | 8.365 | 35.4093| 19.62 | 17.8334 | 36.3331|



# Installation
1. Please create a virtual environment using the command `virtualenv venv` and use `source bin/activate` to activate the same
2. Install the required libraries using the command `pip install -r requirements.txt`
3. Launch the jupyter notebook by executing `jupyter notebook` in the current directory
4. Please put the dataset in the data folder present in current working directory 
5. Execute all cells of the jupyter notebook to reproduce the results as above



