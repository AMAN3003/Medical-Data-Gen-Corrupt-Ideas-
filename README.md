
## Dependencies between Medical data attributes modeled for each longitudinal Medical Data  

###### [ I ]
** [ 1 ]**
**BMI** -The body mass index, or **BMI**, is a calculation used to determine your level of body fat and used to Predict chronic Diseases Risks.The BMI is defined as the body Weight divided by the square of the body height, expressed in of kg/m2.
* **(Dependency)** BMI Depends on the Height / (Weight)2 . BMI is Continuous attribute which depends on the Continuous attributes Height and Continuous attribute Weight.
* **(Error and variation)**-In real world BMI index are estimated in Health Survey with the Measure Value of Height and Weight of the People, as every Measurement have some errors of the estimate so will have Height and Weight and indeed will have the BMI,which is Relative Standard Error of the Estimate for the BMI for different Height and Weight Intervals.This will be used to generate Corrupted BMI.For Variation We will plot the generated  BMI  vs the Height and Weight and compare the result with health survey reports of different years.

###### [ II ]
**[ 2 ]**
**Hemoglobin**-Hemoglobin is the protein molecule in red blood cells that carries oxygen from the lungs to the body's tissues and returns carbon dioxide from the tissues back to the lungs.
* **(Dependency)** Hemoglobin (Continuous) depends on the age(Continuous) and then on sex(Categorical). Hemoglobin values are relatively low among the youngest and oldest age groups.with the lowest found at age below 5. While Hemoglobin values are highest between the adulthood and 50 years for Men whereas trend for female is decreasing Hemoglobin with age from adulthood.Using the Distribution(% of the specified Age-Interval vs Hemoglobin ) data of the  adults,by age and sex we generate Hemoglobin.
*  **(Error and variation)** -in real world errors in Hemoglobin values are :
a)Error caused by personal technique(Inadequate Mixing Blood) b)errors in  Hemacytometry c)platelets counting errors d)Sampling and Measurement errors
Based on the Probability of the above errors we will generate the corrupted Hemoglobin

###### [ III ]
**[ 3 ]**
**Resting Pulse Rate(RPR)**-Resting Pulse Rate or Heart Rate is the number of times your heart beats per minute. Normal heart rate varies from person to person.
* **(Dependency)** RPR (Continuous) depends on the age(Continuous) and then on sex(Categorical). RPR is inversely associated with age.RPR decreased significantly with increasing age for children and adolescents of both sexes. For male RPR plateaus to steady state level at adult while it plateaus much later in adulthood for female.The frequency distribution of RPR by age groups and sex approx to a normal distribution used to generate RPR
* **(Error and variation)** in real world RPR has imperfect data for three major reasons:
a)Position of Patients while measuring RPR 
b)The design of the survey(Resting time) 
c)Human error overlooking ,calculation mistake

Average errors of RPR  were 1.89, 1.89 and 1.80 bpm for standing, sitting and supine positions of patients.Resting Time given before measuring RPR to patients depends on the survey results in error in data. Human errors result in slight variation in RPR.
Based on the Probability of the above errors we will generate corrupted RPR.

###### [ IV ]
**[ 4 ]**
**Glucose Level**-The amount of glucose (“sugar”, measured in mg/dL) in your blood changes throughout the day and night. Your levels will change depending upon when, what and how much you have eaten, and whether or not you have exercised.
* **(Dependency)** Blood Glucose Level(Continuous attribute) depends on the Age(Continuous) and the Sex(Continuous).It rises steadily with age for both the sexes however, the level is consistently slightly higher for women than for men. Using  the Health Survey Statistics we would generate the glucose level  based on different Age Interval and then on sex.
* **(Error and variation)**-In real world glucose level data are imperfect for two major reason: a)Sampling Errors b) The design of the Survey (glucose tolerance test)    
For the Sampling Errors we can use the standard error(from the survey data) in the  mean glucose level measurement for different age intervals to generate corrupted glucose level value.For the variation in glucose level generation we can use the result of different health surveys glucose level data and generate the glucose levels based on their statistics with probability assigned to each health survey data

###### [ V ]
**[ 5 ]**
**Blood pressure**-Blood pressure (BP) is the pressure exerted by circulating blood upon the walls of blood vessels.It is usually expressed in terms of the systolic (maximum) pressure over diastolic (minimum) pressure and is measured in mm (Hg).
* **(Dependency)**-Blood Pressure(Continuous) depends on Age(Continuous) and then on  Sex(Continuous).Systolic blood pressure rises steeply with the age.while diastolic blood pressure rises until the age of [45-54] for men and [55-64] for the women,after which they decline.At younger age blood pressure are higher for men then women,and at older stage this is reversed.Using the Distribution(% of the specified Age-Interval vs  bp values) data of the systolic and diastolic blood pressure of adults,by age and sex,Australia we will create systolic and diastolic bp for different age interval ,sex and use this lookup file to generate Blood Pressure.
* **(Error and variation)**-Real world data error in Blood Pressure Measurement are due:
a)Standard errors in Estimation of bp b)Incorrect Position of Patient Body c)Wrong size
Cuff used d) Cuff placed incorrectly.    
 Using the relative standard errors of estimate health survey data for different age interval vs different systolic and diastolic interval we can  generate the corrupted systolic and diastolic bp.
With the incorrect position of the Patient body we get 1.86 mm(hg) measurement errors
While incorrect placement of the cuff result in 10 mm(hg) difference between the right and left arm measurement,whereas incorrect position of cuff result in variation of systolic and diastolic values with (2-8mm) rise or drop.
Based on the Probability of the above errors we will generate the corrupted blood pressure
 
###### [ VI ]
**[ 6 ]**
**Visual Acuity**-clarity of the visions.
* **(Dependency)**-Visual acuity (Categorical attribute) depends on the Age(Continuous) and the Sex(Continuous).The decline of acuity with age is clearly evident in the survey data for both men and women.The proportion with at least normal vision starts dropping rapidly after 45 years of age.The distance vision  rapidly falls from (70-80 %)under 45 years to(below 10 %) above 65 years.Using the percentage distribution level of adults reaching specified acuity level for the  distance vision by age and sex we can generate the vision acuity for different age interval with their percentage acuity for the interval and use this a lookup file.
* **(Error and variation)** - a) Sampling and Measurement errors
Using the relative standard errors survey data we can generate the visual acuity with slight variation

###### [ VII ]
**[ 7 ]**
**Heart Diseases**
* **(Dependency)**-heart diseases depends on Age, Sex, chest pain,blood pressure,high glucose level,resting electrocardiographic(ECG) results,maximum heart rate,general cardiac enlargement
Heart Diseases is further classified based on the age ,sex plus above value as
a)Hypertensive heart diseases- Hypertension plus left bundle block by ecg or gce and high glucose
b)Coronary heart diseases-ecg results or chest pain,high glucose level
c)other heart diseases
Heart diseases were more in women compared to men. heart diseases rose sharply with the age for both men and the women. Based on the health survey distribution data - percentage of people suffering from different heart diseases vs the age interval we would generate the type of heart diseases the person is suffering from.
* **error and variation-** a) Sampling and measurement error b)error in the dependency attributes like error in ECG,blood pressure etc
Using the standard errors of estimate health survey data percentage of people suffering from different heart diseases vs the age interval we could corrupt the heart diseases.
Based on the error in the dependency attribute there may be chance to generate different heart diseases type indeed the one required to be generated.

###### [ VIII ]
**[ 8 ]**
**Hiv-1 Protease cleavage**- HIV-1 protease is a retroviral aspartyl protease (retropepsin) that is essential for the life-cycle of HIV, the retrovirus that causes AIDS.
* **(Dependency)**-It depends on a 8 letter octamer (Categorical attribute) of string type  and also depends on label(Categorical) which determine whether represents a site in a peptide (or protein) where the HIV-1 protease cleaves it (+1 if yes, -1 if no).
Octamer can be viewed as independent attribute of 8 character string from the allowed alphabet ‘ARNDCQEGHILKMFPSTWYV’ which represents the amino acid.
we can generate the cramer and  the cleavage level and use the UCI data to check HIV-1 protease cleavage.
* **Error and variation** -since hiv-1 protease cleavage depends on the cramer. And cramer can have Typographic Errors(Deletion ,Substitution,Transpose,Insertion),Keyboard errors,OCR, Phonetic which will result in variation in the HIV-1 protease cleavage depending on the presence of the corrupted cramer in the UCI datasets.

###### [ IX ]
**[ 9]**
**Indian Liver patients records-**
* **(Dependency)-** It depends on the age, gender,Total Bilirubin,Direct Bilirubin,Alkaline Phosphatase,Alanine Aminotransferase,Aspartate Aminotransferase,Total Proteins,Albumin,Albumin and Globulin Ratio,Selector field.
Patient record will be generated by clustering the patient record UCI data sets based on the age and then gender and generating any random patient records based on his age and gender from the clustered UCI data sets.
* **(Error and variation)-** UCI datasets may result in no record with particular age and sex value resulting in Missing value parameter in liver patient record. The Clustered UCI data sets may result in huge records with particular age and patient records which will result in generation of many patients records hence result in variation of the liver records

###### [ X ]
**[ 10 ]**
**Liver Disorder**- Liver disorder data focus mainly on hepatitis and cirrhosis. Liver disorder happen due to excessive alcohol consumption.
* **(Dependency)-** It depends 5 blood tests which are thought to be sensitive to liver disorders that might arise from excessive alcohol consumption and also depends on number of half-pint equivalents of alcoholic beverage drunk per day and selector field.Based on the UCI data sets of the liver records we will generate Liver Disorder records.

###### [ XI ]
**[ 11 ]**
**Lung Cancer**-Depends on Age,Smoking Status,Sex,Pulmonary Diseases,Family History of Lung Cancer.
* **(Dependency)-**
* **(ERRORS)**

###### [ XII ]
**[ 12 ]**
**Arthritis** depends on Age ,Sex,Overweight,Joint Injuries,Industrial Group.

###### [ XIII ]
**[ 13 ]**
**Hepatitis** depends on Age,Sex,Steroids Antiviral,Fatigue,Malaise,Anorexia 

###### [ XIV ]
**[ 14 ]**
**Diabetes** depends on Age,Sex,Obesity,Blood Pressure,Cholesterol,Insulin. 


###### [ XX ]
**[ 20 ]**
**Refrences FOR ALL THE  MEDICAL DATA'S TO BE GENERATED **

[US STATISTICS AND RESEARCH PAPAER MOST IMPORTANT ](http://www.cdc.gov/nchs/products/series/series11.htm)

[AUSTRALIAN HEALTH SURVEY STATISTICS](http://www.abs.gov.au/australianhealthsurvey)

[NATIONAL HEALTH SURVEY STATISTIC](http://www.cdc.gov/nchs/nhis.htm)

[INDIAN HEALTH SURVEY STATISTICS](http://censusindia.gov.in/2011-common/AHSurvey.html)

[INDIAN OTHER HEALTH STATISTICS](http://www.mohfw.nic.in/index1.php?lang=1&level=1&sublinkid=1756&lid=1645)

[CANADIAN HEALTH SURVEY STATISTICS](http://www23.statcan.gc.ca/imdb/p2SV.pl?Function=getSurvey&SDDS=3225)

**[ 21 ]**
**INDIVISUAL REFRENCES FOR THE MEDICAL DATAS**

1. [BMI VS Height and Weight]

* 1.1 [bmi Australian Survey Statistics](http://www.abs.gov.au/ausstats/abs@.nsf/lookup/33C64022ABB5ECD5CA257B8200179437?opendocument)

* 1.2 [Bmi US Survey Statistics](http://www.cdc.gov/nchs/data/nhanes/databriefs/adultweight.pdf)

* 1.3 [Bmi EURPOES Survey Statistics](http://ec.europa.eu/eurostat/statistics-explained/index.php/Overweight_and_obesity_-_BMI_statistics)

2. [BMI VS Age and Sex Survey statistics]

* 2.1 [Hemoglobin Canada Survey Statistics](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC1946575/?page=1)

