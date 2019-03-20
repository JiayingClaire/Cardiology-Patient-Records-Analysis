### Cardiology-Patient-Records-Analysis

#### About The Data
This analysis is focusing on a simulated data set related to electronic health records and long-run outcomes for cardiology patients. The data is written in long format (e.g. panel data). Each patient’s records are collected over time in one or more rows. Each row corresponds to a period of time. During this time, the patient’s status is recorded in terms of medications, hospitalizations, and complications. Each patient is followed until either death or the end of the follow-up period.

#### Goal: Analyze the effectiveness of each cardiology medication with unadjusted odds ratios

#### Steps:
* Cleaned and inspected the electronic health records for cardiology patients in the panel data format in R (dataset: 2.43 million health records with 13 variables)

* Analyzed the impact of medicine ACE Inhibitors/ Beta Blockers/ Statins by summarizing the utilization and the Crude Event Rates (deaths/ heart attacks/ hospitalizations)

* Concluded the potential rank of the effectiveness: Statins > ACE Inhibitors > Beta Blockers) by computing the unadjusted odds ratio 

#### Variables Description
* id: This is a unique identifier for each patient. 

* begin: This is the beginning of the observation interval. This is defined as the number of days since the patient entered the study (see the definition of age above). The patient’s age at the beginning of the interval is the age variable (in years) plus the begin variable (in days).

* end: This is the end of the observation interval. This is defined as the number of days since the patient entered the study (see the definition of age above). The observation interval is half open. This means that the begin date is included, while the end date is excluded. For patients with more than one row of records, the beginning of the next row should correspond to the end of the previous row. Any mismatches between these values constitute gaps in coverage, when we lack records on a patient. (For instance, if a patient switches insurance companies and then switches back, then we might lose a year’s worth of records.) The length of an interval in one row is therefore end - begin days. The patient’s age at the end of the interval is the age variable (in years) plus the end variable (in days).

* age: This is the patient’s age in (rounded) years at the time of entry into the study – at the first diagnosis of coronary heart disease. For patients with multiple records in different rows, the age should be the same in every entry. For the purpose of this study, all of the patients should be at least 18 years old.

* diabetes: This is an indicator of whether the patient had a diagnosed case of diabetes mellitus.

* hypertension: This is an indicator of whether the patient had a diagnosed case of hypertension.

* kidney_disease This is an indicator of whether the patient had a diagnosed case of kidney disease.

* ace: This is an indicator of adherence for ACE Inhibitors, a common cardiovascular drug. This information is recorded based on a self-reported log that tracks the patient’s daily usage of the medicine. Therefore, we have the following coding for the values of ace: 1: Possession/ 0: No possession.

* beta.blocker: This is an indicator for adherence of Beta Blockers, a cardiovascular medicine. It has the same coding as that of ace.

* statin: This is an indicator for adherence of Statins, another cardiovascular medicine. It has the same coding as that of ace and beta.blocker.

* hospital: This is an indicator of whether the patient was in the hospital during the interval. Its values are coded as: 1: Hospitalized / 0: Not Hospitalized.

* heart.attack: This is an indicator of whether the patient suffered a heart attack. When this occurs, the patient is assumed to go to the hospital and stay for some period of time (e.g. 1-7 days). The heart attack is assumed to happen at the beginning of the interval, and the remainder of this time is considered a recovery period. The values are coded as: 1: Suffered a heart attack. / 0: No heart attack.

* death: This is an indicator of the end of the patient’s life. Its values are coded as: 1: End of life / 0: Patient is still alive.
