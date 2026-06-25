# Advanced EDA & Feature Engineering

## Overview

This project focuses on performing Advanced Exploratory Data Analysis (EDA), Data Cleaning, Outlier Detection, and Feature Engineering on an E-Commerce transaction dataset.

The goal was to transform raw transactional data into a clean and structured dataset suitable for future Machine Learning applications.

---

# Tasks Completed

## Data Loading & Inspection

* Loaded the E-Commerce dataset using Pandas.
* Examined dataset structure and dimensions.
* Verified data types of all features.
* Analyzed dataset shape and summary information.

---

## Missing Value Handling

* Identified missing values across all columns.
* Found missing records in the `CouponCode` column.
* Replaced missing values with **"No Coupon"**.
* Verified that the dataset contains no remaining missing values.

---

## Data Formatting

* Converted the `Date` column to datetime format.
* Created new date-related features:

  * OrderMonth
  * OrderYear
  * OrderQuarter

---

## Data Validation

* Verified whether:

```text
TotalPrice = Quantity × UnitPrice
```

* Created a temporary validation feature (`CheckPrice`) to confirm data consistency.
* Removed the validation column after verification.

---

# Exploratory Data Analysis (EDA)

## Univariate Analysis

Performed distribution analysis on:

* Quantity
* UnitPrice
* TotalPrice

Used:

* Histograms
* Distribution Curves (KDE)

---

## Categorical Analysis

Analyzed:

### Product Analysis

* Examined product frequency distribution.
* Identified product occurrence patterns.

### Payment Method Analysis

* Visualized payment method distribution.
* Compared customer payment preferences.

### Order Status Analysis

* Examined distribution of order statuses.
* Analyzed order completion patterns.

---

# Outlier Detection

Outliers were detected using the **Interquartile Range (IQR) Method**.

Features analyzed:

* Quantity
* UnitPrice
* TotalPrice

### IQR Formula

```text
IQR = Q3 − Q1
```

### Lower Bound

```text
Q1 − 1.5 × IQR
```

### Upper Bound

```text
Q3 + 1.5 × IQR
```

---

# Outlier Treatment

Applied outlier treatment using:

```python
numpy.clip()
```

Outliers were capped for:

* Quantity
* UnitPrice
* TotalPrice

This helped reduce the influence of extreme values while preserving the dataset.

---

# Feature Engineering

Created several new features to enhance analytical and Machine Learning capabilities.

| Feature         | Description                                      |
| --------------- | ------------------------------------------------ |
| OrderMonth      | Month in which the order was placed              |
| OrderYear       | Year in which the order was placed               |
| OrderQuarter    | Quarter in which the order was placed            |
| AvgItemValue    | Average value per purchased item                 |
| DiscountApplied | Indicates whether a coupon was used              |
| BasketValue     | Average value per item in cart                   |
| HighValueOrder  | Indicates orders above average transaction value |
| CartRatio       | Ratio of cart items to purchased quantity        |

---

# Correlation Analysis

Performed correlation analysis on numerical features.

### Techniques Used

* Correlation Matrix
* Heatmap Visualization

Purpose:

* Identify relationships between numerical features.
* Detect highly correlated variables.
* Support future feature selection.

---

# Feature Encoding

Converted categorical features into numerical representations using:

```python
pd.get_dummies()
```

Encoded:

* Product
* PaymentMethod
* OrderStatus
* ReferralSource

This prepares the dataset for Machine Learning models.

---

# Dataset Export

Generated and exported:

```text
cleaned_dataset.csv
```

The final dataset contains:

* Cleaned data
* Engineered features
* Treated outliers
* Machine Learning-ready structure

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Google Colab
* GitHub

---

# Project Outputs

* Missing Value Analysis
* Data Cleaning
* Date Feature Extraction
* Univariate EDA
* Categorical Analysis
* Outlier Detection
* Outlier Treatment
* Feature Engineering
* Correlation Analysis
* Encoded Dataset
* Cleaned Dataset Export

---

# Author

**Ajay Parmar**

Data Science Intern

Python | Data Analytics | Machine Learning Enthusiast