# stroke-pred-project
This project focuses on predicting stroke occurrences using a healthcare dataset.
## Dataset
The project utilizes the `healthcare-dataset-stroke-data.csv` dataset, which contains various clinical and demographic features to predict the likelihood of stroke.
## Data Preparation
1.  **Loading the Dataset**: The `healthcare-dataset-stroke-data.csv` file was loaded into a pandas DataFrame.
2.  **Dropping 'id' Column**: The `id` column was dropped as it's not relevant for prediction.
3.  **Handling Missing 'bmi' Values**: Missing values in the `bmi` column were imputed using the median value (28.1).
4.  **One-Hot Encoding**: Categorical features (`gender`, `ever_married`, `work_type`, `Residence_type`, `smoking_status`) were converted into numerical format using one-hot encoding.
5.  **Train-Test Split**: The dataset was split into training (80%) and testing (20%) sets, with `stroke` as the target variable (`y`) and the remaining features as predictors (`X`).
## Models & Methodology
Two primary modeling approaches were explored to address the class imbalance inherent in stroke prediction:

1. Logistic Regression with Class Weight Balancing
2. Tuned Logistic Regression with SMOTE and Feature Selection
