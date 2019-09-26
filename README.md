# Project One - Examining SAT and ACT data

## Executive Summary

### Problem Statement

The SAT and ACT are two of the most commonly accepted standardised tests used in college applications. The general perception is that students would typically take either test (i.e. not both) if they intend to apply for college in the United States. Using data for both tests in 2017 and 2018, we want to investigate how the two tests and their components (e.g. Verbal/Reading, Math) are correlated such that we can use one variable to make inferences about another. We also want to pick out any trends and anomalies that might be present in the data, and understand the events that could explain these data points.

### How it was carried out
We started off with a provided set of data for the two tests in 2017, cleaned it up, then manually created an additional set of data points for 2018. Besides running quick Pandas functions (e.g. `describe`), we also visualised the features using different types of charts (histogram, scatterplot, boxplot) to look for interesting trends in our data and to explain them.

### Analysis
Broadly, we found out that participation rates in SAT and ACT are strongly negatively correlated (about -0.85). 

We also found that, with the exception of ACT 2017 Science scores, performance in one subject score is strongly positively correlated with performance in another subject in the same standardised test.

However, subject scores tend to be strongly negatively correlated between SAT and ACT.

Another discovery is that within these two years of data, high participation rates in a given test tends to damp down the test scores. 

We also found out from looking up real world info that many states that have extremely high participation rates tend to be so because of state-wide requirements for students to sit for either of the tests, such as in Colorado which mandated SAT. 


### Shortcomings
* The data timeframe is just two years, which is quite short-term, and likely to be heavily impacted by neaby events e.g. 2017 ruling in Colorado that makes SAT testing mandatory. A longer timeframe would likely smooth out sudden spikes/dips caused by major events.
* Although participation percentages are a good starting point, it will also be helpful to know actual number of test-takers for a given test in a given state. This will help us better assess and understand trends.  

### Recommendations
* Take a longer timeframe view for the analysis by working with at least 5 years of data.
* Make testing mandatory and free, and administer tests during school hours on school premises to provide more opportunities to more students to apply for college.
---
## Data Dictionary

|Feature|Type|Dataset|Description|Min|Max|
|---|---|---|---|---|---|
|**state**|*object*|SAT|The state that the SAT data is from|_n.a._|_n.a._|
|**sat_participation_2017**<br>**sat_participation_2018**|*float*|SAT|SAT participation rate (in percentage) for a given state in a given  year|0%|100%|
|**sat_ewr_2017<br>sat_ewr_2018**|*float*|SAT|Average score for Evidence-Based Reading and Writing for a given state in a given  year|200|800|
|**sat_math_2017<br>sat_math_2017**|*float*|SAT|Average score for Math for a given state in a given year|200|800|
|**sat_total_2017<br>sat_total_2018**|*float*|SAT|Average total score for a given state in a given year, computed using EWR and Math scores|400|1600|
|**act_participation_2017<br>act_participation_2018**|*float*|ACT|ACT participation rate (in percentage) for a given state in a given  year|0%|100%|
|**act_english_2017<br>act_english_2017**|*float*|ACT|Average score for English for a given state in a given year|1|36|
|**act_math_2017<br>act_math_2018**|*float*|ACT|Average score for Math for a given state in a given year|1|36|
|**act_reading_2017<br>act_reading_2018**|*float*|ACT|Average score for Reading for a given state in a given year|1|36|
|**act_science_2017<br>act_science_2018**|*float*|ACT|Average score for Science for a given state in a given year|1|36|
|**act_composite_2017<br>act_composite_2018**|*float*|ACT|ACT Composite score for a given state in a given year|1|36|




