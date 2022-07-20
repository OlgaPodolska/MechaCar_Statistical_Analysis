# MechaCar_Statistical_Analysis
R statistical study, multiple linear regression analysis and statistical difference t-tests

# Purpose

The purpose of that analysis is to review the production data for insights that may help the manufacturing team. 
R version 4.2.1
RStudio 2022.07.0 

# Results

## Linear Regression to Predict MPG
The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars. Results from analysis this data set:

** mpg = (6.267)vehicle_length + (0.0012)vehicle_weight + (0.0688)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD + (-104.0)**

![img1.png](/Images/img1.png) 

** Statistical Summary:**

* Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

The vehicle length and vehicle ground clearance have a significant impact on miles per gallon. Conversely, the vehicle weight, spoiler angle, and All Wheel Drive (AWD) have p-Values that indicate a random amount of variance on the MechaCar prototype.

* Is the slope of the linear model considered to be zero? 

The p-Value for this model is 5.35e-11, what is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis. It  indcates that the slope of this linear model is not zero.

* Does this linear model predict mpg of MechaCar prototypes effectively? 

From our regression model r-squared value is 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. That means this model does predict mpg of MechaCar prototypes effectively.

## Summary Statistics on Suspension Coils
The Suspension Coil dataset provided for the MechaCar contains the results of testing the weight capacities of multiple suspension coils from multiple production lots to determine consistency.

* The suspension coil’s PSI continuous variable across all manufacturing lots

![img2.png](/Images/img2.png) 

* The following PSI metrics for each lot: mean, median, variance, and standard deviation

![img3.png](/Images/img3.png) 

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. The current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually. 

* Created Visualizations for the Trip Analysis for all lots

![img4.png](/Images/img4.png) 

## T-Tests on Suspension Coils

I performed t-tests to determine if all manufacturing lots are statistically different from the population mean of 1,500 pounds per square inch.

![img5.png](/Images/img5.png) 

Here we can see the a p-Value is 0.06, which is higher than the common significance level of 0.05. It means there is not enough evidence to support rejecting the null hypothesis. In another words, the mean of all three manufacturing lots is statistically similar to the presumed population mean of 1500.

In addition I performed t-tests to determine if  each lot individually is statistically different from the population mean of 1,500 pounds per square inch.

![img6.png](/Images/img6.png) 

In the two from those tree lots our p-value is above our significance level. Therefore, we do not have sufficient evidence to reject the null hypothesis, and we would state that the two means are statistically similar.
However, in Lot 3 the p-Value is 0.04, which is lower than the common significance level of 0.05. Here we should reject the null hypothesis that this sample mean and the presumed population mean are not statistically different.

## Study Design: MechaCar vs Competition

* What metric or metrics are you going to test?

We should collect data for comparable models across all major manufacturers for past 3 years for metrics:

**Safety Rating** as Independent Variable
**MPG (Gasoline Efficiency)** as Independent Variable
**Engine Type (Electric, Hybrid, Gasoline)** as Independent Variable
**Current Price** as Dependent Variable

* What is the null hypothesis or alternative hypothesis?

**Null Hypothesis:** MechaCar is priced correctly based on its performance of key factors.
**Alternative Hypothesis:** MechaCar is not priced correctly based on performance of key factors.

* What statistical test would you use to test the hypothesis? 

A multiple linear regression would be used to determine the factors that have the highest correlation/predictability with the list selling price (dependent variable); which combination has the greatest impact on price. 

What data is needed to run the statistical test?

I need data that will be correct and represent the true real-world results. To limit type I error (reject the null hypothesis when it is actually true) I would decrease the P to 0.1 as mentioned above and in order to limit type 2 error (fail to reject the null hypothesis when it is actually false) I would add additional measurments such a Resale Value or Average Annual Cost of Ownership.