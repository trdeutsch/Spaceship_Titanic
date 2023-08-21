DESCRIPTION
Welcome to the year 2912, where your data science skills are needed to solve a cosmic mystery. We've received a transmission from four lightyears away and things aren't looking good. The Spaceship Titanic was an interstellar passenger liner launched a month ago. With almost 13,000 passengers on board, the vessel set out on its maiden voyage transporting emigrants from our solar system to three newly habitable exoplanets orbiting nearby stars. While rounding Alpha Centauri en route to its first destination—the torrid 55 Cancri E—the unwary Spaceship Titanic collided with a spacetime anomaly hidden within a dust cloud. Sadly, it met a similar fate as its namesake from 1000 years before. Though the ship stayed intact, almost half the passengers were transported to an alternate dimension! To help rescue crews retrieve lost passengers, you are challenged to predict which passengers were transported by the anomaly using records recovered from the spaceship’s damaged computer system.

BUSINESS UNDERSTANDING
What is the goal of the project? What is the problem that you are trying to solve?
To predict which passengers were transported by the anomaly using records recovered from the spaceship’s damaged computer system.

ANALYTIC APPROACH
What kind of analytics should we use? Predictive? Descriptive?
Because the goal of the project requires predicting True/False answers, we need to use the Classification model.

DATA REQUIREMENT
What kind of data is needed for the project?
In order to predict data, including both binary or specific values, we require labeled data. In this particular project, we need binary data.

DATA COLLECTION
Where are the data come from? How to gather the data?
The data was downloaded from Kaggle in CSV format. 

DATA UNDERSTANDING 
The data include 3 CSV files, which are sample_submission.csv, test.csv, and train.csv. Each file contains columns, ie:
train.csv: Personal records for about two-thirds (~8700) of the passengers, to be used as training data.
- PassengerId: A unique Id for each passenger. Each Id takes the form gggg_pp where gggg indicates a group the passenger is traveling with and pp is their number within the group. People in a group are often family members, but not always.
- HomePlanet: The planet the passenger departed from, typically their planet of permanent residence.
- CryoSleep: Indicates whether the passenger elected to be put into suspended animation for the duration of the voyage. Passengers in cryosleep are confined to their cabins.
- Cabin: The cabin number where the passenger is staying. Takes the form deck/num/side, where the side can be either P for Port or S for Starboard.
- Destination: The planet the passenger will be debarking to.
- Age: The age of the passenger.
- VIP: Whether the passenger has paid for special VIP service during the voyage. RoomService, FoodCourt, ShoppingMall, Spa, VRDeck - Amount the passenger has billed at each of the Spaceship Titanic's many luxury amenities.
- Name: The first and last names of the passenger.
- Transported: Whether the passenger was transported to another dimension. This is the target, the column you are trying to predict.

test.csv: Personal records for the remaining one-third (~4300) of the passengers, to be used as test data. Your task is to predict the value of Transported for the passengers in this set.

sample_submission.csv: A submission file in the correct format.
- PassengerId: Id for each passenger in the test set.
- Transported: The target. For each passenger, predict either True or False.

DATA PREPARATION
- Clean data: Drop missing values, and duplicate values using NumPy. Replace missing values with frequent values and mean values using NumPy.
- Transforming: Transform data type. Convert categorical values into numerical values using LabelEncoder.
- Standardizing: Transform data values into smaller values using StandardScaler.
- Features Engineering: Combine different columns into a new one.

MODELING
- Split data: Split 70% of the data for training and 30% of the data for testing purposes, with random_state parameter = 2.
- Model selection: Decision Tree
- Model parameters selection: Use GridSearchCV to find the best parameter with the best score.
- Predict targeted value: Use the selected model to fit the training set and predict the test set.

EVALUATION
Use accuracy_score to find the score between the targeted value in the test set and the predicted value. 
