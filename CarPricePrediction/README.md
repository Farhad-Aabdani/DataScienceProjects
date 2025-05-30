Car Price Prediction with Regression Models

This project predicts car prices using regression models (linear, multiple linear, polynomial, and Ridge regression) on the automobile dataset (automobileEDA.csv). The pipeline includes data cleaning, preprocessing, exploratory data analysis (EDA) with comprehensive visualizations, model development, and evaluation. The project is optimized for GitHub with saved plots and detailed analysis.

Project Structure
•	main.py: Complete pipeline for data loading, cleaning, EDA, model training, evaluation, and visualizations.
•	requirements.txt: Lists project dependencies.
•	README.md: Project documentation (this file).
•	.gitignore: Excludes generated files (e.g., .pkl, .png) and environment-specific files.

Setup Instructions

1.	Clone the Repository:
git clone <repository-url>
cd <repository-directory>

2.	Install Dependencies:
Ensure Python 3.8+ is installed, then run:
pip install -r requirements.txt

3.	Dataset:
o	The dataset (automobileEDA.csv) 
o	The dataset should contain columns like price, engine-size, horsepower, curb-weight, wheel-base, city-mpg, highway-mpg, normalized-losses, bore, stroke, peak-rpm, num-of-doors, fuel-type, aspiration, body-style, drive-wheels, engine-location, length, width, and height.

4.	Run the Project:
	     python main.py

Usage
•	The script downloads automobileEDA.csv, performs data cleaning (handling missing values, converting units, normalizing features), and conducts EDA with visualizations.
•	Four regression models are implemented: simple linear regression, multiple linear regression, polynomial regression, and a Ridge regression pipeline.
•	Model performance is evaluated using R² and MSE metrics, with cross-validation for robustness.
•	Visualizations and the final Ridge regression model are saved as files in the project directory.

Output
•	Console Output:
o	Dataset info, summary statistics, and cleaned data info.
o	Horsepower binning counts.
o	Columns before and after encoding.
o	R² and MSE for simple linear regression, multiple linear regression, and Ridge regression.
o	Cross-validation R² scores (mean and standard deviation).
•	Saved Files:
o	feature_distributions.png: Histograms with KDE for numerical features (price, engine-size, horsepower, etc.).
o	horsepower_bins.png: Bar plot of horsepower bin distribution.
o	correlation_heatmap.png: Heatmap of correlations for numerical features.
o	regression_plots.png: Regression plots of key features vs. price.
o	categorical_boxplots.png: Box plots of price by categorical features (body-style, drive-wheels, engine-location).
o	pair_plot.png: Pair plot of key numerical features.
o	simple_residual_plot.png: Residual plot for simple linear regression.
o	multiple_distribution_plot.png: KDE plot of actual vs. predicted prices for multiple linear regression.
o	polynomial_degree_comparison.png: R² score vs. polynomial degree plot.
o	polynomial_fit.png: Cubic polynomial fit for highway-L/100km vs. price.
o	car_price_ridge_model.pkl: Trained Ridge regression model.

Notes
•	The dataset is fetched automatically from a public URL, ensuring accessibility.
•	Visualizations are saved as PNG files to avoid display issues in non-interactive environments.
•	The Ridge regression model uses a pipeline with standardization and polynomial features (degree=2) for improved performance.
•	Categorical columns are one-hot encoded, with checks to ensure only existing columns are processed.
•	The project includes robust error handling for missing columns, with debug prints to identify issues.
•	Adjust hyperparameters (e.g., Ridge alpha, polynomial degree) in main.py if needed.
For issues or contributions, please open a GitHub issue or pull request.

