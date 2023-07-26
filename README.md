# Titanic-Analysis

Libraries and their use

pandas (pd): Used for data manipulation and analysis with DataFrames.

numpy (np): Used for numerical operations and array manipulations.

matplotlib.pyplot (plt): Used for creating visualizations and plotting data.

seaborn (sns): A powerful library for creating visually appealing statistical graphics.

sklearn.metrics.accuracy_score: A function from scikit-learn (sklearn) to calculate the accuracy score for classification models.

sklearn.datasets: A module from scikit-learn that provides datasets for practicing and testing machine learning algorithms.

sklearn.svm: A module from scikit-learn that provides Support Vector Machine algorithms.

sklearn.tree.DecisionTreeClassifier: A class from scikit-learn to create decision tree classifiers.

sklearn.naive_bayes.GaussianNB: A class from scikit-learn to create Gaussian Naive Bayes classifiers.

sklearn.linear_model.LogisticRegression: A class from scikit-learn to create logistic regression classifiers.

The dataset contains the following columns:
----------------------------------------------------------------------------------------------------------------

PassengerId: A unique identifier for each row (passenger).

Survived: The target variable we want to predict, indicating whether a passenger survived (1) or did not survive (0).

Pclass: The socio-economic class of the passenger, which is a categorical ordinal feature with three unique values (1, 2, or 3) representing upper, middle, and lower classes, respectively.

Name: The name of the passenger.

Sex: The gender of the passenger (male or female).

Age: The age of the passenger.

SibSp: The number of siblings and spouses traveling with the passenger.

Parch: The number of parents and children traveling with the passenger.

Ticket: The ticket number of the passenger.

Fare: The fare paid by the passenger.

Cabin: The cabin number of the passenger.

Embarked: The port of embarkation, which is a categorical feature with three unique values (C, Q, or S) representing Cherbourg, Queenstown, and Southampton, respectively.

Data preprocessing steps:
------------------------------------------------------------------------------------------------------------------------------

Filling Missing Values: We filled the missing values in the "Age" feature using median values based on passenger class and sex groups. This approach accounts for the correlation between age, passenger class, and sex, leading to more accurate imputations.

Filling Embarked Missing Values: As there were only two missing values in the "Embarked" feature, we made an informed decision to fill them with the mode value for upper-class female passengers (C).

Filling Fare Missing Value: With only one missing value in the "Fare" feature, we employed the median value of the entire dataset to fill the missing entry.

Handling Cabin and Introducing Deck: We replaced the "Cabin" feature with the newly created "Deck" feature, which contains the deck information extracted from the first letter of the original cabin values. By doing this, we retained essential information about the passenger's cabin location while reducing the high cardinality of the feature.

Dropping Cabin Feature: As the "Deck" feature serves as a more meaningful and manageable representation of the cabin location, we dropped the original "Cabin" feature from the dataset.

No Missing Values Left: After the above steps, there are no missing values remaining in the dataset, making it ready for further analysis and modeling.


