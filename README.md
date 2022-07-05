# Big_Data

## T-Tests on Suspension Coils

Argument to show the PSI for each manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch.The results of the 3 different lots as detailed and show below:
Manufacturing Date for Lot 1
The results are not equal to 1500 which is the true value as it yielded  (1499.719 1500.281) as displayed
in this example (t = 0, df = 49, p-value = 1).

Manufacturing Data for Lot 2
The results are not equal to 1500 which is the true value as it yielded (1492.431 1499.849) as displayed
t = 0.51745, df = 49, p-value = 0.6072


Manufacturing Data for Lot 3 
The results are not equal to 1500 which is the true value as it yielded (1492.431 1499.849) as displayed
in this example (t = -2.0916, df = 49, p-value = 0.04168)


> # t-test for all lots
> t.test((Coil_Data$PSI),mu = 1500)

	One Sample t-test

data:  (Coil_Data$PSI)
t = -1.8931, df = 149, p-value = 0.06028
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1497.507 1500.053
sample estimates:
mean of x 
  1498.78 

> # t-test for each lot
> t.test(subset(Coil_Data,Manufacturing_Lot =="Lot1")$PSI,mu = 1500)

	One Sample t-test

data:  subset(Coil_Data, Manufacturing_Lot == "Lot1")$PSI
t = 0, df = 49, p-value = 1
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1499.719 1500.281
sample estimates:
mean of x 
     1500 

> t.test(subset(Coil_Data,Manufacturing_Lot =="Lot2")$PSI,mu = 1500)

	One Sample t-test

data:  subset(Coil_Data, Manufacturing_Lot == "Lot2")$PSI
t = 0.51745, df = 49, p-value = 0.6072
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1499.423 1500.977
sample estimates:
mean of x 
   1500.2 

> t.test(subset(Coil_Data,Manufacturing_Lot =="Lot3")$PSI,mu = 1500)

	One Sample t-test

data:  subset(Coil_Data, Manufacturing_Lot == "Lot3")$PSI
t = -2.0916, df = 49, p-value = 0.04168
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1492.431 1499.849
sample estimates:
mean of x 
  1496.14 
  
## Study Design: MechaCar vs Competitive

Test metrics give you the data you need to track and improve your test process as well as finding answers to questions like: How long did it take to release?  There are three categoroes of metrics:  product metrics, process metrics, and project metrics. The metrics would be of interest to a consumer especially to analyze: cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.  
for examle, in the case of highway, kilometers are used to measure long distances.  It will be useful to figure out the lenfth of a road, the distance between two locations, etc.  The Metrics sign conversion is the best sysytem to use.

What is the Null Hypothesis or Alternative Hypothesis:

The null hypothesis and alternative hypothesis are used in statistical hypothesis testing. The null hypothesis always predics no effect or no relationship between variables, while the alternative hypothesis states the research prediction oa an effect or relationship.

What statistical test would you use to test the Hypothesis?  And why?


What data is needed to run the statistical tests?
A t-test is used as a hyoothesis testing tool, which allows testing of an assumption applicable to a population.  A t-test looks at the t-statistic, the t-distribution values, and the degrees of freedom to determine the statistical significance.


What data is needed to run the statistical test?
For a statistical test to be valid, your sample size needs to be large enough to approximate the true distribution of the population being studied.  You will need to know your data meets certain assumptions and the type of variable you are dealing with. 

