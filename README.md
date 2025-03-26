# blood-donation-analysis

# Blood Donation Prediction and Donor Profiling

This project performs an in-depth exploratory data analysis (EDA), feature engineering, clustering, and machine learning modeling on the **Blood Transfusion Service Center dataset**. The goal is to identify patterns in donor behavior and predict whether a person will donate blood in March 2007.

---

## Dataset

- **Source:** UCI Machine Learning Repository  
- **Title:** Blood Transfusion Service Center  
- **Observations:** 748  
- **Target variable:** `Donated in March 2007` (binary)

### Features:
| Variable       | Description                                | Unit            |
|----------------|--------------------------------------------|------------------|
| Recency        | Months since last donation                 | Months           |
| Frequency      | Total number of donations                  | Count            |
| Time           | Months since first donation                | Months           |
| Target         | Donated in March 2007 (0 = No, 1 = Yes)    | Binary           |

---

## 🔍 Project Structure

### 1. Exploratory Data Analysis (EDA)
- Summary statistics and distribution plots for all numerical features
- Pie chart for the categorical `Target` variable
- Correlation matrix and pairwise plots
- Outlier detection using IQR method

### 2. Feature Engineering
New variables derived:
- `DonationRate` = Frequency / Time
- `RecencyRatio` = Recency / Time
- `RecencyLevel` (binned)
- `FrequencyLevel` (binned)
- `DonorType` = RecencyLevel + FrequencyLevel

### 3. Clustering
- KMeans clustering on scaled and encoded features
- PCA for 2D visualization of clusters
- Cluster profiling (average behavior, % of donors per cluster)

### 4. Supervised Modeling
Models trained to predict donation:
- Logistic Regression
- Random Forest
- XGBoost
- K-Nearest Neighbors

### 5. Model Evaluation
- Confusion Matrix
- Classification Report
- ROC AUC Curve
- Cross-Validation (5-Fold) for generalization
- Model comparison table with quantitative + qualitative assessment

---

## Insights and Use Cases

- **Behavioral profiling**: Donor segmentation into actionable groups
- **Targeting strategies**: Who to recall, reward, or remove
- **Model deployment**: Ready-to-use pipeline with preprocessing steps

---

## Tech Stack

- Python (Pandas, Scikit-learn, Seaborn, Matplotlib)
- XGBoost
- Jupyter Notebook

---

## Files

| File                  | Description                                  |
|-----------------------|----------------------------------------------|
| `blood.csv`           | Raw dataset from UCI                         |
| `notebook.ipynb`      | Complete analysis and modeling pipeline      |
| `README.md`           | Project documentation                        |

---

## 🏁 How to Run

1. Clone the repository
2. Install requirements:  
   `pip install -r requirements.txt`
3. Open `notebook.ipynb` in Jupyter or VSCode
4. Follow the workflow step by step

---

## License

This project is for academic and educational purposes.

---

## Credits

Based on data from Yeh, I-Cheng et al. (2008):  
*Knowledge discovery on RFM model using Bernoulli sequence*, Expert Systems with Applications.

