# Drug Related Adverse Events

## **Introduction**
Post marketing drug adverse event (DAE) surveillance constitutes continuous efforts to 
measure and document drug efficacy and indentify opportunities to minimize patient risk and 
support the entire cycle of drug safety, effectiveness, quality, regulation and public trust.

Our aim is to provide an overview of drug related adverse events that occured in our 
facility in the first quarter of 2024. The principal adverse event of our analysis is 
mortality. Our analysis highlight patient factors and administration factors that highly
expose patients to mortality. 

Accross drug with suffienct reporting volume, our analysis employs Signal detection, a widely 
adopted first step in identifying and monitoring potential DAE to detect drugs with 
dispropotional mortality. Using logistic regression we identify pateint level factors and 
drug administration factors that lead to the exacerbation of the risk of mortality.

## **Data Description**
In fist quater of 2024, 24 thousand DAEs were reported at our facility. The unit of analysis is each drug adverse event 
(DAE). Variables with missingness greater than 30 percent were excluded from our analysis. The shape of the data has 
transformed to 34 columns after processing for missingness. There are 32 distinct `safetyreportversions`. Report version 
show the number of times the original report has been altered with new or updated information. Ninety-nine percent of 
the data ranges form a report version 1 to report version 8. The highest report version is 65 and no duplicate reports 
were detected accross all reports.

Various demographic data about the patient in each report were aggregated and
described. For each event, `reporttype` referred to if the event was spontaneous or from a
clinical study. Severity of each event was documented by recording outcomes for death, hospitalization, and disability.
Each adverse reaction was documented and standardized using the Medical Dictionary for Regulatory Activity Preferred 
Term (MEDRAPT). Additionally, various drug facts were also gathered including, most common drugs, drug indication and 
reaction. Descriptive statistics for other variables including administration route, dosage and treatment duration are 
provided. The four main dosage units were standardized to grams.

**Patient Descriptive Summary**: The mean age is 55 years and the average weight is 70 kilograms (kg). Patients under 
the age of 18 represent are associated with 7 percent of total report of AEs while 93 percent of reports are associated 
with patients older that 18. Females account for a proportion of 57 percent and males account for 42 percent. The death 
rate is 8 percent while the hospitalization rate is 41 percent across both sexes. Among females the death rate is 6 
percent and hospitalization rate is 37 percent. For males, the death rate is 11 percent and hospitalization rate is 46 
percent.

**Drug Summary**: Out of the 24 thousand DAEs reported, 1701 unique drugs were documented in association or causing the 
AE and 2716 unique reactions and 1911 unique drug indications are observed. A table of \*\*top 10\*\* drugs, reactions 
and drug indications are shown below. About 98 percent of drugs are characterized as primary suspects while the other 2 
percent is attributed to concomitant or interacting effects. There are 43 unique administration routes. The average 
treatment duration accross all drugs is 138 days.

## **Results**
**Signal Detection**: Our signal detection analysis identified 19 drugs that showed signals for disproportionate 
reporting of death with a specific drug. The Reporting Odds Ratio (ROR) metric was used during signal analysis with a 
treshold of 2. This treshold is the general accepted baseline for signal monitoring and reporing. Additionally 
confidence intervals of about half of the drugs indicate statistically sound signals while other showed moderate to weak 
signals given that lower bounds are closer to 1.

**Adverse Event Prediction Model**: Building on our signal detection analysis, we used an L2 regularization logistic 
regression model to examine potential drug administration and patient factors that increase the risk of mortality. Our 
analysis was conducted on the 19 drugs identified in the dispropotionality analsyis. An additional criteria for volume 
of cases and a proportion of adverse events were implemented. The model primarily examined drug routes, drug dosage, 
treatment duration and patient level factors. Across all drugs, we identified 4 key trends that are shared below.

*Drug Dosage*: Elevated risk factors increasing the odds of death between 3 and 9 times. Varying administration routes 
and low proportion of less common routes led to moderate observations. In some cases, IV administration routes showed 
moderate to high varying elevated risk for death. Addtitionally, it must be noted that When only one route exists risk 
is primarily attributed to drug dosage, treatement duration and patient factors. 
*Treatment Duration*: Treatement duration showed low to moderate risk of death accross all drugs. 

**Patient Factors**

*Sex*: Higher levels of risk of death is observed for men compared to women across all drugs. 

*Weight*: Drug specific effect were obsereved although the general risk level trends accross drugs is moderate.

**Recomendations**:

*Route Selection*: For drugs with elevated risk, route selection and dose monitoring is critical for patient safety. A 
low cost remedy is to reinforce drug administration guideline while monitoring staffing adequacy.

*Population Specific Adjusments*: High risk patients/porpulation must strickly monitored. Based on model, older adults, 
underweight patients and males patient should be considered high risk and flagged for enhanced monitoring. 
A low cost intervention is to develop administration guidelines and observation timelines for acurate documatation of 
patient treatement progress.

*Drug Specific Guidelines*: For drugs with highest risk signals, targets audits and chart reveiws must performed. Low 
level remedies to be implemented include strict administration supervision, and progress monitoring in EHR system. 
Frequent didactics or round-tables led by pharmacists. Additional line of threat monitoring includes circulating 
documentation of safety guidelines for continuous education and administration management.