# School_District_Analysis
Utilizing Python Pandas to analyze data
## Overview: Background and Purpose
### Background
In this analysis, we are working alongside Maria - data scientist for city school district - to prepare a report of analysis on standardized testing data to adress performance patterns among the students and find any trends with relation to funding. While building this report, evidence of academic dishonesty was found in relation to the the Thomas High School's ningth graders reading and math scores.
### Purpose
The goal of this analysis is to identify whether the omission of the Thomas High School ninth grade scores has an effect on the overall analysis. 

## Results
How is the district summary affected?
---
- First let us look at the result of the initial district analysis:

![Initial distric analysis results](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/district_analysis_df_init.PNG?raw=true)
  
- Now, we can compare these results the the table that we get after changingthe data to reflect the THS (Thomas High School) ninth grade test score ommission:
  
![District analysis after THS ommission](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/district_analysis_df_post.PNG?raw=true)

- We see that in both the averages of the test scores in both subjects, and in the passing passing percentages of both subjecs and overall that taking out the compromised scores has decreased these values. However, at this level of the analysis, the change is very slight - we see between a 0.1 and 0.3 value difference. 
   
How is the school summary affected?
-
- Like above, we will look first at the initial analysis before removing the compromised data - spicifally at the row for THS:

![Initial School Summary Unadjusted](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/school_analysis_df_init.PNG?raw=true)

- Next we look at the results post-ommitting compromised data:

![School summary after ommission unadjusted](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/school_analysis_df_unadjusted.PNG?raw=true)

- Here we can see a stark difference in the passing percentages - specifically in the overall passing percentage we see a jump from 90.9% to 65.1%. However we have to acknowledge that this data reflects all of the students being accounted for while the pportion that are the ninth grade class are null values. we went further to calculate the averages and passing percentages using only the 10th-12th grade class data and adjusted the total number of students for THS to reflect this as well and got the following outcome:

![School summary after adjustment](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/school_analysis_df_post.PNG?raw=true)

- In this data, we see a much higher over all percentage, but when compared to the initial analysis, we can note that the passing percentages and averages are lower.
  
How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
-
- Before adjusting for the number of students in THS (i.e. when looking at all the students and not just the 10th-12th graders) we saw that the ranking dropped from 2nd (with 90.9% overall) to 8th (with 65.1% overall). However, after adjustment we note that THS' ranking remains in the 2nd spot.

Top 5 Schools: Initial     |  Top 5 Schools: After adjusting for THS 
:-------------------------:|:---------------------------------------:
![](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/top_schools_init.PNG?raw=true) | ![](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/top_schools_post.PNG?raw=true)

How does replacing the ninth-grade scores affect the following:
-
  - Math and reading scores by grade

Math Scores by Grade (initial) | Math Scores by Grade (adjusted)
:-----------------------------:|:--------------------------------:
![](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/math_scores_grade_init.PNG?raw=true) | ![](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/math_scores_grade_post.PNG?raw=true)

Reading Scores by Grade (initial) | Reading Scores by Grade (adjusted)
:-----------------------------:|:--------------------------------:
![](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/reading_scores_grade_init.PNG?raw=true) | ![](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/reading_scores_grade_post.PNG?raw=true)

  - Scores by school spending

Performance Across Spending Ranges (initial)    |   Performance Across Spending Ranges (ajusted)
:----------------------------------------------:|:-----------------------------------------------:
![](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/spending_init.PNG?raw=true) | ![](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/spending_post.PNG?raw=true)


  - Scores by school size
 
 Performance Across School Size (initial)       |      Performance Across School Size (adjusted)
 :---------------------------------------------:|:------------------------------------------------:
 ![](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/size_init.PNG?raw=true) | ![](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/size_post.PNG?raw=true)
 
 
  - Scores by school type


  Perfomance Amongst School Types (initial)      |      Perfomance Amongst School Types (adjusted)
  :---------------------------------------------:|:-----------------------------------------------:
  ![](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/type_init.PNG?raw=true) | ![](https://github.com/chichi-ugo/School_District_Analysis/blob/main/Resources/images/type_post.PNG?raw=true)

## Summary
- [change 1]
- [change 2]
- [change 3]
- [change 4]
