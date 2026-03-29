# **Predictive Maintenance System using Machine Learning**

Predictive Maintenance System is a comprehensive data science project designed to anticipate machine failures and classify failure types using advanced machine learning techniques. Built on the AI4I dataset, the system combines exploratory data analysis, preprocessing, feature engineering, and multiple ML models to deliver reliable and interpretable predictions for Industry 4.0 applications.

---

## **Features**

**End-to-End ML Pipeline**
Covers the complete lifecycle from data ingestion and preprocessing to model training, evaluation, and interpretation

**Dual Prediction Tasks**

* Binary Classification → Predict whether a machine will fail
* Multi-Class Classification → Identify the type of failure

**Advanced Data Preprocessing**
Handles missing values, removes anomalies, encodes categorical features, and applies feature scaling

**Class Imbalance Handling**
Implements SMOTE (Synthetic Minority Oversampling Technique) to balance rare failure cases

**Feature Engineering & PCA**
Extracts meaningful insights using correlation analysis and Principal Component Analysis

**Multiple ML Models**
Compares performance across Logistic Regression, KNN, SVM, Random Forest, and XGBoost

**Model Interpretability**
Includes feature importance, permutation importance, and decision tree visualization

**Performance Optimization**
Uses GridSearchCV for hyperparameter tuning and F2-score prioritization for recall-sensitive scenarios

---

## **Tech Stack**

**Language**
Python 3.8+

**Data Analysis**
pandas, numpy

**Visualization**
matplotlib, seaborn

**Machine Learning**
scikit-learn, XGBoost, imbalanced-learn

**Model Interpretation**
Permutation Importance, PCA

---

## **Dataset Description**

The project uses the **AI4I Predictive Maintenance Dataset** from the UCI Repository.

### **Dataset Characteristics**

* 10,000 records
* 14 features
* Mix of numerical and categorical variables

### **Key Features**

* Air Temperature
* Process Temperature
* Rotational Speed
* Torque
* Tool Wear
* Machine Type (L, M, H)

### **Target Variables**

* **Machine Failure (Binary)**
* **Failure Type (Multi-Class)**

  * Tool Wear Failure (TWF)
  * Heat Dissipation Failure (HDF)
  * Power Failure (PWF)
  * Overstrain Failure (OSF)
  * Random Failure (RNF)

---

## **Project Workflow**

### **1. Exploratory Data Analysis (EDA)**

* Checked for missing values and duplicates
* Analyzed feature distributions and outliers
* Identified correlations between variables

### **2. Data Preprocessing**

* Removed ambiguous and inconsistent data points
* Encoded categorical features
* Applied StandardScaler for normalization

### **3. Handling Imbalanced Data**

* Used SMOTE to balance failure vs non-failure cases
* Maintained realistic feature distributions

### **4. Feature Engineering**

* Explored feature combinations (e.g., Power = Torque × Speed)
* Applied PCA to reduce dimensionality and improve interpretability

### **5. Model Training**

Implemented and compared:

* Logistic Regression (Benchmark)
* K-Nearest Neighbors (KNN)
* Support Vector Machine (SVM)
* Random Forest
* XGBoost

### **6. Hyperparameter Tuning**

* Used GridSearchCV
* Optimized models using F2 Score (recall-focused metric)

### **7. Evaluation Metrics**

* Accuracy
* AUC (ROC Score)
* F1 Score
* F2 Score (higher weight on Recall)

---

## **Model Performance Insights**

**Best Performing Model**
XGBoost achieved the highest accuracy and overall performance

**Fastest Model**
KNN provided instant predictions but slightly lower accuracy

**Balanced Models**
Random Forest and SVM offered strong performance with better interpretability

**Key Observations**

* Tool Wear, Torque, and Rotational Speed are the most important features
* Machine Type has minimal impact on prediction
* PCA revealed three dominant components:

  * Temperature
  * Power
  * Tool Wear

---

## **How It Works**

The system trains models to learn patterns from sensor data and predicts outcomes based on learned relationships.

### **Binary Classification**

Predicts:

```
Will the machine fail or not?
```

### **Multi-Class Classification**

Predicts:

```
What type of failure will occur?
```

### **Core Objective Function**

Optimized using recall-heavy metric:

F_{\beta} = (1 + \beta^2) \frac{Precision \cdot Recall}{\beta^2 \cdot Precision + Recall}

(β = 2 prioritizes minimizing missed failures)

---

## **Getting Started**

### **1. Installation**

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn
```

### **2. Dataset Setup**

* Download AI4I dataset from UCI repository
* Place CSV file in project directory

### **3. Run the Project**

Execute the notebook or Python scripts step by step:

* Data preprocessing
* Model training
* Evaluation

---

## **Key Learnings**

* Handling imbalanced datasets is critical in real-world ML problems
* Feature engineering can significantly impact model performance
* Trade-off exists between accuracy and interpretability
* Recall-focused metrics are essential in safety-critical systems

---

## **Future Enhancements**

* Real-time sensor integration (IoT systems)
* Deployment using Flask or FastAPI
* Dashboard visualization (Streamlit)
* Deep learning models for time-series prediction

---

## **Conclusion**

This project demonstrates how machine learning can significantly reduce maintenance costs and downtime by predicting failures in advance. By combining strong data preprocessing, balanced learning, and model comparison, the system provides both accurate and actionable insights for industrial applications.

* convert this into a **GitHub-ready README.md (with badges + visuals)**
* or create a **resume-worthy project description (very important for AI roles)** 🚀
