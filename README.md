# Data Cleaning and Model Training

### Data processing instructions:

1) Import the raw data set into a Pandas DataFrame. Perform some exploratory analysis on the raw data set. Check for the types of data hygiene issues mentioned in the lesson. Whenever you find a possible issue, write some code to fix it. Apply your fixes systematically, not case-by-case. Be sure to include comments to explain your process.
2) Find the number of missing values in each column and each row. Remove rows where at least 50% of the values are missing. Then remove columns where at least 50% of the values are missing.
3) Calculate descriptive statistics for each column. Let's define an outlier as a value at least 3 standard deviations away from the mean. Which columns have outliers? What are those values?
4) With the remaining columns, use scikit-learn to impute missing values. For continuous features, fill in the mean. For categorical features, fill in the mode.
5) Combine the date-related columns into one column with the Pandas to_datetime() method, then use that column to create a numeric Age column (in years). Calculate Age based on today's date; it doesn't have to be a whole number. Once you've created the Age column, remove the other date-related columns, including the one you created with Pandas.
6) Create dummy variables for the categorical features. Drop one level of each feature to end up with k-1 dummies, not k.



### Model Training Instructions

1) Using your processed data set from the previous exercise, create a new Pandas DataFrame called X that includes everything except the target variable column. Make sure this is a new object; don't overwrite any previous data sets.
2) Create a new Pandas Series called y that includes just the target variable column. Again, make sure this is a new object.
3) Following the documentation above, create new objects X_train, X_test, y_train, and y_test. Let the test set be 30% of the original data set. Specify a random seed value of your choice so you can reproduce your steps later.
4) Use the Pandas .describe() method to compare the descriptive statistics of the training sets and test sets.
