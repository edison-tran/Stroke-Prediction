# A Precuationary Deep Dive Into The Nature Of Stroke
**Tools Used: Excel, MS SQL Server, Tableau**

[Dataset Used](https://www.kaggle.com/datasets/atharvasoundankar/global-cybersecurity-threats-2015-2024/data)

[Tableau Visualization](https://public.tableau.com/app/profile/edison.tran/viz/DistributionBasedonStrokeVs_Non-StrokeIndividuals/Dashboard1)

[Tableau Visualization](https://public.tableau.com/app/profile/edison.tran/viz/AnalysisofBMIandGlucoseBasedonAgeandGender/Dashboard2)

[Tableau Visualization](https://public.tableau.com/app/profile/edison.tran/viz/AnalyzingSmokingStatusAffectonStroke/Dashboard3)

# Introduction
Addressing the worldwide public health crisis of stroke incidents is growing to be more evident and complicated. As it stands,
stroke is the second leading cause of death globally, being recognized by the World Health Organization. The global instance rate of 
disabilities can also be attributed to adverse experience of stroke. While stroke rates are inherently tied to an aging population,
there's a critical and growing trend of younger individuals in low and middle income countries suffering the ordeal of stroke. This
unforeseen burden on younger demographics in developing countries displays an underlying public health challenge, calling for an overhaul
of risk factors and intervention strategies. This alarming statistic underscores the critical need for proactive strategies to combat 
stroke's worldwide toll. This project delves into a comprehensive dataset encompassing various patient attributes such as gender,
age, pre-existing diseases, and smoking status, with the overarching aim of predicting stroke.


# Motivation and Objective
The increasing prevalence of strokes, particularly in unexpected demographics like younger adults and urban dwellers, highlights an urgent need for proactive prediction and prevention strategies. Traditional healthcare approaches often fail to identify at-risk individuals early enough, resulting in higher mortality and disability rates. This project is driven by the necessity to bridge this gap and address pressing questions about stroke risk:
Risk Factor Trends: Which factors most significantly contribute to stroke risk, and how do they evolve across different populations?  

Vulnerable Populations: Which demographic groups are most susceptible to strokes, and what unique risk profiles do they exhibit?  

Predictive Accuracy: How effectively can we forecast stroke risk using available data, and where do current models fall short?

These objectives aim to equip healthcare providers and researchers with actionable insights to prioritize interventions, target high-risk groups, and enhance stroke prevention efforts globally.

# Approach
## Data Extraction & Transformation (SQL)
Data Cleaning:  
Imputed missing BMI values with the median to maintain dataset integrity, given its relevance to stroke risk. Corrected anomalies such as negative ages or inconsistent categorical entries (e.g., smoking status).

Analytical Queries:  
Used aggregations to calculate stroke rates by demographic and health factors. Applied advanced SQL techniques, such as window functions and Common Table Expressions (CTEs), to assess risk trends across age groups and lifestyle variables.


## Visualization (Tableau)
Heatmaps: Displayed stroke risk correlations across combinations of factors, such as gender, residence type, and line of work.  

Butterfly Graph: Offers analysis on between two variables based on a certain metric such as BMI distribution and age distribution. 

Dual Axis Bar Charts: Emphasizes the relationship between variables such as gender, average glucose level, and smoking status.
