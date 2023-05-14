# Airlines_Passenger_Satisfaction
customer satisfaction plays a crucial role in determining business performance and serves as a strategic tool for gaining a competitive edge. This study uses machine learning models to predict the overall satisfaction of passengers with the full service provided by the airline. We aim to select the important factors that affect passenger satisfaction using RFECV() feature selection tool in Scikit-Learn to identify the optimum number of features to obtain the highest accuracy score. We pass in DecisionTreeClassifier() to use as the estimator.

## Data Source
Data used in this study are the passenger satisfaction data set of an American airline on Kaggle (https://www.kaggle.com/binaryjoker/airline-passenger-satisfaction) 

### Data Preprocessing
The dataset contains 129880 samples. Initial dataset contains 0.3% of missing values. We used median method to fill the missing values. Flight Distance, Departure Delay and Arrival Delay have some outliers. After removing the outliers, there are 105722 samples. It is a balanced dataset with 57.253% data Neutral or Dissatisfied and 42.747% Satisfied target

### Feature Selection
RFECV() feature selection tool is used to identify the optimum number of features to use in our model to obtain the highest accuracy score. DecisionTreeClassifier() is used as the estimator. As RFECV() also handles cross-validation, it is used with StratifiedKFold() method with accuracy as the scoring metric. 

The number of features with the highest accuracy is 16. 

### Machine Learning model
Using the feature subset with 16 features, a Decision Tree Classifier model is constructed to predict the satisfaction of passenger. The evaluation index used are accuracy, precision, recall and F1 value.
The accuracy score of the model is 87.01%.

### Business insights
- Short haul passenger have higher returning rate of 54.53% than in medium haul flights (34.17%) followed by long haul flights (11.28%) however the passenger in short haul flight are more dissatisfied with the flight service than medium haul and long haul flights
- Business class passenger are more satisfied with the flight service whereas economy class passenger are highly dissatisfied followed by Economy Plus class passenger. Further, business class passenger are more loyal than other class passenger.
- Young adult and elderly people are neutral or dissatisfied with the flight service whereas adult are more satisfied. Adult are more likely to return than passenger of other age groups.
- The most important type of service is Online boarding, followed by flight distance, In-flight entertainment, ease of online booking and leg room service.



