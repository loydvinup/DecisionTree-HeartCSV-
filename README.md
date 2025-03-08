# Decision Tree - Heart Disease Prediction  

## Overview  
This project implements a **Decision Tree Classifier** to predict heart disease based on patient data. The dataset contains **303 records** with **14 medical attributes**, such as **age, cholesterol levels, blood pressure, heart rate, and chest pain type**.  

The goal is to classify whether a patient has heart disease (`target = 1`) or not (`target = 0`) based on these medical attributes. The project includes **data preprocessing, exploratory data analysis (EDA), model training, and evaluation** using **Scikit-learn's DecisionTreeClassifier**.  

## Dataset  
📂 **File:** `heart (5).csv`  
📊 **Rows:** 303  
🔢 **Columns:** 14  

### **Key Features:**  
- **age** – Patient’s age  
- **sex** – Gender (1 = Male, 0 = Female)  
- **cp** – Chest pain type (1 = Typical Angina, 2 = Atypical Angina, 3 = Non-anginal, 4 = Asymptomatic)  
- **trestbps** – Resting blood pressure (mm Hg)  
- **chol** – Serum cholesterol (mg/dl)  
- **fbs** – Fasting blood sugar (> 120 mg/dl, 1 = True, 0 = False)  
- **restecg** – Resting electrocardiographic results (0 = Normal, 1 = ST-T wave abnormality, 2 = Left ventricular hypertrophy)  
- **thalach** – Maximum heart rate achieved  
- **exang** – Exercise-induced angina (1 = Yes, 0 = No)  
- **oldpeak** – ST depression induced by exercise relative to rest  
- **slope** – Slope of peak exercise ST segment (1 = Upsloping, 2 = Flat, 3 = Downsloping)  
- **ca** – Number of major vessels (0-3) colored by fluoroscopy  
- **thal** – Thallium stress test result (1 = Fixed defect, 2 = Reversible defect, 3 = Normal)  
- **target** – Heart disease (1 = Present, 0 = Not Present)  

---

## Project Workflow  
### **1️⃣ Data Preprocessing**  
- Loads `heart (5).csv` into a Pandas DataFrame  
- Handles missing values and removes duplicates  
- Converts categorical variables where necessary  

### **2️⃣ Exploratory Data Analysis (EDA)**  
- Displays **summary statistics** (mean, standard deviation, min/max values)  
- Uses **box plots** to detect outliers in key features  
- **Counts and visualizes** feature distributions (e.g., chest pain type, blood sugar levels)  

### **3️⃣ Model Training - Decision Tree Classifier**  
- Splits the data into **training (70%) and testing (30%)** sets  
- Trains a **Decision Tree Classifier (`max_depth=2`)**  
- Predicts outcomes on the test set  

### **4️⃣ Model Evaluation**  
- Computes **accuracy score** and **confusion matrix**  
- Measures **true positives (TP), false positives (FP), true negatives (TN), and false negatives (FN)**  
- Compares model performance with different `max_depth` values  

### **5️⃣ Hyperparameter Tuning**  
- Loops through different values of `max_depth` to find the best-performing model  
- Plots the effect of `max_depth` on accuracy  

### **6️⃣ Visualization**  
- Uses **Seaborn** to visualize age distribution among heart disease patients  
- Plots the **confusion matrix** to analyze misclassifications  

---

## **Technologies Used**  
🚀 **Python Libraries:**  
- **Pandas** – Data manipulation  
- **NumPy** – Numerical computations  
- **Matplotlib & Seaborn** – Data visualization  
- **Scikit-learn** – Machine learning model training and evaluation  

## **Results & Insights**  
- **Higher chest pain types (3 & 4)** correlate strongly with heart disease  
- **ST depression (`oldpeak`) is a critical indicator** of heart disease presence  
- **Decision Trees perform well but require hyperparameter tuning** for optimal performance  

## **Future Improvements**  
🔹 Experiment with **Random Forest** for better performance  
🔹 Optimize tree depth using **GridSearchCV**  
🔹 Apply **Feature Engineering** to improve model accuracy  

