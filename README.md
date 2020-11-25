# ACA-Medicaid-Study
#### This code uses data from BRFSS to study the effects of ACA Medicaid Expansion on self reported Health Outcomes.
#### Implemented the difference-in-difference econometrics technique in STATA for the hypothesis
#### 
The objective of my project was to study the effects of ACA medicaid expansion
on self reported health outcomes. The main purpose of ACA medicaid was to
provide affordable health insurance and to cover all adults with income below
138% FPL. ACA was proposed in 2010 and in 2012 it was made optional for states
to choose if they want to expand under it. Therefore in 2014, 27 states expanded
under ACA medicaid followed by 3 other in 2015 and 2 in 2016, making the total
states which expanded 32.
The data for this project was taken from BRFSS where data is stored by CDC by
conducting a monthly telephone survey. The reason for choosing BRFSS data was
a) it is a comprehensive data
b) it includes many outcome variables and
c) it is one among the first large scale health dataset to release the data from 2015
Therefore it helped me to examine the three calendar years after the ACA
medicaid expansion. For this study, I only included individuals between 25-64
years of age with annual income upto $30k. I used data from 2011 to 2017. My
approach was to start by compiling the data from different years into one table,
followed by cleaning it due to numerous inconsistent entries in the table. To point
out a couple of examples, BRFSS used different names for the same variable in
different years. Moreover, the variable values had codes for which dummies
needed to be created. I can go into more details for the cleaning part if you would
like, or shall I move forward with next steps.
For this study, my explanatory variables were a range of demographic, economic
and family structure variables like age, gender, years of education, number of
children etc. To account for the recovery rate of states from the 2009 financial
crisis, I included unemployment rate which I gathered from the BLS website.
Coming to the model, my dependent variables were:
(1) Self-reported overall health as very good or excellent
(2) The number of days in the past month that physical health was not good
(3) The number of days in the past month respondent was not in good mental health
(4) The number of days in the past month with health-related functional limitations 

I created another variable: medicaid expansion which was 1 for the 32 states that
expanded and 0 for others. I took 2014 as the reference year because it was the
year when the states expanded.
I applied diff-in-diff technique in which outcomes are observed for two groups
(control and treatment) for two time periods. One group is exposed to a treatment
in the second period but not in the first. In our case, treatment is the ACA medicaid
expansion, taking place in 2014 and the 32 states fell into the treatment group. The
other group is not exposed to treatment during either periods. In our case, the 18
states which did not expand fall into this category. This diff-in-diff technique
works on parallel trend assumption which means in the absence of treatment, there
would be no difference between treatment and control groups as both the groups
have parallel trend in the pre-treatment period. The average gain in the control
group is subtracted from the average gain in the treatment group. This removes
biases in the second period comparison between the groups due to permanent
differences between the groups and the biases due to comparison over time.
To test the equality of pre-expansion trends, I conducted and event study in which
I estimated regression by interacting the treatment group dummies with the year
dummies. I took 2013 as the reference year. My null hypothesis is that all pre-2014
interaction terms should be zero. However, the results indicated that we fail to
reject the null of equal trends.
From the diff in diff regression, I did not find any significant result for my
estimator except for statistically significant reduction of 0.06 days and 0.08 days
in poor mental health and health related functional limitations respectively. The
results obtained align with the literature available on this topic.
