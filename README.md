Project Overview

Forest fires are one of the most devastating natural disasters, causing significant environmental, economic, and human losses every year. Early prediction and detection are crucial to minimize these damages. This project aims to predict forest fire occurrences and Fire Weather Index (FWI) using historical weather data and fire indices from Algeria.

The dataset consists of environmental variables such as temperature, relative humidity, wind speed, rainfall, and fire weather indices like FFMC, DMC, DC, ISI, BUI, and FWI.

Objective

Classify Fire Events: Identify whether a particular day is prone to a fire (fire vs not fire).

Predict Fire Weather Index (FWI): Using environmental features to predict FWI, which is a quantitative measure of fire risk.

Visualize Fire Patterns: Analyze monthly trends, correlations, and regional fire distributions to understand fire dynamics.

Dataset

Source: Algerian Forest Fires Dataset (2012)

Number of Records: 243

Features:

Feature	Description
day	Day of the month
month	Month
year	Year
Temperature	Daily temperature (°C)
RH	Relative Humidity (%)
Ws	Wind speed (km/h)
Rain	Rainfall (mm/m²)
FFMC	Fine Fuel Moisture Code
DMC	Duff Moisture Code
DC	Drought Code
ISI	Initial Spread Index
BUI	Build-Up Index
FWI	Fire Weather Index (target for regression)
Classes	Fire occurrence: fire / not fire
Region	Region ID (0 = Bejaia, 1 = Sidi-Bel Abbes)
Data Cleaning and Preprocessing

Removed null and redundant values.

Standardized column names.

Converted numerical features to appropriate types (int/float) for modeling.

Consolidated fire labels (fire / not fire) and encoded them as 1/0 for classification.

Removed highly correlated features (threshold = 0.85) to reduce multicollinearity.

Standardized the dataset using StandardScaler for numerical stability.

Exploratory Data Analysis (EDA)

Histograms: Displayed feature distributions to identify skewness or outliers.

Pie Chart: Visualized class balance between fire and not fire.

Correlation Heatmap: Analyzed relationships between environmental variables and fire occurrence.

Boxplot: Examined the distribution of FWI.

Monthly Fire Patterns: Countplots for Bejaia and Sidi-Bel Abbes regions revealed seasonal fire trends.

Modeling

Features and Target

Features (X): Temperature, RH, Wind Speed, Rain, FFMC, DMC, DC, ISI, BUI, Classes, Region.

Target (Y): FWI (for regression) or Classes (for classification).

Train-Test Split

Split dataset into training (75%) and testing (25%) sets.

Scaling

Standardized features using StandardScaler.

Correlation Handling

Removed highly correlated features to avoid multicollinearity.

Model Types

Classification: Predict fire occurrence.

Regression: Predict Fire Weather Index (FWI).

Models can include Linear Regression, Random Forest, Gradient Boosting, or Neural Networks.

Visualizations

Feature Distributions: Histograms for temperature, humidity, wind speed, etc.

Correlation Heatmap: Showed inter-feature relationships.

Boxplot: FWI outliers visualization.

Monthly Fire Trends: Countplots separated by region and fire occurrence.

Insights

Fire occurrence is more frequent in certain months (e.g., July–September).

FWI is highly correlated with FFMC, DMC, ISI, and BUI.

Temperature positively correlates with fire risk, while RH (humidity) negatively correlates.

Regional analysis helps understand localized fire risks.

Usage

Clone the repository:

git clone https://github.com/yourusername/forest-fire-prediction.git
cd forest-fire-prediction


Install dependencies:

pip install -r requirements.txt


Run the Jupyter Notebook:

jupyter notebook Forest_Fire_Prediction.ipynb


Explore:

Data Cleaning

EDA

Regression and Classification modeling

Fire pattern visualization

Technologies Used

Python 3.x

Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn

Jupyter Notebook for experimentation and visualization

Future Enhancements

Integrate real-time satellite and weather data for live fire prediction.

Apply advanced neural networks or LSTM models for time-series prediction.

Develop a web dashboard for visualizing fire risk dynamically.

Implement feature importance analysis to better understand contributing factors.

Author

Karamjodh Singh

Machine Learning & Data Science Enthusiast

GitHub: https://github.com/Karamjodh
