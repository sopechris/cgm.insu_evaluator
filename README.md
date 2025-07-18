# 🩺 CGM and Insulin Analysis Notebook

This repository contains the **CGM/Insulin Analysis** Jupyter notebook, which provides a comprehensive workflow for analyzing glucose, insulin, and related physiological data. The notebook is designed for diabetes data analysis, focusing on daily and weekly trends, bootstrapped confidence intervals, and anomaly detection.

## ✨ Features

- **Insulin Intake Analysis:**  
  - Loads and processes insulin data.
  - Calculates daily basal and bolus insulin intake.
  - Visualizes daily insulin totals.

- **Glucose Analysis:**  
  - Loads and filters glucose data.
  - Computes key statistics (mean, median, standard deviation, GMI).
  - Calculates and visualizes Time In Range (TIR) and other glucose distribution metrics.
  - Provides bootstrapped medians and confidence intervals for daily glucose and force data.

- **Ambulatory Glucose Profile (AGP):**  
  - Interactive Dash app for weekly glucose visualization.
  - Optionally overlays PIE and force data.
  - Displays 95% confidence intervals.

- **Anomaly Detection:**  
  - Identifies days with glucose anomalies (2 and 3 standard deviations).
  - Flags days based on TIR, insulin intake, and anomaly presence.
  - Exports daily evaluation to a color-coded Excel file.
 
- **Table creation:**  
  - Creation of table with color guide for ease of analysis.
  - Green for good scenario vs red for bad scenario.


## 🛠️ Requirements

- Python 3.7+
- Jupyter Notebook
- pandas
- numpy
- matplotlib
- seaborn
- plotly
- dash
- openpyxl
- dateutil

Install dependencies with:

```sh
pip install pandas numpy matplotlib seaborn plotly dash openpyxl python-dateutil
```

## 🚀 Usage

1. **Prepare your data files:**  
   - Insulin, glucose, CGM, PIE, and force data in CSV format.
   - Glucose anomaly data in Excel format.

2. **Update file paths:**  
   - In the notebook, specify the correct file paths for your data files where indicated (search for `pd.read_csv('')` and `pd.read_excel('')`).

3. **Run the notebook:**  
   - Open `Anomalies copy.ipynb` in Jupyter Notebook or VS Code.
   - Execute cells sequentially.

4. **Interactive AGP Dashboard:**  
   - Run the Dash app cell to launch the interactive dashboard in your browser.

5. **Export Results:**  
   - The notebook generates a color-coded Excel file (`daily_evaluation.xlsx`) summarizing daily evaluations.

## 📁 File Structure

- `cgm_insu_stats.ipynb` — Main analysis notebook.
- `daily_evaluation.xlsx` — Output Excel file with daily evaluation (generated by the notebook).

## 📝 Notes

- The notebook uses random data generation for demonstration if data files are not provided.
- Update all file paths to your actual data files for real analysis.
- The Dash app requires running in a Python environment that supports web servers.

## 📄 License

This project is provided for academic and research purposes. Please cite appropriately if used in publications.
