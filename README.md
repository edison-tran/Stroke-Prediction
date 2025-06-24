# A Precuationary Deep Dive Into The Nature of Stroke
**Tools Used: Excel, MS SQL Server, Tableau**

[Dataset Used](https://www.kaggle.com/datasets/atharvasoundankar/global-cybersecurity-threats-2015-2024/data)

[Tableau Visualization](https://public.tableau.com/app/profile/edison.tran/viz/DistributionBasedonStrokeVs_Non-StrokeIndividuals/Dashboard1)

[Tableau Visualization](https://public.tableau.com/app/profile/edison.tran/viz/AnalysisofBMIandGlucoseBasedonAgeandGender/Dashboard2)

[Tableau Visualization](https://public.tableau.com/app/profile/edison.tran/viz/AnalyzingSmokingStatusAffectonStroke/Dashboard3)

# Introduction
Addressing the worldwide health crisis of stroke has grown to become more evident and complicated in an unprecedented manner. As it stands,
stroke is the second leading cause of death globally, being recognized by the World Health Organization. The global instance rate of disabilities 
can also be attributed to adverse experiences of stroke. This project delves into a comprehensive dataset encompassing various patient attributes 
such as gender, age, pre-existing diseases, and smoking status, with the overarching aim of predicting stroke.While stroke rates are inherently tied 
to an aging population,there's a critical and growing trend of younger individuals in low and middle-income countries suffering the ordeal of stroke. 
This unforeseen burden on younger demographics in developing countries displays an underlying public health challenge, calling for an overhaul of risk 
factors and intervention strategies. This discover highlights the need for precautionary actions and strategies to combat stroke's worldwide toll. 


# Motivation and Objective
The increasing prevalence of strokes, particularly in unexpected demographics such as young adults and indivudals living in urban spaces, 
highlights an urgent need for proactive prediction and prevention strategies. Traditional healthcare approaches often fail to identify 
at-risk individuals early enough, resulting in higher mortality and disability rates. This project is driven by the necessity to bridge 
this gap and address pressing questions about stroke risk:

Risk Factor Trends: Which factors most significantly contribute to stroke risk, and how do they evolve across different populations?  

Vulnerable Populations: Which demographic groups are most susceptible to strokes, and what unique risk profiles do they exhibit?  

Predictive Accuracy: How effectively can we forecast stroke risk using available data, and where do current models fall short?

These objectives aim to equip healthcare providers and researchers with actionable insights to prioritize interventions, target 
high-risk groups, and enhance stroke prevention efforts globally.

# Approach
## Data Extraction & Transformation (SQL)
Data Cleaning:  
Imputed missing BMI values with the median to maintain dataset integrity, given its relevance to stroke risk. Created a BMI_Missing 
indicator that provides clarity to instances where individuals had missing BMI values for consistent binary classification. Corrected 
anomalies such as negative ages or inconsistent categorical entries (e.g., smoking status).

Risk Factor Correlation: 
Explored relationships between demographic factors, pre-existing conditions, lifestyle choices (smoking, work type, marriage 
status), and average health metrics (average glucose level, BMI) across different patient segments. Furthermore, this lead to 
identifying  patients with significantly higher or lower health metrics within specific demographic groups in order to determine anomalies.

Analytical Queries:  
Used aggregations to calculate stroke rates by demographic and health factors. Applied advanced SQL techniques, such as window 
functions, CTEs, and aggregate functions in order to assess risk trends across age groups and lifestyle variables.


## Visualization (Tableau)
Heatmaps: Displayed stroke risk correlations across combinations of factors, such as gender, residence type, and line of work.  

Butterfly Graph: Offers analysis on between two variables based on a certain metric such as BMI distribution and age distribution. 

Dual Axis Bar Charts: Emphasizes the relationship between variables such as gender, average glucose level, and smoking status.

# Results
## Age and Demographic Vulnerabilities
Among the various health metrics, analysis revealed a relatively limited stroke rate among younger demographics specifically, 
it was found that 5.6% of female stroke incidents occured before the age of 35. In contrast, stroke incidents for male individuals 
had a 100% incident rate after the age of 40. After the age of 40, both male and female stroke incidents flucuated as age progressed, 
however there was still a steady trend of stroke incidents increasing. Further age analysis reveals that across all age groups, the 
average BMI value for females was marginally less compared to males, however the average glucose level was 12% higher in the 50-69 
age range and 16% higher in the 70+ age range.

## Interplay of Risk Factors
Patients presenting with both hypertension and heart disease exhibited no noticeable changes stroke rates across all age groups. 
Stroke instances with both hypertension and heart disease were also found to be only 5.2% of all stroke incidents, suggesting 
no causation between risk factors and stroke occurrence. When looking at the impact of smoking habits, individuals that had never 
smoked before had a 49% decrease in stroke rate, whereas individuals that had formerly smoked had a 350% increase in stroke rate 
and individuals that still smoke had a 161% increase in stroke rate.

# Conclusion
Through understanding the importance of stroke-related signifiers and establishing them through data-driven modeling, key demographics were 
revealed such as physiological and lifestyle factors strongly associated with stroke. Utilizing SQL and Tableau, the goal of this project was 
to uncover critical insights into stroke risk, heart disease, hypertension, and smoking as key drivers while revealing surprising vulnerabilities 
among younger, urban populations. These findings provide a foundation for targeted healthcare strategies, such as improved screening for 
hypertension in older adults and public health efforts to resolve smoking in high-risk groups. As stroke continues to be a leading cause of death 
and disability worldwide, a data-driven approach to analyzing and predicting its occurrence is not only valuable, but essential for combatting the 
pervasiveness of stroke incidents.
