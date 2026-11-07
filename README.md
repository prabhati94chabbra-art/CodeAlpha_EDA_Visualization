# CodeAlpha — Black Friday EDA & Data Visualization

## Project overview
This project completes CodeAlpha Data Analytics Task 2 (Exploratory Data Analysis) and Task 3 (Data Visualization) using the supplied Black Friday transaction dataset.

## Folder structure
```text
CodeAlpha_Black_Friday_EDA_Visualization/
├── data/
│   └── Black Friday Data.csv
├── notebooks/
│   └── Black_Friday_EDA_Visualization.ipynb
├── charts/                  # 15 generated PNG charts
├── outputs/                 # Exported summary CSV files
├── PROJECT_FINDINGS.md
├── README.md
└── requirements.txt
```

## Run the project
1. Install Python 3.10+ (or a compatible Python 3 environment).
2. Open a terminal in this project folder.
3. Install dependencies: `pip install -r requirements.txt`.
4. Start Jupyter: `jupyter notebook`.
5. Open `notebooks/Black_Friday_EDA_Visualization.ipynb` and run all cells from top to bottom.

The notebook searches for the dataset in the project `data/` folder. Keep the folder structure unchanged.

## Analysis included
- Dataset structure, data types, descriptive statistics, and unique values
- Missing-value and duplicate checks
- Univariate analysis of gender, age group, city category, product category, and purchase amount
- Segment comparisons by gender, age, city, marital-status code, city tenure, and occupation code
- Age-by-gender grouped heatmap
- Product-level and customer-level aggregation
- IQR-based potential outlier screening
- Welch two-sample t-test using one observation per customer
- 15 PNG charts and reusable summary CSV exports

## Important limitations
- The dataset does not include a transaction date, so time trends cannot be analyzed.
- It does not contain item quantity, unit price, cost, or profit fields.
- Category and occupation values are codes; the CSV does not provide their descriptive labels.
- The purchase currency is not specified in the supplied CSV.
- Potential outliers are flagged for investigation, not automatically removed.

## Submission note
Before submitting, review the notebook, inspect the generated charts, and add your own short explanation of the key findings. Upload the complete project source to a GitHub repository named in the format required by your internship instructions, e.g. `CodeAlpha_EDA_Visualization`.
