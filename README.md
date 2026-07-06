# Capstone Project 1 — Working with NumPy Matrices (NHANES Body Measurements)

## Overview

This project analyses adult body measurement data from the **National Health and
Nutrition Examination Survey (NHANES) 2020**. Using NumPy matrix operations, the
notebook explores, visualises, and statistically compares body measurements for
male and female participants, and derives health-related indices such as **BMI**,
**waist-to-height ratio (WHtR)**, and **waist-to-hip ratio (WHR)**.

The analysis was completed as part of a Data Science with Python course capstone.

## Author

**Stutipriya Shadangi**

## Dataset

Two excerpts from the NHANES 2020 dataset, sourced from the
[gagolews/teaching-data](https://github.com/gagolews/teaching-data/tree/master/marek)
repository:

| File | Description |
|---|---|
| `nhanes_adult_male_bmx_2020.csv` | Body measurements for adult male participants |
| `nhanes_adult_female_bmx_2020.csv` | Body measurements for adult female participants |

Each dataset contains seven columns:

1. Weight (kg)
2. Standing height (cm)
3. Upper arm length (cm)
4. Upper leg length (cm)
5. Arm circumference (cm)
6. Hip circumference (cm)
7. Waist circumference (cm)

> The CSV files are expected in a `data/` subfolder relative to the notebook
> (e.g. `data/nhanes_adult_male_bmx_2020.csv`).

## Repository Structure

```
.
├── data/
│   ├── nhanes_adult_male_bmx_2020.csv
│   └── nhanes_adult_female_bmx_2020.csv
├── capstone1.ipynb
└── README.md
```

## Notebook Contents

The notebook (`capstone1.ipynb`) is organised into the following sections:

1. **Setup & Imports** — loads NumPy, pandas, matplotlib, seaborn, and SciPy.
2. **Load Data** — reads the CSV files into `male` and `female` NumPy matrices and removes missing values.
3. **Histograms of Weights** — compares male and female weight distributions on a shared x-axis scale.
4. **Box-and-Whisker Plot (Weights)** — compares male and female weight distributions side by side.
5. **Numerical Aggregates** — computes and interprets measures of location, dispersion, and shape for both weight distributions.
6. **BMI Calculation** — adds a BMI column to the female matrix.
7. **Standardisation (z-scores)** — creates `zfemale`, a standardised version of the female dataset.
8. **Scatterplot Matrix & Correlations** — visualises pairwise relationships and computes Pearson/Spearman correlations for standardised height, weight, waist, hip, and BMI.
9. **Waist Ratios** — computes waist-to-height and waist-to-hip ratios for both sexes.
10. **Box-and-Whisker Plot (Ratios)** — compares WHtR and WHR distributions across sexes.
11. **BMI vs. WHtR vs. WHR Discussion** — advantages and disadvantages of each index.
12. **Extreme BMI Cases** — prints standardised measurements for the 5 lowest- and 5 highest-BMI female participants.
13. **Conclusion** — summary of key findings.

Each code cell is preceded by a brief explanation of its purpose and followed by a
discussion of the results, in line with a formal report style suitable for
stakeholders.

## Requirements

- Python 3.x
- numpy
- pandas
- matplotlib
- seaborn
- scipy

Install dependencies with:

```bash
pip install numpy pandas matplotlib seaborn scipy
```

## Usage

1. Clone this repository.
2. Ensure the two NHANES CSV files are placed in the `data/` folder.
3. Open `capstone1.ipynb` in Jupyter Notebook or JupyterLab.
4. Run all cells sequentially from top to bottom.

```bash
jupyter notebook capstone1.ipynb
```

## Key Findings

- Male participants are, on average, heavier and taller than female participants, with greater dispersion in weight.
- Both weight distributions are positively skewed, with a heavier right tail.
- BMI is strongly correlated with weight, waist circumference, and hip circumference in females, while height shows little correlation with these measures.
- Males exhibit a higher waist-to-height ratio; females show a lower waist-to-hip ratio, consistent with known sex differences in fat distribution.
- No single body composition index (BMI, WHtR, WHR) is sufficient on its own — together they provide a more complete picture of health status.

## License

This project is for educational purposes as part of a Data Science capstone assignment.
