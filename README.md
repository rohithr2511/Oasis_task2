# Oasis_task2

# README: House Price Prediction using Linear Regression  

This project involves predicting house prices using Exploratory Data Analysis (EDA) and Linear Regression modeling. Below are the essential steps and components of the workflow:  

---

## **Libraries Used**  
- **Data Manipulation & Analysis**: `numpy`, `pandas`  
- **Visualization**: `matplotlib`, `seaborn`  
- **Machine Learning**: `scikit-learn`  

---

## **Dataset Overview**  
- **File**: `Housing.csv`  
- **Shape**: 545 rows × 13 columns  
- **Columns**:  
  - Numerical: `price`, `area`, `bedrooms`, `bathrooms`, `stories`, `parking`  
  - Categorical: `mainroad`, `guestroom`, `basement`, `hotwaterheating`, `airconditioning`, `prefarea`, `furnishingstatus`  

---

## **Data Insights**  
- **Null Values**: None found.  
- **Key Statistical Metrics**:  
  - `price`: Mean = 4.77M, Max = 13.3M  
  - `area`: Mean = 5150, Max = 16,200  
  - Distribution of prices, areas, and other features explored through histograms, KDE plots, scatterplots, and boxplots.  

---

## **Exploratory Data Analysis (EDA)**  
- **Visualizations**:  
  - Histogram of `price` and `area`.  
  - Boxplot: `furnishingstatus` vs. `price`.  
  - Scatterplot: `area` vs. `price`.  
  - Pairplot of all features.  

---

## **Data Preprocessing**  
1. **Binary Variables (Yes/No)**: Converted to `0` (No) and `1` (Yes).  
2. **Dummy Variables**:  
   - For `furnishingstatus`: Created `semi-furnished` and `unfurnished` dummy variables, dropping `furnished` to avoid redundancy.  
3. **Dropped Columns**: Removed `furnishingstatus` after encoding.  
4. **Min-Max Scaling**: Applied scaling to `area`, `bedrooms`, `bathrooms`, `stories`, `parking`, and `price`.  

---

## **Train-Test Split**  
- **Training Data**: 70% of dataset (381 rows).  
- **Testing Data**: 30% of dataset (164 rows).  
- Used `train_test_split` with `random_state=100`.  

---

## **Modeling: Linear Regression**  
1. **Target Variable**: `price` (dependent variable).  
2. **Features**: All other columns (independent variables).  
3. **Model Used**: Linear Regression from `sklearn`.  
4. **Training**:  
   - Fitted the model using scaled training data (`x_train`, `y_train`).  

---

## **Future Steps**  
- Evaluate the model using metrics like R², Mean Absolute Error, etc.  
- Perform predictions on test data.  
- Refine the model by addressing outliers or feature selection.  

