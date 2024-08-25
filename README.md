# Loan Defaulter Prediction Project
Overview
This project involves developing a machine learning model to predict loan defaulters using data from a financial institution. The project is divided into two main parts: Data Preprocessing and Exploration and Model Training and Evaluation.

Part 1: Data Preprocessing and Exploration
1. Data Loading
Loaded the application data and previous application data into pandas DataFrames.
Merged the datasets after thorough preprocessing.
2. Data Cleaning
Handled missing values using appropriate imputation techniques.
Removed duplicate entries and irrelevant features.
Filtered columns with more than 40% missing values to avoid introducing bias.
3. Feature Engineering
Created new interaction features such as AMT_INCOME_TOTAL_X_AMT_CREDIT.
Applied transformations like logarithms and polynomials to enhance feature representation.
Encoded categorical variables using techniques like one-hot encoding and label encoding.
Scaled numerical features using StandardScaler to ensure they contribute equally to the model.
4. Data Exploration and Visualization
Reviewed the distribution of key numerical and categorical features.
Filtered numerical columns based on variance to focus on the most relevant features.
Computed and visualized the correlation matrix for the filtered features to identify potential relationships.
Analyzed and visualized the distribution of categorical variables to understand their impact on the target variable.
5. Train-Test Split
Split the dataset into training and testing sets, with an 80-20 ratio.
Converted the continuous target variable into binary using a threshold.
Part 2: Model Training and Evaluation
1. Logistic Regression
Model 1 (Baseline): Trained a Logistic Regression model without handling class imbalance. Achieved an accuracy of 97%, but with poor recall for the minority class.
Model 2 (Improved): Used SMOTE for oversampling and applied class weights to handle imbalance. Achieved a balanced accuracy with better recall for the minority class.
2. Decision Tree
Trained a Decision Tree classifier, which provided good accuracy but struggled with the minority class, reflecting the need for better handling of class imbalance.
3. Random Forest
Trained a Random Forest classifier, which generally handles class imbalance better due to its ensemble nature. However, it still struggled with predicting the minority class accurately.
4. Model Evaluation
Evaluated models using metrics such as accuracy, confusion matrix, classification report, and ROC AUC score.
Compared model performances, with Logistic Regression (Model 2) showing the best balance between precision, recall, and overall accuracy.
Conclusion
The Logistic Regression model with SMOTE and class weights emerged as the best-performing model for this binary classification task, effectively handling class imbalance and providing the most reliable predictions.

Next Steps
Consider further hyperparameter tuning for the Logistic Regression model to improve performance.
Explore additional advanced techniques such as ensemble methods (e.g., XGBoost) to enhance model accuracy.
Continue refining feature engineering techniques to capture more relevant patterns in the data.
Files
app_data.csv: Application data used for the project. (https://drive.google.com/file/d/1YVFCfNCV7r3Rlo5Es7EnkyFZz12NCIpU/view?usp=sharing)
prev_app_data.csv: Previous application data used for merging with the main dataset.(https://drive.google.com/file/d/13JDxj5Te8e_kUEasyxonBCav-pw1O_jW/view?usp=sharing)
columns_description: (https://drive.google.com/file/d/1vUqS5fRE7xIwCcyv5kb-6ahNNP03fSGy/view?usp=sharing)
SAMABANKFINAL (1).html: Jupyter Notebook containing the code for the entire project.
Presented by Sama Amr.pdf: A concise presentation summarizing the key findings and model performance.
Prerequisites
Python 3.x
Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
