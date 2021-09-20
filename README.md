# School District Analysis using Python

## Overview of Project

### Purpose

This is an analysis of student funding and student standardized test scores from the a variety of schools. We are given access to every students' math and reading test scores, as well as various information on the schools they attend. We aggregate the data to showcase trends and school performance. These insights are used to inform discussions and strategic decisions at the school and district level regarding the school budget and priorities. In addition, we are tasked to remove the reading and math grades for Thomas High School ninth graders and replace them with NaNs while keeping the rest of the data intact. We will discuss how this change will affect the results of our analysis.

## Results

### How is the district summary affected?

The distict summary changed slightly after the ninth graders from Thomas High School had their grades replaced with NaNs. Most of the averages and percent passing decreased slightly. There are 461 ninth graders from Thomas High School which represents 1.18% of the total number of students from all the schools (total number of students is 39,170). This explains why the change to the district summary was minimal.

- Average Math Score decreased from 79.0 to 78.9
- Average Reading Score was unchanged at 81.9
- % Passing Math decreased from 75 to 74.8
- % Passing Reading decreased from 86 to 85.7
- % Overall Passing decreased from 65 to 64.9

#### District Summary BEFORE

![district_summary_df_before.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/district_summary_df_before.png)

#### District Summary AFTER

![district_summary_df_after.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/district_summary_df_after.png)

### How is the school summary affected?

The data from Thomas High School is the only row that is affected by the change. All the other schools have the same school summary data since Thomas High School was the only school with a data change. (See the next question to see this in greater detail)

### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

When looking at the Average Math Score and Average Reading Score, you can see that these changed slightly. The new averages represent the average of math and reading scores of Thomas High School students without ninth graders included. 

You'll also see that the % Passing Math, % Passing Reading, and % Overall Passing drop significantly, because we define passing to be a grade equal to 70 or above. Therefore, NaNs count as a non-passing grade and sets all ninth graders to not passing. We correct this later to exclude ninth graders from the % passing calculations.

- Average Math Score decreased from 83.418349 to 83.350937
- Average Reading Score increased from 83.848930 to 83.894082
- % Passing Math decreased from 93.272171 to 66.911315
- % Passing Reading decreased from 97.308869 to 69.663609
- % Overall Passing decreased from 90.948012 to 65.076453

#### Per School Summary BEFORE

![per_school_summary_df_before.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/per_school_summary_df_before.png)

#### Per School Summary AFTER

![per_school_summary_df_after.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/per_school_summary_df_after.png)

As previously stated, we fixed the % passing scores to exclude ninth graders and corrected the values as you'll see below.

With this revisions here are the changes:
- % Passing Math decreased from 93.272171 to 93.185690	
- % Passing Reading decreased from 97.308869 to 97.018739
- % Overall Passing decreased from 90.948012 to 90.630324

#### Per School Summary AFTER with % passing fix

![per_school_summary_df_after_fix.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/per_school_summary_df_after_fix.png)

If we did not fix the % passing data, Thomas High School would have been misrepresented and would have fell out of the Top 5 Schools with overall passing grades. Since we fixed this, Thomas High school remained in the top 5 schools.

#### Top 5 Schools BEFORE

![top_schools_before.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/top_schools_before.png)

#### Top 5 Schools AFTER with % passing fix

![top_schools_after.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/top_schools_after.png)

### How does replacing the ninth-grade scores affect math and reading scores by grade?

The only changes made to the math and reading scores by grade is done to Thomas High School ninth graders. In the picture below, you'll see that for Thomas High School ninth graders had their math and reading scores replaced with NaNs.

#### Thomas High School Math Score BEFORE

![math_score_by_grade_before.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/math_score_by_grade_before.png)

#### Thomas High School Math Score AFTER

![math_score_by_grade_after.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/math_score_by_grade_after.png)

#### Thomas High School Reading Score BEFORE

![reading_score_by_grade_before.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/reading_score_by_grade_before.png)

#### Thomas High School Reading Score AFTER

![reading_score_by_grade_after.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/reading_score_by_grade_after.png)

### How does replacing the ninth-grade scores affect scores by school spending

Since Thomas High School's Per Student Budget is $638 it falls under the $630-644 range on our Spending Summary chart, so the changes will only affect this row. (Please note that when rounded to the nearest tenth, you'll see no change.)

- Average Math Score decreased from 78.518855 to 78.502002
- Average Reading Score increased from 81.624473 to 81.636261
- % Passing Math decreased from 73.484209 to 73.462589	
- % Passing Reading decreased from 84.391793 to 84.319261
- % Overall Passing decreased from 62.857656 to 62.778233

#### Spending Summary BEFORE

![spending_summary_df_before.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/spending_summary_df_before.png)

#### Spending Summary AFTER

![spending_summary_df_after.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/spending_summary_df_after.png)

### How does replacing the ninth-grade scores affect scores by school size

Since Thomas High School's Student Size is 1635 it falls under the 1000-2000 range on our School Size Summary chart, so the changes will only affect this row. (Please note that when rounded to the nearest tenth, you'll see no change.)

- Average Math Score decreased from 83.374684 to 83.361201
- Average Reading Score increased from 83.864438 to 83.873869
- % Passing Math decreased from 93.599695 to 93.582398	
- % Passing Reading decreased from 96.790680 to 96.732654
- % Overall Passing decreased from 90.621535 to 90.557997

#### School Size Summary BEFORE

![size_summary_df_before.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/size_summary_df_before.png)

#### School Size Summary AFTER

![size_summary_df_after.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/size_summary_df_after.png)

### How does replacing the ninth-grade scores affect scores by school type

Since Thomas High School's School Type is "Charter" it falls under the Charter Type on our School Type Summary chart, so the changes will only affect this row. (Please note that when rounded to the nearest tenth, you'll see no change.)

- Average Math Score decreased from 83.473852 to 83.465425
- Average Reading Score increased from 83.896421 to 83.902315
- % Passing Math decreased from 93.620830 to 93.610020	
- % Passing Reading decreased from 96.586489 to 96.550223
- % Overall Passing decreased from 90.432244 to 90.392533

#### School Type Summary BEFORE

![size_summary_df_before.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/size_summary_df_before.png)

#### School Type Summary AFTER

![size_summary_df_after.png](https://github.com/alexhuynh0530/School_District_Analysis/blob/main/Resources/size_summary_df_after.png)




#### Conclusion


## Summary


