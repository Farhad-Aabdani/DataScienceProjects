Fake Job Postings Classification

This project classifies job postings as real or fake using a Random Forest Classifier on the fake_job_postings.csv dataset. The pipeline includes data cleaning, feature encoding, feature selection, handling class imbalance with SMOTE, model training with hyperparameter tuning, evaluation, and comprehensive visualizations for exploratory data analysis (EDA) and model performance. The project is optimized for GitHub with saved plots and detailed analysis.

Project Structure
•	main.py: Complete pipeline for data loading, cleaning, EDA, feature selection, model training, evaluation, and visualizations.
•	requirements.txt: Lists project dependencies.
•	README.md: Project documentation (this file).
•	.gitignore: Excludes generated files (e.g., .pkl, .png) and environment-specific files.

Setup Instructions
1.	Clone the Repository:
git clone <repository-url>
cd <repository-directory>
2.	Install Dependencies: Ensure Python 3.8+ is installed, then run:
pip install -r requirements.txt
3.	Prepare the Dataset:
o	Place the fake_job_postings.csv file in the project directory.
o	The dataset should contain columns like job_id, fraudulent, location, company_profile, description, requirements, benefits, employment_type, required_experience, required_education, industry, function, department, salary_range, telecommuting, has_company_logo, and has_questions. Ensure data types match expectations (e.g., fraudulent as 0/1, categorical columns as strings).
4.	Run the Project:
python main.py

Usage
•	The script loads fake_job_postings.csv, performs data cleaning (e.g., handling missing values, dropping unnecessary columns), and conducts EDA with visualizations.
•	Features are encoded using one-hot encoding and label encoding, followed by feature selection using Chi-squared scores.
•	Class imbalance is addressed using SMOTE, and a Random Forest Classifier is trained with hyperparameter tuning via GridSearchCV.
•	Model performance is evaluated using classification reports, confusion matrices, and feature importance visualizations.
•	Visualizations and the trained model are saved as files in the project directory.

Output
•	Console Output:
o	Dataset info and summary statistics.
o	Original and balanced class distribution (before and after SMOTE).
o	Shapes of training and test sets.
o	Best hyperparameters and F1 score from GridSearchCV.
o	Train and test accuracy (F1 score and overall accuracy).
o	Classification report for test set.
o	Selected features and their Chi-squared scores.
o	Feature importance rankings.
•	Saved Files:
o	employment_type_distribution.png: Bar plot of employment type by fraudulent status.
o	required_experience_distribution.png: Bar plot of required experience by fraudulent status.
o	correlation_heatmap.png: Heatmap of correlations for numerical features (if available).
o	confusion_matrix.png: Confusion matrix of model predictions.
o	feature_importance.png: Top 10 feature importance bar plot.
o	fake_jobPostings.pkl: Trained Random Forest model.

Notes
•	The dataset (fake_job_postings.csv) is not included in the repository. Users must provide it in the project directory.
•	Visualizations are saved as PNG files to avoid display issues in non-interactive environments.
•	The Random Forest model uses hyperparameter tuning to optimize the F1 score. Adjust the param_grid in main.py if needed.
•	Class imbalance is handled via SMOTE, which may increase memory usage for large datasets.
•	Feature selection uses Chi-squared scores to select important categorical features, with a threshold of 10.
•	The correlation heatmap is only generated if numerical features (other than fraudulent) are present.
For issues or contributions, please open a GitHub issue or pull request.

