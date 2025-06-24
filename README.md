# Spotify-Analysis
 ## Project Goal

The objective of this project is to classify Spotify songs as “Hit” or “Flop” based on their audio features.

### Phase 1: Dataset Exploration

The dataset was successfully loaded and basic information was reviewed.

The target variable (hit vs flop) was found to be imbalanced.


NaN values and incompatible data types were identified.

### Phase 2: Data Cleaning

All missing (null) values were either imputed or removed.

Duplicate rows were dropped.

Columns with inappropriate object types were converted to numeric or category.

Outliers in columns like loudness and energy were detected and handled using the IQR method.

### Phase 3: EDA (Exploratory Data Analysis)
Distributions of audio features were visualized.

Comparisons between hit and flop songs showed patterns:

For example, hit songs tend to have higher energy and danceability.

A correlation matrix was generated to explore feature relationships.

### Phase 4: Preprocessing
Feature scaling was applied using StandardScaler.

Categorical variables were encoded using LabelEncoder or OneHotEncoder.

Irrelevant or highly correlated features were removed.

The dataset was split into train and test subsets.

### Phase 5: Handling Imbalanced Data
Since the target variable was imbalanced, SMOTE was applied.

All modeling was then performed on the balanced dataset.

Class distribution was successfully equalized.

### Phase 6: Model Development
The following algorithms were tested:

Logistic Regression

Random Forest

XGBoost

KNN

5-fold Stratified Cross-Validation was used.

Evaluation was based on the f1_macro metric.

GridSearchCV was used to tune hyperparameters for Random Forest.

### Phase 7: Evaluation
Best performance was achieved by Random Forest and XGBoost models.

Performance metrics such as accuracy, precision, recall, and f1-score were calculated.

The confusion matrix was visualized.

Model decision-making was interpreted using feature importance and SHAP values.

### Phase 8: Visualization & Reporting
Visualizations were created using Seaborn, Matplotlib, and SHAP to support findings.

Model behavior and decision logic were explained clearly.

Most important features included: energy, danceability, loudness, acousticness.

### Final Recommendation

For a model prioritizing interpretability, use Logistic Regression.

For higher performance, use Random Forest or XGBoost.

