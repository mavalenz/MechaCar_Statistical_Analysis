# MechaCar_Statistical_Analysis

## Overview
Help Jeremy who works for AutosRUs to review the production data for insights on the newest prototype *MechaCar* that may help the manufacturing team understand the production troubles faced. We will help Jeremy and the data analytics team do the following:
- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes.
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population.
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

## Linear Regression to Predict MPG:
1. No variables/coefficients provided a non-random amount of variance to the mpg values. 
![Linear_Regression](https://github.com/mavalenz/MechaCar_Statistical_Analysis/blob/main/Resources/Linear_Regression.PNG)

2. The slope is not zero because the p-value of 5.35e-11 is lower than the 0.05 statistical significance. Which provides strong evidence against the null hypothesis of slope = 0.
![Linear_Regression_Summary](https://github.com/mavalenz/MechaCar_Statistical_Analysis/blob/main/Resources/Linear_Regression_Summary.PNG)

3. We can say that the linear model predicts mpg of MechaCar prototypes effectively because the *r-squared value* is .7149, indicating about 71% of the variance has a strong association with mpg.

## Summary Statistics on Suspension Coils:
Per the *total_summary* dataframe below, we can confirm that the current manufacturing data meets the design specification as the variance of the supsension coils does not exceed 100, it is at 62.29.
![Total_Summary](https://github.com/mavalenz/MechaCar_Statistical_Analysis/blob/main/Resources/Total_Summary.PNG)

However, breaking down the manufactoring data by looking at the *lot_summary* we can confirm that Lot 3 exceeds the 100 pounds per square inch limitation. Per the below you see that tha variance of lot 3 was much higher at 170.28.
![Lot_Summary](https://github.com/mavalenz/MechaCar_Statistical_Analysis/blob/main/Resources/Lot_Summary.PNG)

## T-Tests on Suspension Coils:

**ALL Lots T-Test**
![T-Tests_All_Lots](https://github.com/mavalenz/MechaCar_Statistical_Analysis/blob/main/Resources/T-Tests_All_Lots.PNG)

In the t-test for all lots, we found that the p-value of 0.06 is higher than the assumed statistical significance of 0.05, which means the null hypothesis can be accepted as the results are not significant.

**Lot 1 T-Test**
![T-Tests_Lot1](https://github.com/mavalenz/MechaCar_Statistical_Analysis/blob/main/Resources/T-Tests_Lot1.PNG)

In the t-test for lot 1, we found that the p-value is a at 1. This indicates similar to the ALL lots t-test where it is higher than the statisical significance showing we accept the null hypothesis.

**Lot 2 T-Test**
![T-Tests_Lot2](https://github.com/mavalenz/MechaCar_Statistical_Analysis/blob/main/Resources/T-Tests_Lot2.PNG)

In the t-test for lot 2, we found that the p-value is at 0.6 which is also higher than the statistical significance and thus we accept the null hypothesis.

**Lot 3 T-Test**
![T-Tests_Lot3](https://github.com/mavalenz/MechaCar_Statistical_Analysis/blob/main/Resources/T-Tests_Lot3.PNG)

In the t-test for lot 3, we found that the p-value is at 0.04 which is lower than the statistical significance, meaning we reject the null hypothesis and accept the alternative.

## Study Design: MechaCar vs Competition:
For many consumers, a big component for selecting cars would be safety and reliability of the car.
- Metrics to test for to compare safetyness against competitors would be safety ratings.
- The **Null Hypothesis** would be - MechaCar's safety ratings have no difference to its competitors and the **Alternative Hypothesis** would be vice versa of safety ratings are different.
- To test my hypothesis I would perform a **T-Test** because it will help me determine if there is a significant difference between the means of competitors.
- Data needed to run the statistical test would be safety ratings across competitors, car model, year, etc.
