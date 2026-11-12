# ASD-Prediction-Using-Machine-Learning-Masters-Capstone-Project
A Machine Learning classification project for Autism Spectrum Disorder (ASD) prediction using Python, featuring EDA, data preprocessing, SMOTE, Decision Tree, Random Forest, XGBoost, and hyperparameter optimization.

**Autism Spectrum Disorder (ASD) Prediction Using Machine Learning with Python**
**Project Overview**
This project focuses on developing a Machine Learning-based classification model to identify potential indicators of Autism Spectrum Disorder (ASD) using demographic information, behavioral screening responses, and other relevant attributes.
The primary objective is to analyze the available dataset, perform data preprocessing and exploratory data analysis, address class imbalance, and develop predictive classification models to distinguish between individuals belonging to the ASD-positive and ASD-negative classes.
Three Machine Learning algorithms — Decision Tree, Random Forest, and XGBoost — are implemented and evaluated. Hyperparameter optimization using Randomized Search Cross-Validation is performed to identify the best-performing model.
The project demonstrates an end-to-end Machine Learning workflow, covering data understanding, preprocessing, feature analysis, model development, optimization, and performance evaluation using Python.

**Objectives**
-Understand and analyze the dataset to identify meaningful patterns and relationships.
-Perform data cleaning and preprocessing to improve data quality.
-Conduct Exploratory Data Analysis (EDA) to understand feature distributions and correlations.
-Handle categorical variables through Label Encoding.
-Identify and treat outliers using the Interquartile Range (IQR) method.
-Address class imbalance using Synthetic Minority Over-sampling Technique (SMOTE).
-Develop and compare multiple Machine Learning classification algorithms.
-Optimize model performance through hyperparameter tuning.
-Evaluate the selected model using appropriate classification metrics.
-Save the trained model and encoding objects for potential future use.

**Technologies and Libraries Used**
-->Python – Primary programming language.
-NumPy – Numerical computations and array operations.
-Pandas – Data manipulation and analysis.
-Matplotlib – Data visualization.
-Seaborn – Statistical visualization and exploratory analysis.
-Scikit-learn – Data preprocessing, model development, cross-validation, hyperparameter tuning, and evaluation.
-Imbalanced-learn – Handling class imbalance using SMOTE.
-XGBoost – Gradient boosting-based classification.
-Pickle – Saving trained machine learning models and encoders.
-Jupyter Notebook – Interactive development and experimentation environment.

**Project Workflow**

**1. Data Collection and Understanding**
-Imported the dataset using Pandas.
-Examined dataset dimensions, column information, and data types.
-Inspected unique values and class distributions.
-Identified relevant numerical and categorical features.

**2. Data Cleaning and Preprocessing**
-Removed unnecessary columns such as ID and age_desc.
-Standardized selected country and ethnicity categories.
-Grouped certain relationship categories into a common category.
-Converted categorical variables into numerical representations using Label Encoding.
-Examined missing or inconsistent categorical entries.

**3. Exploratory Data Analysis (EDA)**
Performed exploratory analysis to understand the dataset and identify meaningful patterns.
Key activities included:
-Age and result distribution analysis.
-Mean and median calculations.
-Histograms and Kernel Density Estimation (KDE).
-Box plots for identifying potential outliers.
-Frequency distribution analysis of categorical features.
-Correlation analysis using a heatmap.

**4. Outlier Detection and Treatment**
Applied the Interquartile Range (IQR) method to identify outliers in numerical features, particularly age and result.
Outlier values were replaced with the respective feature median to reduce the potential influence of extreme observations.

**5. Feature Selection and Data Splitting**
-Separated independent features (X) and the target variable (y).
-Used Class/ASD as the target classification variable.
-Split the dataset into training and testing subsets using an 80:20 ratio.
-Used a fixed random state of 42 for reproducibility.

**6. Handling Class Imbalance**
Applied SMOTE (Synthetic Minority Over-sampling Technique) to the training data to address class imbalance by generating synthetic samples for the minority class.
This helps provide a more balanced dataset during model training.

**7. Machine Learning Model Development**
Implemented and compared the following classification algorithms:

**-Decision Tree Classifier**
-Builds decision-based rules to classify observations.
-Provides an interpretable tree-based approach.

**-Random Forest Classifier**
-Combines multiple decision trees to improve predictive performance.
-Uses ensemble learning to produce more robust predictions.

**-XGBoost Classifier**
-Uses gradient boosting to build an ensemble of decision trees.
-Sequentially improves model predictions by learning from previous errors.

**8. Model Evaluation and Hyperparameter Tuning**
-Applied 5-fold cross-validation to compare the initial models.
-Used RandomizedSearchCV to explore different hyperparameter combinations.
-Evaluated model performance using accuracy, confusion matrix, precision, recall, and F1-score.
-Selected the best-performing model based on cross-validation accuracy.

**9. Model Serialization**
Saved the selected trained model and categorical encoders using Pickle:
-best_model.pkl – Trained classification model.
-encoders.pkl – Label encoders used during preprocessing.

**Model Performance**
The initial cross-validation comparison produced the following results:

Algorithm                   Mean Cross-Validation Accuracy

Decision Tree                 85.63%

Random Forest                 91.95%

XGBoost                       90.39%

After hyperparameter optimization, the Random Forest Classifier was selected as the best-performing model.

**Final Model Evaluation**

**Evaluation Metric**                       **Result**

Best Cross-Validation Accuracy              92.72%

Test Accuracy                               81.88%

Precision (Class 1)                         0.59

Recall (Class 1)                            0.64

F1-Score (Class 1)                          0.61

The final model achieved an accuracy of approximately 81.88% on the held-out test dataset.
These results demonstrate the model's classification performance on the available dataset. Accuracy alone does not establish clinical reliability or diagnostic suitability.

**Key Learning Outcomes**
Through this project, I gained practical experience in:
-End-to-end Machine Learning project development.
-Data cleaning, transformation, and preprocessing.
-Exploratory Data Analysis and statistical interpretation.
-Categorical feature encoding.
-Outlier detection and treatment.
-Handling imbalanced datasets using SMOTE.
-Implementing supervised Machine Learning algorithms.
-Ensemble learning techniques.
-Cross-validation and hyperparameter optimization.
-Classification model evaluation.
-Saving and managing trained Machine Learning models.

**Disclaimer**
This project is developed for educational and academic purposes as part of a Machine Learning with Python capstone project.
The model is intended for experimentation and learning purposes only. It is not a clinically validated diagnostic system and should not be used to diagnose Autism Spectrum Disorder or make medical decisions.
