# Student Wellbeing Data Cleaning & Analysis

## Overview
This project provides a complete workflow for cleaning, analyzing, and visualizing a student wellbeing dataset. The goal is to prepare the data for modeling, extract key insights, and generate informative visualizations to understand the relationships between study habits, lifestyle factors, and academic performance (CGPA).

## Features
- Cleans raw student wellbeing data (removes duplicates, fills missing values, converts categorical data, handles outliers)
- Saves a cleaned CSV for further analysis or modeling
- Generates visualizations:
  - Correlation heatmap
  - Scatter plot (Hours of Study vs. CGPA)
  - Boxplots (CGPA by Stress Level and Extracurricular Activity) with quartile lines
- Prints key statistical insights and correlation values

## File Structure
```
.
├── data_cleaning.ipynb                # Main Jupyter notebook for cleaning and analysis
├── student_wellbeing_dataset.csv       # Raw input data (CSV)
├── cleaned_student_wellbeing.csv       # Output: cleaned data (CSV)
└── README.md                          # Project documentation
```

## How to Use
1. **Open `data_cleaning.ipynb` in Jupyter Notebook or VS Code.**
2. **Run all cells in order:**
   - The notebook will import libraries, define the main function, and execute the cleaning and analysis pipeline.
   - All graphs and outputs will be displayed inline.
3. **Check the outputs:**
   - Cleaned data is saved as `cleaned_student_wellbeing.csv`.
   - Visualizations and insights are printed in the notebook.

## Data Cleaning Steps
- **Remove Duplicates:** Ensures each student record is unique.
- **Fill Missing Values:** Numerical columns are filled with their mean.
- **Convert Categorical Columns:**
  - `Extracurricular`: Yes → 1, No → 0
  - `Stress_Level`: Low → 0, Medium → 1, High → 2
- **Handle Outliers:** Caps extreme values using the interquartile range (IQR) method.
- **Drop Unnecessary Columns:** Removes `Student_ID` if present.

## Visualizations
- **Correlation Heatmap:** Shows relationships between Hours_Study, Sleep_Hours, Screen_Time, and CGPA.
- **Scatter Plot:** Visualizes the relationship between Hours_Study and CGPA.
- **Boxplots:**
  - CGPA by Stress Level (Low, Medium, High)
  - CGPA by Extracurricular Activity (Yes, No)
  - Horizontal lines indicate Q1 and Q3 quartiles for each group (full width)

## Key Insights Printed
- Correlation values for each factor (e.g., Study Hours vs. CGPA)
- Group means for CGPA by Stress Level and Extracurriculars
- Interpretations of the relationships (positive/negative, strong/moderate)

## Requirements
- Python 3.x
- pandas
- numpy
- seaborn
- matplotlib

Install requirements with:
```bash
pip install pandas numpy seaborn matplotlib
```

## Customization
- To use your own data, replace `student_wellbeing_dataset.csv` with your file (ensure columns match).
- You can modify the cleaning steps or add new visualizations as needed.

## License
This project is provided for educational and research purposes. Feel free to adapt and extend it for your own use.
