You are an expert in Machine Learning, Data Science, and Academic Research Writing.

I am working on TWO separate but related research papers using rainfall datasets.

---

## PROJECT STRUCTURE

I have three datasets (CSV files):

1. Chennai (common base dataset)
2. Bengaluru
3. Uttarkashi

I am building TWO research papers:

---

PAPER 1:
"Machine Learning–Based Urban Flood Risk Assessment with Cross-City Validation: Chennai and Bengaluru"
------------------------------------------------------------------------------------------------------

* Chennai → Training dataset
* Bengaluru → Cross-city validation dataset
* Focus → Urban flooding comparison

---

PAPER 2:
"Machine Learning–Based Flood Risk Assessment in Contrasting Terrains: Chennai and Uttarkashi"
----------------------------------------------------------------------------------------------

* Chennai → Training dataset
* Uttarkashi → Validation dataset
* Focus → Coastal vs mountainous flood behavior

---

IMPORTANT:
The MACHINE LEARNING PIPELINE must remain SAME for both papers.
Only analysis, interpretation, and conclusions should differ.

---

## TASKS (DO STEP-BY-STEP)

### STEP 1: DATA LOADING & CLEANING

* Load all three CSV files
* Inspect structure, missing values
* Standardize columns (Date, Rainfall)
* Convert Date into Year, Month

---

### STEP 2: FEATURE ENGINEERING (COMMON PIPELINE)

For ALL datasets, create:

* Year
* Monthly rainfall aggregation
* Total yearly rainfall
* Monsoon rainfall (June–September)
* Extreme rainfall events (define threshold)
* Optional: rolling averages

---

### STEP 3: TARGET VARIABLE CREATION

Create Flood_Label using historical flood years:

* Chennai → 2015, 2023
* Bengaluru → 2022
* Uttarkashi → 2013, 2021

Flood_Label:
1 = flood year
0 = non-flood year

---

### STEP 4: FINAL DATASET STRUCTURE

Each dataset should look like:

* Year
* Monsoon_Rainfall
* Total_Rainfall
* Extreme_Rain_Count
* Flood_Label

---

### STEP 5: MODEL DEVELOPMENT (COMMON FOR BOTH PAPERS)

Train ONLY on Chennai dataset:

Models:

* Logistic Regression (baseline)
* Random Forest (main model)

Perform:

* Train-test split
* Model training
* Predictions
* Evaluation metrics:
  Accuracy, Precision, Recall, F1-score

---

### STEP 6: CROSS-DATASET VALIDATION

CASE 1 (Paper 1):

* Train on Chennai
* Test on Bengaluru
* Evaluate performance

CASE 2 (Paper 2):

* Train on Chennai
* Test on Uttarkashi
* Evaluate performance

---

### STEP 7: COMPARATIVE ANALYSIS (VERY IMPORTANT)

For Paper 1 (Chennai vs Bengaluru):

* Both are urban cities
* Compare rainfall patterns
* Compare model performance
* Explain urban flooding differences

For Paper 2 (Chennai vs Uttarkashi):

* Coastal vs mountainous terrain
* Compare rainfall behavior
* Explain why model generalization changes
* Highlight terrain-driven flood mechanisms

---

### STEP 8: EXPLAINABLE AI (SHARED)

* Extract feature importance (Random Forest)
* Identify most influential rainfall factors
* Compare importance across datasets

---

### STEP 9: OUTPUT REQUIREMENTS

I want:

1. Clean Python code (Jupyter Notebook ready)
2. Separate evaluation results for both papers
3. Graphs:

   * Rainfall trends
   * Model performance
   * Feature importance
4. Interpretation for BOTH papers separately
5. Clear explanation of:

   * Why model works better/worse across cities
   * Limitations of rainfall-only approach

---

### STEP 10: RESEARCH PAPER WRITING SUPPORT

Help generate:

For BOTH papers:

* Abstract
* Introduction
* Methodology
* Results
* Discussion
* Conclusion

But ensure:

* Same methodology section
* Different analysis + discussion sections

---

CONSTRAINTS:

* Keep everything beginner-friendly
* Avoid heavy GIS or satellite processing
* Use only tabular ML
* Ensure code runs on a normal laptop

---

OUTPUT STYLE:

* Step-by-step
* Clean code blocks
* Clear explanations
* Structured like a real research workflow

---

Start from STEP 1 and proceed sequentially.
