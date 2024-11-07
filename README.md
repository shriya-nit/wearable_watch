
# Classification Model: Predicting Physical Activities with features in fitness trackers

This project aims to classify human activities using data from wearable devices (Apple Watch and Fitbit) collected from 46 participants. By applying machine learning classification models, we predict various activity types based on sensor data. The project explores the effectiveness of models like RandomForest and XGBoost for accurate activity categorization, providing insights into the potential of wearable data in health and fitness applications.

## Dataset

The dataset, sourced from Kaggle(https://www.kaggle.com/datasets/aleespinosa/apple-watch-and-fitbit-data/data), includes various biometric and activity-related metrics recorded by Apple Watches and Fitbits of which some features are:

- steps
- calories
- heart rate
- entropy of heart rate
- entropy of steps

and many more.

## Methodology

The project follows a structured approach:

1. Data Cleaning: Preparing the dataset for analysis, ensuring no missing values, and applying necessary transformations.
2. Exploratory Data Analysis(EDA) and Feature selection: Selecting and creating relevant features based on preliminary EDA insights.
3. Model Selection and Tuning: Choosing and fine-tuning classification models like RandomForest and XGBoost to improve predictive performance.

## Data Insights from EDA

Key findings from the initial analysis is as follows:

1. Heart rate values ranged from abnormally low (2.222 bpm) to high (194 bpm)
2. Activity "Lying" had a noticeable class imbalance (Managed class imbalance using SMOTE during modeling)
3. Gender identification: 0 is Female (lower mean height and weight)
4. Device distribution: Slightly fewer FitBit data points compared to Apple Watch
5. Age distribution: Mostly individuals aged 18 to 40
6. Numerical features: Steps, calories, and distance distributions are highly skewed.

The outliers were removed using the Z-score method and some most important features were selected from the correlation matrix(heatmap).

## Modeling and Evaluation

Various models were employed to classify activities, with RandomForest and XGBoost showing the best results. Evaluation metrics included accuracy, precision, and recall. Key highlights:

- XGBoost Model Performance: XGBoost achieved the highest individual accuracy among all models tested.
- Ensemble Model Performance: Combining Random Forest and XGBoost in an ensemble model resulted in the highest overall accuracy.
- Feature Importance: Steps emerged as the most important feature for predicting physical activity type, contrary to the initial hypothesis focusing on heart rate.

## Conclusions

The project successfully classified activities based on wearable data with strong accuracy. 
- Direct Measure of Movement: Steps are a direct measure of movement and consistently correlate with various physical activities.
- Heart Rate Variability: While heart rate is important, it can be influenced by numerous factors (e.g., stress, caffeine) and may not always clearly indicate activity type on its own.
- Potential for New Features:
  1. Steps-Heart Ratio: Combining steps and heart rate into a new feature could provide a more nuanced measure of physical activity.
  2. Steps-Distance Ratio: Introducing the steps-distance ratio could further enhance model performance by capturing the relationship between movement and distance covered.

## Acknowledgements

 - Kaggle for the dataset
 - BrainStation Canada for teaching me the necessary tools to do this project
