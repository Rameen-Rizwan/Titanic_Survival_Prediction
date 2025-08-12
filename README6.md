# 🚢 Titanic Survival Classification (Task 1)

This project builds a machine learning model to predict whether a passenger survived the Titanic disaster using basic features such as age, gender, class, and fare.  
We compare **Random Forest** and **Logistic Regression** models to evaluate performance using various metrics — including **Accuracy**, **Confusion Matrix**, and the **ROC Curve**.

---

## 📌 Objective

To classify passengers into **Survived (1)** or **Not Survived (0)** based on:

- `Pclass` (Ticket class)
- `Sex`
- `Age`
- `SibSp` (Number of siblings/spouses aboard)
- `Parch` (Number of parents/children aboard)
- `Fare`
- `Embarked` (Port of embarkation)

---

## 🔍 Dataset

- Source: [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)
- Format: CSV
- Target column: `Survived`

---

## 🧼 Steps Performed

### 1. Importing Libraries
Essential Python libraries such as:
- `pandas`, `numpy` for data processing
- `matplotlib`, `seaborn` for visualization
- `sklearn` for machine learning

---

### 2. Data Preprocessing
- Dropped irrelevant columns: `Name`, `Cabin`, `Ticket`, `PassengerId`
- Handled missing values:
  - `Age`: Filled with median
  - `Embarked`: Filled with mode
- Converted categorical columns:
  - `Sex` and `Embarked` encoded using `LabelEncoder`

---

### 3. Feature Selection

Selected features:  
`['Pclass', 'Sex', 'Age', 'SibSp', 'Parch', 'Fare', 'Embarked']`

Target: `Survived`

---

### 4. Model Training

Trained two classifiers:
- 🌲 **Random Forest Classifier**
- ➗ **Logistic Regression**

Used an 80/20 Train-Test split.

---

### 5. Evaluation Metrics

✅ **Accuracy**  
🧮 **Classification Report**  
📉 **Confusion Matrix** (with heatmaps)  
📈 **ROC Curve**

---

## 📊 ROC Curve Explanation

The ROC Curve visualizes how well the model can distinguish between classes.

- **X-axis**: False Positive Rate
- **Y-axis**: True Positive Rate
- The curve compares true positives vs false positives at various thresholds.
- The **closer the curve to the top-left corner**, the better the model.