# HR Attrition Analysis

Exploratory data analysis of the IBM HR dataset (1,470 employees) to find the factors linked to employee attrition and suggest ways to reduce it.

**Tools:** Python, Pandas, Matplotlib, Seaborn (Google Colab / Jupyter)
**Dataset:** [IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) on Kaggle (`WA_Fn-UseC_-HR-Employee-Attrition.csv`, 1,470 rows, 35 columns)

## Questions answered
1. What is the overall attrition rate?
2. Does overtime affect attrition?
3. Which departments and job roles lose the most people?
4. Does age matter?
5. Does pay matter?
6. Does job satisfaction matter?
7. Which numeric factors are most related to attrition?

## Data preparation
- Dropped 4 columns with no analytical value (3 constant columns and an employee ID).
- Created `AttritionFlag` (1 = left, 0 = stayed) to calculate attrition rates.
- Grouped employees into age groups and income bands (quartiles), and gave the 1-4 satisfaction scores readable labels.

## Key findings
- **Overall attrition is 16.1%** (237 of 1,470 employees).
- **Overtime:** employees working overtime left at 30.5%, against 10.4% for those who did not, about 3x higher.
- **Department:** Sales is highest (20.6%), then HR (19.0%) and R&D (13.8%).
- **Job role:** Sales Representatives are highest at 39.8%, followed by Laboratory Technicians (23.9%) and HR (23.1%). Research Directors are lowest at 2.5%. Some role groups are small, so treat these as patterns.
- **Age:** employees aged 18-25 leave most (35.8%), about 4x the 36-45 group (9.2%).
- **Pay:** the lowest income band leaves at 29.3%, against 10.3% for the highest band.
- **Job satisfaction:** low satisfaction means 22.8% attrition, against 11.3% for very high satisfaction.
- **Correlations:** all numeric correlations with attrition are weak (strongest: -0.17 for total working years and job level), so no single numeric factor explains attrition.

## Recommendations
1. **Manage overtime**, starting with Sales Representatives and Laboratory Technicians.
2. **Retain early-career staff** with mentoring, a clear promotion path and a pay review for entry-level roles.
3. **Review workload and incentives for Sales Representatives**, and run regular satisfaction check-ins.

## Limitations
- This is a single static dataset, so the results show patterns, not proof of cause.
- Age, pay and job level overlap, so these factors are not fully independent.

## How to run
1. Download the CSV from the Kaggle link above, or use the copy in this repo.
2. Open `HR_Attrition_Analysis(1).ipynb` in Google Colab or Jupyter.
3. Upload the CSV next to the notebook and run all cells.
