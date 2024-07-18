# Predicit Diabetes with Machine learning and Evaluate predictor impact via Explainable AI to reveal new insides for healthcare

## Summary

In this project I performed a exploratory data analysis to understand a diabetes dataset. I found that the dataset does not differentiate between type I and type II diabetes, but both conditions are present in the dataset. Therefore, I decided to investigate the relationship between the existing features and type I diabetes, type II diabetes, and healthy individuals using explainable AI. To do this, I deterministically classified diabetes into type I and type II based on blood sugar and insulin levels. <br>

Furthermore, the dataset lacks information on gender, which motivated me to make the prediction gender-neutral. As a result, I chose to omit the predictor "Number of Pregnancies," contrary to approaches commonly found in the literature.<br>

The dataset contained a number of duplicates, which I removed to avoid bias in the model evaluation due to identical cases in the training and test data. With the additional cleanup of erroneous/incomplete datasets, only 539 instances remained, leading me to choose a Random Forest model.<br>

As expected, glucose and insulin emerged as the most important predictors for the model. Using SHAP values, I initially examined whether the physiological relationships were correctly reproduced by the machine learning model. <br>

The results encouraged me to repeat the process without insulin, relying solely on age, skin thickness, BMI, glucose, diabetes pedigree function, and blood pressure to make predictions. I intended to use explainable AI to determine which of these features were most relevant in the context of type I and type II diabetes. <br>

However, the dataset contains only 50 individuals with type I diabetes, and it is generally questionable whether all individuals in the dataset were originally correctly diagnosed as diabetics or healthy. Consequently, the models did not perform well enough. Since SHAP values only explain the feature contribution to the learned model and not the reality, further analysis was not pursued. <br>

Overall, this project demonstrates that with large and reputable datasets, machine learning models can learn relationships in health data that may not be immediately apparent to human observers. Using explainable AI, ML models could reveal significant health relationships, potentially inspiring new preventive or curative approaches in the healthcare sector.<br>


## Data

I used a diabetis dataset from kaggle provided by nanditapre:<br>
https://www.kaggle.com/datasets/nanditapore/healthcare-diabetes/code

