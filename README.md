
## Dependencies between Medical data attributes modeled for each longitudinal Medical Data  

**[ 1 ]**
**BMI** -The body mass index, or **BMI**, is a calculation used to determine your level of body fat and used to Predict chronic Diseases Risks.The BMI is defined as the body Weight divided by the square of the body height, expressed in of kg/m2.
* **(Dependency)** BMI Depends on the Height / (Weight)2 . BMI is Continuous attribute which depends on the Continuous attributes Height and Continuous attribute Weight.
* **(Error and variation)**-In real world BMI index are estimated in Health Survey with the Measure Value of Height and Weight of the People, as every Measurement have some errors of the estimate so will have Height and Weight and indeed will have the BMI,which is Relative Standard Error of the Estimate for the BMI for different Height and Weight Intervals.This will be used to generate Corrupted BMI.For Variation We will plot the generated  BMI  vs the Height and Weight and compare the result with health survey reports of different years.

**[ 2 ]**
**Hemoglobin**-Hemoglobin is the protein molecule in red blood cells that carries oxygen from the lungs to the body's tissues and returns carbon dioxide from the tissues back to the lungs.
* **(Dependency)** Hemoglobin (Continuous) depends on the age(Continuous) and then on sex(Categorical). Hemoglobin values are relatively low among the youngest and oldest age groups.with the lowest found at age below 5. While Hemoglobin values are highest between the adulthood and 50 years for Men whereas trend for female is decreasing Hemoglobin with age from adulthood.Using the Distribution(% of the specified Age-Interval vs Hemoglobin ) data of the  adults,by age and sex we generate Hemoglobin.
*  **(Error and variation)** -in real world errors in Hemoglobin values are :
a)Error caused by personal technique(Inadequate Mixing Blood) b)errors in  Hemacytometry c)platelets counting errors d)Sampling and Measurement errors
Based on the Probability of the above errors we will generate the corrupted Hemoglobin


