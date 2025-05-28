# Water-Pollution-And-Disease-Analysis
**1. Abstract**

This project investigates the correlation between water pollution parameters and the occurrence of waterborne diseases such as diarrhea, cholera, and typhoid. Using machine learning techniques, the project aims to develop predictive models that can estimate the number of disease cases based on various environmental and socio-economic factors. The dataset, though synthetic, simulates realistic conditions by incorporating features like contaminant levels, access to clean water, population density, healthcare access, and sanitation levels. The ultimate goal is to support policymakers, health organizations, and environmental bodies in making informed decisions for disease prevention and water resource management.

**2. Acknowledgement**

We express our gratitude to the developers of the synthetic dataset that reflects water quality and disease patterns across different regions. We also acknowledge the contribution of the Python open-source community, including libraries like Pandas, Scikit-learn, Seaborn, and Streamlit, for facilitating data analysis, model building, and deployment. Special thanks to the project mentors and guides who provided feedback throughout the development process.

**3. Table of Figures**

1. Histogram of Nitrate Levels
2. Correlation Heatmap between Water Quality Parameters and Disease Incidence
3. Actual vs. Predicted Diarrheal Cases (Regression Plot)
4. Box Plot of Bacteria Count by Region
5. Feature Importance Bar Chart (Random Forest)
6. Confusion Matrix for Logistic Regression
7. Comparative Metric Bar Charts for Regression Models

**4. Problem Statement**

**Specific Problem:** Predict waterborne disease cases using water quality indicators.

**Use Case:** To build a machine learning model that helps predict the likelihood of waterborne diseases based on environmental and demographic data.

**Who Benefits:**

* Environmental Protection Agencies
* Health Departments and NGOs
* Data scientists in public health analytics
* Policy makers involved in water and health infrastructure planning

**5. Algorithms Used**

This project primarily involves **supervised learning** techniques.

* **Linear Regression**: Used for predicting the number of diarrheal cases. Chosen due to its interpretability and effectiveness in regression problems.
* **Decision Tree Regressor** and **Random Forest Regressor**: Employed to improve accuracy and interpretability.
* **Logistic Regression**: Applied for classification-based predictions (e.g., disease presence detection).

These models were selected for their efficiency, transparency, and suitability for medium-sized, structured datasets.

**6. Dataset Description**

* **Source**: Synthetic dataset (user-provided)
* **Total Rows**: 3000
* **Total Columns**: 24
* **Features Include**:

  * Water quality: pH, Turbidity, Dissolved Oxygen, Nitrate, Lead, Contaminant Level, Bacteria Count
  * Socioeconomic: Population Density, GDP per Capita, Sanitation, Access to Clean Water, Healthcare Access
  * Target variables: Diarrheal, Cholera, and Typhoid Cases per 100,000 people
* **Preprocessing Performed**:

  * Checked and confirmed no missing values
  * Categorical encoding for variables like Water Source Type and Treatment Method
  * Feature scaling (if required)
  * Data split: 80% training, 20% testing

**7. Exploratory Data Analysis (EDA)**

EDA provided insights into the structure and relationships within the dataset:

* **Feature Correlation**: Strong correlation between nitrate, contaminant level, and bacteria count with diarrheal diseases
* **Distribution of Target Variables**: Diarrheal cases showed right-skewed distribution
* **Outlier Detection**: Outliers identified in lead and bacteria concentration via box plots

**Graphs Included:**

* Histogram of contaminants (e.g., nitrate)
* Correlation heatmap
* Box plots for feature spread
* Pair plots for multivariate trends

**8. Model Building**

* **Target Variable**: Diarrheal Cases per 100,000 people
* **Features Used**: All numerical features and encoded categorical variables
* **Model Training**: Linear Regression, Decision Tree, and Random Forest
* **Train-Test Split**: 80:20 ratio
* **Tools Used**: Scikit-learn for modeling, evaluation, and predictions

**9. Model Evaluation**

Regression metrics were calculated as follows:

* **Mean Absolute Error (MAE)**: \~4.06
* **Root Mean Squared Error (RMSE)**: \~5.05
* **R-squared Score (R2)**: \~0.80

These scores reflect good model performance on the test data, especially for Linear and Random Forest regressors.

**10. Results and Discussion**

The model showed high accuracy in predicting disease cases, particularly diarrheal. Significant predictors included:

* Contaminant Level (ppm)
* Nitrate and Bacteria Levels
* Access to Clean Water

**Unexpected Findings**: High disease incidence was sometimes observed even in regions with higher sanitation, hinting at unaccounted variables like behavioral factors or secondary contamination sources.

**11. Challenges Faced**

* Limited real-world applicability due to synthetic nature of dataset
* Risk of overfitting due to correlated features
* Lack of time-series data or regional time-based breakdown
* Balancing model complexity with interpretability

**12. Conclusions and Future Work**

**What Worked:**

* Simple regression models were effective and interpretable
* EDA revealed meaningful insights
* Visualizations aided communication of findings

**What Needs Improvement:**

* More robust real-world dataset
* Advanced techniques like feature selection, PCA
* Fine-tuning of hyperparameters

**Future Scope:**

* Try ensemble models like XGBoost or LightGBM
* Integrate time-series and geospatial analysis
* Build a real-time Streamlit app for interactive disease risk prediction
