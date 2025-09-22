# Medical Cost Analysis (SQL · Python · Power BI)

## Overview
This project analyzes healthcare insurance charges to identify key cost drivers.  
The workflow is **SQL-first**, with Python used for data preview, CSV export, and simple visualizations.  
A companion **Power BI dashboard** presents the outputs interactively.

## Tech Stack
- **SQL (SQLite)** – queries, aggregations, binning  
- **Python (pandas, matplotlib, seaborn)** – run SQL queries, save CSVs, export charts  
- **Power BI** – dashboard with KPIs and drill-downs  

## Methods
- **SQL:**  
  - Group-by aggregations on smoker status, BMI bins, age groups, region, and sex × smoker  
  - Views created for BMI and age binning logic  

- **Python:**  
  - Runs SQL queries with `pandas.read_sql`  
  - Saves CSV outputs to feed Power BI  
  - Exports simple bar charts (matplotlib/seaborn)  

- **Power BI:**  
  - Consumes the CSV outputs  
  - Provides interactive filters, KPIs, and drill-down reporting  

## Key Takeaways
- **Smokers vs Non-Smokers:** Smokers average **~$32K** compared to **~$8K** for non-smokers (~4× higher).  
- **BMI Effect:** Obese patients average **~$16K** vs **~$11K** for those with a healthy BMI.  
- **Age Effect:** Charges rise steadily with age — the **20–29 group averages ~$8K**, while the **60–64 group exceeds ~$20K**.  

**Conclusion:** Smoking status, BMI, and age are the primary cost drivers, while region and sex show comparatively smaller effects.

## Quick Links
- [Notebook](medical_cost_analysis.ipynb) 
- [Dashboard (PDF)](visuals/medical_cost_dashboard.pdf)  
- [Charts (Visuals Folder)](visuals/)  
- [CSV Outputs](data/outputs/)  


