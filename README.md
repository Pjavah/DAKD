# DAKD
## Data Analysis and Knowledge Discovery exercises

All exercises passed. 

## Some feedback:

### EX1:</br> 	
Good job.  Clear and concise answers and good enough code. The notebook was a bit hard to read due to some big printouts and  plots, but this is a solid pass.

### EX2:</br>
I give you the 'pass' as unfortunately there's no anwer for the bonus exercise.  Very good job, Patrik!
Some notes:
- Stratification: But when the data is randomly splitted, how do you ensure that train and test sets have similar proportions of cases of disease in both if there's 713 0-labels and 287 1-labels? What if you would end up with a 70/30 split and only 0-labels would be in a train set: Could a model learn anything about 1-labels?
- You only fit a StandardScaler with x_train and use this scaling for x_test (so only transform() is used for x_test)
- Did you forgot to use binary values for training and testing? Only numerical were scaled but binary values are also important.
- Even though there's a reference, you should not use any copy-pasteing in exercises.
- Other metrics can also be used with LOO cv. You should also scale the features for cross validation.
- The question for the 4th exercise was quite unclear and misleading but you did good job with it! But what happens when k=1 - why the accuracy is 1.0?
- 5: I couldn't give you any minus points as the necessary plots were there - any extra is always a good thing! :)

Also, as you wondered why the MAE is so different with the k-NN regression, note that you computed MAE in different places: While iterating over different k-values, you first gathered _every_ prediction of each split in a list and afterwards computed the MAE for a spesific k-value (total of 467 labels used here). But when using k=3, you actually computed MAE right after the predictions are made for each split, and since you use loocv, you make only one prediction at a time and compare it with an actual label. I guess that's where the difference comes from.

### EX3:</br>

TBA
