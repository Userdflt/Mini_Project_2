# **Evaluating Material Performance for Space Applications**
## **A Data Science Approach Using NASA’s Outgassing Data**

- [View Presentation](./Evaluating_Material_Performance_for_Space_Applications.pptx)
---

# **NASA Outgassing Materials Data Processing**
## Contents

1. **Data Preprocessing**
    - Cleaning and feature extraction code
    - [View detailed notebook](./NASA_Outgassing_Materials_Data_Processing.ipynb)

## **1. Data Preprocessing**

### Data Import and Initial Exploration

- **Importing Dataset:**
    - The dataset is imported from a CSV file for initial exploration and analysis.

- **Initial Data Exploration:**
    - Checking the structure and basic statistics of the dataset.
    - Setting the 'ID' column as the index for better data management.

### Data Cleaning

- **Handling Outliers:**
    - Initial analysis shows high variance in key metrics such as TML, CVCM, WVR, and Space Code.
    - Filtering outliers using quantile-based methods.
    - Visualizing the distribution of filtered data using histograms and box plots.

- **Further Outlier Removal:**
    - Using the Interquartile Range (IQR) method to further clean the data by removing extreme outliers.
    - Rechecking the distribution and presence of outliers through updated histograms and box plots.

### Handling Missing Values

- **Identifying Missing Values:**
    - Analyzing the dataset for missing values.
    - Dropping columns and rows with significant missing data, particularly in 'Cure', 'Material Usage', and 'Space Code'.

- **Final Data Cleaning:**
    - Checking and removing any duplicate records.
    - Ensuring the final dataset is clean and ready for exploratory data analysis (EDA).

### Final Dataset Preparation

- **Saving Cleaned Data:**
    - The final cleaned dataset is saved as a CSV file for further analysis in the next stages.

---

# **NASA Outgassing Materials Exploratory Data Analysis (EDA)**

## Contents

- Detailed analysis and visualization of the cleaned dataset.
- Identification of trends and insights from the data.
- [View detailed notebook](./NASA_Outgassing_Materials_EDA.ipynb)

---

# **NASA Outgassing Materials ML Modelling**

## Contents

1. **Define Goals**
2. **Feature Engineering**
    - Performance Score Calculation
3. **Initial Model Selection and Implementation**
    - Regression Models
    - Classification Models
4. **Best Model Selection**
5. **Conclusion**
6. **Model Pipeline**
    - [View detailed notebook](./NASA_Outgassing_Materials_ML_Modelling.ipynb)
    - [View ML pipeline notebook](./NASA_Outgassing_Materials_ML_Pipeline.ipynb)

## **1. Define Goals**

### Objective

1. Develop a `linear regression model` to evaluate and predict material performance based on material quality metrics (TML, CVCM, WVR).
2. Use `classification machine learning` to assess material reliability by predicting values for procurement and quality control.

### Understanding Features

- **CVCM:** Measures the percentage of volatile material that can condense on a cold surface during the outgassing test. Lower CVCM values are preferable for high-vacuum environments.
- **WVR:** Measures the amount of water vapor a material absorbs back after being subjected to tests. Lower WVR values are preferable to avoid issues like corrosion or degradation.
- **TML:** Measures the percentage of a material's mass lost during a test. Lower TML indicates better performance in vacuum environments.

## **2. Feature Engineering**

- **Supplier Performance Evaluation:**
    - Calculating performance scores based on TML, CVCM, and WVR.
    - Adding noise to the dataset to simulate realistic scenarios.

## **3. Initial Model Selection and Implementation**

### Regression Models

- **Linear Regression:** Predicting the supplier performance score.
- **Random Forest Regressor:** An alternative regression model for predicting performance.

### Classification Models

- **Logistic Regression:** Classifying suppliers into performance categories.
- **Random Forest Classifier:** A model for classifying performance.
- **Support Vector Machine (SVM):** Another classification model considered.

## **4. Best Model Selection**

- **Regression Model:** Linear Regression is selected based on evaluation scores.
- **Classification Model:** Logistic Regression is chosen for classification tasks.

## **5. Conclusion**

- **Further Research Recommendations:**
    - Expand the dataset to improve model performance.
    - Experiment with additional classification models.
    - Incorporate categorical features for deeper analysis.

- **Potential Application of the Model:**
    - Optimized material selection for specific space applications.
    - Proactive quality control to prevent mission failures.
    - Driving R&D efforts to improve material performance.

---

*This project involves processing and modeling NASA Outgassing Materials data to evaluate and predict material performance. The steps include data preprocessing, feature engineering, model selection, and implementation, concluding with recommendations for future research and potential applications.*

---

# END

*For further details, please refer to the following notebooks:*
- [NASA Outgassing Materials Data Processing](./NASA_Outgassing_Materials_Data_Processing.ipynb)
- [NASA Outgassing Materials Exploratory Data Analysis (EDA)](./NASA_Outgassing_Materials_EDA.ipynb)
- [NASA Outgassing Materials ML Modelling](./NASA_Outgassing_Materials_ML_Modelling.ipynb)
- [NASA Outgassing Materials ML Pipeline](./NASA_Outgassing_Materials_ML_Pipeline.ipynb)

---
