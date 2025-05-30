Customer Churn Prediction with Random Forest

This project predicts customer churn using a Random Forest Classifier on the customerChurnDataset.csv dataset. The pipeline includes data cleaning, feature encoding, exploratory data analysis (EDA) with detailed visualizations, model training with class weighting, and comprehensive evaluation. The visualizations provide insights into churn distribution, feature relationships, and model performance, making it ideal for GitHub presentation.



Project Structure

customer_Churn.py: Complete pipeline for data loading, cleaning, EDA, model training, evaluation, and visualizations.
requirements.txt: Lists project dependencies.
README.md: Project documentation (this file).
.gitignore: Excludes generated files (e.g., .pkl, .png) and environment-specific files.


Setup Instructions

1.Clone the Repository:
git clone <repository-url>
cd <repository-directory>

2.Install Dependencies: Ensure Python 3.8+ is installed, then run:
pip install -r requirements.txt


3.Prepare the Dataset:

Place the customerChurnDataset.csv file in the project directory.
The dataset should contain columns like Churn, Age, Gender, Contract Length, CustomerID, Subscription Type, Usage Frequency, Tenure, and Total Spend. Ensure data types match expectations (e.g., Churn as 0/1, Age as numeric, Gender and Contract Length as categorical).

4.Run the Project:

Run the Project:

pyhton customer_Churn.py

Usage


The script loads customerChurnDataset.csv, performs data cleaning, and conducts EDA with multiple visualizations.
A Random Forest Classifier is trained with class weighting to handle imbalanced data.
Model performance is evaluated using classification reports, confusion matrices, and a precision-recall curve.
Visualizations and the trained model are saved as files in the project directory.

Output

Console Output:

Dataset info, summary statistics, and cleaned data info.
Churn distribution percentages.
Shapes of training and test sets.
Classification reports for training and test sets.
Training and test accuracies.
Feature importance rankings.

Saved Files:

churn_distribution.png: Bar plot of churn vs. no-churn counts with percentages.
age_distribution.png: Histogram with KDE of age by churn status.
age_boxplot.png: Box plot of age by churn status.
age_violinplot.png: Violin plot of age by churn status.
churn_rate_by_<column>.png: Bar plots of churn rate for each categorical column.
stacked_churn_by_<column>.png: Stacked bar plots of churn distribution for each categorical column.
pair_plot.png: Pair plot of numerical features (Age, Tenure, Total Spend) by churn.
correlation_heatmap.png: Heatmap of correlations for encoded numerical features.
confusion_matrix.png: Normalized confusion matrix (percentages).
precision_recall_curve.png: Precision-recall curve with AUC.
feature_importance.png: Top 10 feature importance bar plot.
random_forest_churn_model.pkl: Trained Random Forest model.

Notes

The dataset (customerChurnDataset.csv) is not included in the repository. Users must provide it in the project directory.
Visualizations are saved as PNG files to avoid display issues in non-interactive environments.
The Random Forest model uses pre-tuned hyperparameters. Adjust them in customer_Churn.py if needed.
Class imbalance is handled via class_weight='balanced' in the Random Forest Classifier.
Ensure sufficient memory for pair plots, as they can be resource-intensive for large datasets.

For issues or contributions, please open a GitHub issue or pull request. 
