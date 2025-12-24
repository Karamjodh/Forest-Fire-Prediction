# 🌲 Forest Fire Prediction using Machine Learning 🔥

## 🚀 Project Overview

Forest fires are one of the most devastating natural disasters, causing significant environmental, economic, and human losses every year.  
Early prediction and detection are crucial to minimize these damages. This project aims to **predict forest fire occurrences and Fire Weather Index (FWI)** using historical weather and fire indices from Algeria.

The dataset consists of environmental variables such as temperature, relative humidity, wind speed, rainfall, and fire weather indices like FFMC, DMC, DC, ISI, BUI, and FWI.

---

## 🎯 Objective

1. **Classify Fire Events**: Predict whether a day is prone to a fire (`fire` vs `not fire`).  
2. **Predict Fire Weather Index (FWI)**: Quantitative measure of fire risk using environmental features.  
3. **Visualize Fire Patterns**: Analyze trends, correlations, and regional fire distributions.

---

## 📊 Dataset

- **Source**: Algerian Forest Fires Dataset (2012)  
- **Number of Records**: 243  
- **Features**:

| Feature | Description |
|---------|-------------|
| `day` | Day of the month |
| `month` | Month |
| `year` | Year |
| `Temperature` | Daily temperature (°C) |
| `RH` | Relative Humidity (%) |
| `Ws` | Wind speed (km/h) |
| `Rain` | Rainfall (mm/m²) |
| `FFMC` | Fine Fuel Moisture Code |
| `DMC` | Duff Moisture Code |
| `DC` | Drought Code |
| `ISI` | Initial Spread Index |
| `BUI` | Build-Up Index |
| `FWI` | Fire Weather Index (target for regression) |
| `Classes` | Fire occurrence: `fire` / `not fire` |
| `Region` | Region ID (0 = Bejaia, 1 = Sidi-Bel Abbes) |

---

## 🧹 Data Cleaning & Preprocessing

- Removed null and redundant values.  
- Standardized column names.  
- Converted numerical features to appropriate types.  
- Encoded fire labels (`fire` / `not fire`) as 1/0 for classification.  
- Removed highly correlated features (`threshold = 0.85`) to reduce multicollinearity.  
- Standardized dataset using `StandardScaler` for numerical stability.

---

## 🔍 Exploratory Data Analysis (EDA)

- **Histograms**: Feature distributions and outliers.  
- **Pie Charts**: Class balance visualization.  
- **Correlation Heatmap**: Relationships between environmental variables and fire occurrence.  
- **Boxplot**: Distribution of FWI.  
- **Monthly Fire Patterns**: Seasonal trends in Bejaia and Sidi-Bel Abbes regions.

---

## 🤖 Modeling

**Features (`X`)**: Temperature, RH, Wind Speed, Rain, FFMC, DMC, DC, ISI, BUI, Classes, Region.  
**Target (`Y`)**: FWI (regression) or Classes (classification).

- **Train-Test Split**: 75% training, 25% testing.  
- **Scaling**: StandardScaler for numerical features.  
- **Correlation Handling**: Removed highly correlated features.  

**Model Types**:  
- Classification: Predict fire occurrence.  
- Regression: Predict Fire Weather Index (FWI).  
- Algorithms: Linear Regression, Random Forest, Gradient Boosting, Neural Networks.

---

## 📈 Visualizations

- **Feature Distributions**: Histograms for temperature, humidity, wind speed, etc.  
- **Correlation Heatmap**: Showed inter-feature relationships.  
- **Boxplot**: Visualized FWI outliers.  
- **Monthly Fire Trends**: Countplots by region and fire occurrence.

---

## 💡 Insights

- Fire occurrence is higher in July–September.  
- FWI correlates strongly with FFMC, DMC, ISI, and BUI.  
- Temperature positively correlates with fire risk; RH negatively correlates.  
- Regional analysis helps identify localized fire risks.

---

## 🛠 Usage

### 1️⃣ Clone the Repository

Start by cloning this project to your local machine:

```bash
git clone https://github.com/yourusername/forest-fire-prediction.git
cd forest-fire-prediction
```

---

### 2️⃣ Install Dependencies

Make sure you have Python 3.x installed. Then, install the required packages:

```bash
pip install -r requirements.txt
```

> **💡 Tip:** It's recommended to use a virtual environment to avoid conflicts with other Python packages.

---

### 3️⃣ Launch the Notebook

Open Jupyter Notebook and explore the project:

```bash
jupyter notebook Forest_Fire_Prediction.ipynb
```

* Navigate through each section:

  * **Data Cleaning & Preprocessing**
  * **Exploratory Data Analysis (EDA)**
  * **Regression & Classification Modeling**
  * **Visualization of Fire Patterns**

---

### 4️⃣ Optional: Run a Script (if available)

If you prefer running a script instead of using the notebook:

```bash
python forest_fire_prediction.py
```

---

### 🔗 Additional Notes

* Ensure all dataset files are in the `data/` folder.
* You can modify the notebook to test **new machine learning models** or **tweak hyperparameters**.
* Visualizations will automatically render within the notebook.
