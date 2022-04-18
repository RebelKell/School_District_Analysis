# School_District_Analysis

## Overview
We were hired to assist Maria in analyzing the performanuce of her local school district by combing through the distrcit data, including school and student level data. 

First thing we did was review and clean the data to ensure that the dataset we were working with would give us an output we could be confident in. 

In our first analysis we provided an overview of each school with a focus on the math and reading scores as an indicator of school success and compared that to school type, size, and spending and provided it to Maria and her team. 

However, after this first report was submitted the school board notified Maria that the data file showed evidence of academic dishonesty within the 9th graders at Thomas High School and they asked us to further clean the data removing these folks and re-run the analysis. 
<br>
<br>


## Results

Below are the results of the new analysis after we replaced Thomas High School's 9th graders math and reading scores with NaN values. 

### Impact on the District Summary
The overall impact on the disctrict was not significant, with passing math reading percentage dropping from 75 to 74.8 (a 0.27% decrease), while passing reading percentage dropped from 86 to 85.7 (a 0.35% decrease), and the overall passing percentage dropped from 65% to 64.9% (a 0.15% decrease). 

[District Summary DF Initial](School_District_Analysis/blob/main/Resources/District%20Summary%20DF%20Initial.png)

[District Summary DF Updated](School_District_Analysis/blob/main/Resources/District%20Summary%20DF%20Updated.png)

### Impact on the School Summary
The school summary also showed minimal change in performance with the largest change seen in *% Overall Passing* being only a 0.35% decrease.


### Impact on Thomas High Schools Performance Relative to Other Schools
Thomas' place in the top five performing school list does not change after removing the 9th graders scores - it remains the 2nd highest performing school in the district. However, the overall passing percentage does see a 0.35% decrease (from 90.94 to 90.63).


### Impact on Math and Reading Scores by Grade
The average math score dropped by 0.29% and the average reading score dropped by 0.10% across all grades - this doesn't represent a significant change within the 9th graders scores across the district.       


### Impact on Scores by School Spending
Thomas High School falls into the $631-645 school spending bin so the change in test scores will be seen within this cohort, not the other spending bins. The *% Overall Passing* for the $631-645 increased by 0.23% (from 62.9 to 63), but *% Passing Math* and *% Passing Reading* decreased by 0.66 and 0.46% respectively.

[Scores by Spend DF Initial](School_District_Analysis/blob/main/Resources/By%20Spending%20-%20Initial.png)

[Scores by Spend DF Updated](School_District_Analysis/blob/main/Resources/By%20Spending%20-%20Updated.png)

### Impact on Scores by School Size
Thomas High School falls into the medium-sizrd school bin and there was no change at all in the scores across the medium sized schools. We did not adjust Thomas High School total population when we removed the 9th grade scores, so they remain in the same categorization.


### Impact on Scores by School Type
There was no change at all in the scores across charter schools.

## Summary 

This updated school district analysis shows only small changes once the Thomas High School 9th graders scores are removed from the analysis and the scores are updated to reflect only the upperclassmen (10th, 11th and 12 graders), but below are four changes we did notice:

- Replacing the 9th grader scores with NaN and *not* updating the scores with just the upperclassmen would have a big impact on the results for Thomas High School with their overall passing percentage dropping from 90.95 to 65.08 - a 28.45% decrease, but because we adjusted for the removal of those scores by calculating scores based only on the upperclassmen population, the dropped by only 0.35%. 
- Had we simply removed the 9th grade scores and not adjusted the scores, Thomas would have dropped from the 2nd best performing school to 8th, but our adjust scored meant that their place in the top five performing schools was not impacted.
-  The biggest impact was seen in the passing math percentage in the scores by spending with a 0.66% decrease (from 73.5 to 73).
- The only increase we saw was within the scores by school spending, where the overall passing percentage increased by 0.23% (from 62.9 to 63).

 



