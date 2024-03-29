# Hotel-Reservation-Cancellation-Prediction

## Project Goals
The goal of this project was to analyze a hotel reservation dataset and employ machine learning to determine if a customers’ cancellation can be predicted and how accurate would it be. My initial hypothesis was that the further in advance a customer makes a reservation, and the time of year would be the most likely predictor variables. 

## Process Approach
### EDA
 - Acquired a dataset from Kaggle.com that was comprised of over 36,000+ rows of data and was somewhat clean to start with.
 - Verified the source to confirm dataset was reliable
 - Looked for any domain knowledge that may provide more detail about the data contained
 - Reviewed the csv file to familiarize myself prior to starting my analysis to get an idea of what features I might be able to use to predict cancellation
 - Looked for nulls and missing information
 - Analyzed the distribution to see if anything was skewed
 - Compare variables and look for correlations to help support my hypothesis early on

<img src="Images/Missing Values Check.png" alt="Notebook" width=30%>   <img src="Images/Summary Statistics.png" alt="Notebook" width=40%>

### Model Selection
I decided to train and test the following 3 models:
- Logisitic Regression as it is faster to train but may not be able to capture complex relationships in the data so I wanted to see how it would perform with information that may not quite be linear
- Random Forest as it is robust, less prone to overfitting and very good with large datasets
- Gradient Boost Machines as it provides higher predictive accuracy but requires careful tuning to avoid overfitting

I found the three models to be good choices as I wanted to compare a more simplistic model against two ensemble models to see the difference in perfomance and benefits of each.

### Preprocessing
 - Cleaned the data
 - Transformed where necessary (one-hot encoding because data was categorical and numerical)
 - Split in to train and test (80/20)

### Model Comparison
<img src="Images/Model Comparison.png" alt="Notebook" width=85%>
 - Trained the model on the preprocessed data
 - Tested using test set of data put aside prior to training
 - Used cross-validation and grid search to find best hyperparameters to help increase accuracy


#### Logistic Regression
<img src="Images/Classification Report - Logistic Regression.png" alt="Notebook" width=65%>

#### Random Forest
<img src="Images/Classification Report - Random Forest.png" alt="Notebook" width=65%>

#### Gradient Boost Machine
<img src="Images/Evaluation Metrics - GBM.png" alt="Notebook" width=60%>

### Created Pickle Files
 - Beneficial as it allows easy storage and preserves the model, so you don’t have to retrain
 - Makes it easier to share
 - Aids with deployment in API’s







## Outcomes
Based on feature importance, lead time, average price per room, number of special requests, arrival date and arrival month were top 5 in contributing to model prediction.

<img src="Images/Feature Importance (Hotel Reservations).png" alt="Notebook" width=75%>

Barplot shows amount of canceled reservations based on market segment type with online having the most.
<img src="Images/Barplot - Market Segement Type.png" alt="Notebook" width=65%>






