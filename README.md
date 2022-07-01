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
  
   - Regarding the comparison of scores by grade, we can see that the removal of the THS ninth grade scores does not have an affect on any of the other grades both within and outside of THS. The are no values for the ninth graders at THS, so we can see that the line has been replaced with the null (i.e. NaN).
   - In all the other areas, we again do not see any significant changes in the output. After adjusting the student count to only account for THS' 10th-12th graders, we dont see much change in their Overall Passing percentage. This in turn leaves these other categores realtively unaffected. 
    - For clarification, the highlighted areas in the images are to show the bins in which THS fell. We do not see any changes between the intial and adjusted results that would indicate that the THS students scores affects the overall analysis in this case.

## Summary
Overall, we see a slight decrease in all of the values for THS' performance after we removed the compromised ninth grade scores. This could indicated that the compromised scores acted to artificially inflate Thomas High School's overall standing in the district. However, it is difficult to draw any conclusion regarding THS' standing as we do not have any values to give as accurate representation of the ninth grade class' ability. By taking out the scores, it would be unfair to count each students score as 0 or failing, this drops THS down significantly in standing amongst the other schools in the district (from 90% to 65% overall passing). 

In the distict analysis, we see that factoring out THS ninth grade scores also has a lowering effect for the entire district - dropping the overall passing percentage from 65% to 64.9%. Again we cannot properly account for the significance as we do not have a method to accurately guage THS ninth graders true performance. That being said, it could be reasoned that with the change being so small, it could be considered nominal.

We do not see a differrence in the results when comparing between the inital and adjust analysis for School Size, School Type, or Spending Range. This could mean that the THS ninth grade scores do not have a significant affect in these areas.

Lastly, in comparison by grade, the biggest caveat we see is that therea are no scores for us to compare THS' ninth graders to the other schools' ninth graders. Because of this, it is difficult to guage whether they are performing well or not and the school board would be unable to make decisions for their education plan in that regaurd.

Ultimately, we conclude that the THS ninth grade scores have a slight, if not nominal, effect on the overall analysis. 

An interesting point to note: in looking at the comparisons based on School Size, we see that smaller schools have the the highest passing percentages. In the School types, we see that Charter schools have the higher passing percentages. And finally, we see that schools with lower spending per student have the higher passing percentages.
