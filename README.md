# ML-Volatility-GP-Project
# Gaussian Process Framework for Predicting Daily Volatility and Risk States in Equity Markets

This repository contains all Python code used for **Task 1** of the MSc coursework project.  
The work investigates how Gaussian Process Regression (GPR) and Gaussian Process Classification (GPC) can be applied to daily financial time series to model volatility and identify high-risk market states.

---

## 📁 Project Structure

```
Task1_Code/
    01_data_download.py
    02_feature_engineering.py
    03_train_test_split_scaling.py
    04_gp_regression_rbf.py
    05_gp_regression_matern.py
    06_gp_regression_rq.py
    07_gp_classification.py
    08_metrics_and_plots.py
figures/
    confusion_matrix.png
    regression_scatter.png
    regression_line.png
README.md
```

Each file corresponds to the workflow described in the coursework report and can be executed independently.

---

## 📊 Dataset

The project uses historical daily data for the **S&P 500 Index (GSPC)**.

Data Source:  
https://finance.yahoo.com/quote/%5EGSPC/history

Data is downloaded programmatically:

```python
import yfinance as yf
data = yf.download("^GSPC", start="2010-01-01", progress=False)
```

No dataset is included in this repository, as it is publicly accessible and downloaded automatically when running the scripts.

---

## ▶️ How to Run the Code

### 1. Install Dependencies

```
pip install -r requirements.txt
```

### 2. Run the workflow in order:

```
01_data_download.py
 02_feature_engineering.py
03_train_test_split_scaling.py
04_gp_regression_rbf.py
05_gp_regression_matern.py
06_gp_regression_rq.py
07_gp_classification.py
08_metrics_and_plots.py
```

Each script prints key output to the console and saves plots (where relevant) in the **figures/** folder.

---

## 🧪 Key Methods Used

- Gaussian Process Regression  
  - RBF Kernel  
  - Matern Kernel  
  - Rational Quadratic Kernel  
- Gaussian Process Classification  
- Feature engineering for financial volatility  
- Scaling and train–test splitting  
- Evaluation metrics and plots  

More details for each step can be found in the main coursework report.

---

## 📈 Summary of Key Results

- Matern kernel produced the strongest regression performance.  
- Gaussian Process Classification achieved **~98% accuracy**, with clear separation between high-risk and low-risk days.  
- Feature engineering (log returns, rolling volatility, momentum, volume metrics) contributed significantly to model stability.

Full tables and figures are included in the project Appendix.

---

## 📝 Requirements

Create a file named **requirements.txt** with:

```
numpy
pandas
matplotlib
scikit-learn
yfinance
scipy
seaborn
```

---

## 👤 Author

**Devika**  
MSc Data Science and Computational Intelligence  
Coventry University

---

## 🔗 Coursework Submission Note

This repository contains all original Python scripts used for Task 1.  
The link is provided in the Appendix of the written coursework to satisfy the requirement of supplying executable code.

