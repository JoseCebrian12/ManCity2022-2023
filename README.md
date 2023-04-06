# Bread price prediction
## Task:

Predict whether the average bread price will increase (binary outcome).

## Subtasks:

- Parse and load the file https://download.bls.gov/pub/time.series/ap/ap.data.3.Food into a dataframe
- Create a dataframe for the historical average bread price (series id: APU0000702111)
- Create a dataframe for the historical average flour price (series id: APU0000701111)
- Create a function that takes a dataframe with year, period, and value columns and converts it to a time-indexed series (year-period as the index and value as the value)
- Create a function that takes a time-indexed series and a k-value (k varying from 1 to 12) and converts it to a dataframe where each row contains the k-prior values and the current series value. Hint: in python use the rolling pandas windowing function.
- Use the functions in 4 and 5 to create a predictor dataset (k-prior average prices) and a label (whether the price increased from the prior value)
- Fit a Logistic Regression model that uses the prices of bread and flour for the prior 3 months to predict whether the price of bread will increase this month
- Will the price of bread increase for the month after the last month of data.
- How accurate is the prediction? Hint: use the prior 100 months to evaluate the model
