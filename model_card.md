# Model Card



## Model Details



The model is a classification model trained on the provided Census Bureau dataset. The model uses a Random Forest classifier to predict whether an individual's salary is greater than $50K or less than or equal to $50K.



## Intended Use



The intended use of this model is to demonstrate a complete machine learning workflow using the provided census data. The model is used to make salary classification predictions and to evaluate model performance across different categorical slices of the data.



## Training Data



The model was trained using the provided `data/census.csv` dataset. The data was split into training and test datasets before training. Categorical features were processed using the provided `process_data` function and encoder.



## Evaluation Data



The evaluation data came from the test portion of the provided census dataset. The test data was processed using the same fitted categorical encoder and label binarizer created from the training data.



## Metrics



The model was evaluated using precision, recall, and F1 score. On the test dataset, the model achieved a precision of 0.7419, a recall of 0.6384, and an F1 score of 0.6863.



## Ethical Considerations



The dataset contains demographic and employment-related categorical features such as race, sex, education, occupation, relationship, and native country. Model performance can vary across different values of these features. For this reason, the project evaluates performance on categorical data slices and records the results in `slice_output.txt`.



## Caveats and Recommendations



The model does not perform equally across every categorical slice of the dataset. Some slices also contain relatively few records, which can result in metrics that appear very high or very low based on a small number of examples. The slice-level results should be reviewed along with the overall model metrics when evaluating model performance.

