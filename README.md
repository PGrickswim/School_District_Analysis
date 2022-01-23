# School_District_Analysis

## Purpose 

PyCity Schools executed standardized testing of the students at all high schools. After an initial analysis of the scores in the test was completed, evidence of academic dishonesty within the 9th grade at Thomas High School was uncovered. The data was then refactored to remove the 9th grade results from Thomas High school, in order to produce analysis of the district at large without being affected by the scores impacted by academic dishonestly. The present report seeks to show differences between the original analysis and the final analysis, and describe how the 9th grade Thomas High School removals impacted the overall analysis.

## Results

### District Summary

The District Summary values are very slightly altered by removing the scores of 9th graders at Thomas High School. The overall passing percentage decreased from 65.2% of the district to 64.9% of the district. Average math and reading scores changed by much less that one percent, and the percent passing math and reading at the district level decreased by 0.2% and 0.1% respectively.

Note that the number of schools, students, and budget did not change with removal of the scores. This is because the students in 9th grade at Thomas High School still command budget, still go to school, and of course still exist.

- Original 

![Original Results](https://github.com/PGrickswim/School_District_Analysis/blob/main/Resources/OriginalDistrictSummary.png)
- Updated

![Updated Results](https://github.com/PGrickswim/School_District_Analysis/blob/main/Resources/UpdatedDistrictSummary.png)

### School Summary

Write up here

- Orginal

![Original Results](https://github.com/PGrickswim/School_District_Analysis/blob/main/Resources/OriginalSchoolSummary.png)
- Updated Results (9th Graders Included)

![Updated Results](https://github.com/PGrickswim/School_District_Analysis/blob/main/Resources/UpdatedSchoolSUmmary.png)
- Updated Results (10th through 12th Grade)

![Updated Results](https://github.com/PGrickswim/School_District_Analysis/blob/main/Resources/UpdatedSchoolWithout9th.png)

Taking a look at the statistics for Thomas High School, the data is very telling. The average math and reading scores with the overall students for 10th-12th grade is very similar to the average scores when 9th grade students passing was included; however, the percent passing math and reading is precipitously lower for the updated dataframe due to the scores for 9th graders not being included, but the denominator. 

Relative to the other schools, Thomas High School was originally the second highest school as far as passing percentage is concerned, and with the academically dishonest scores removed, Thomas High School drops to 65.1% passing overall, but this is with 9th graders including as "not passing". 

When 10th graders through 12th graders kept in the dataframe and the 9th graders removed completely, Thomas is actually still #2 of the 15 high schools assessed - see below.

- Top 5 Schools
![Top 5 Schools](https://github.com/PGrickswim/School_District_Analysis/blob/main/Resources/Top5Schools.png)

### Effect of replacing the Ninth Grade Scores

#### Math and Reading Scores by Grade
When the 9th grade scores at Thomas High School are removed, there is no impact to any of the remaining scores in math or reading for any other High School or Grade. The scores for Thomas High School simply read "nan" when the dataframes are produced. See below example, which shows the reading scores by grade.

- Reading Scores By Grade
![Reading Scores By Grade](https://github.com/PGrickswim/School_District_Analysis/blob/main/Resources/rsbg.png)

#### Spending Per Student
Because the removal of scores do not affect the number of students in any schools of the district nor do the affect the spending per school or district, there is no impact to spending per student as a result of these removals. Moreover, the change in the index of schools that spend $630-$644 (of which Thomas is a member) is so minute that there are no statistically significant changes in the overall data for this subset. See below.

- Spending Per Student Before 9th Grade Thomas High School Removals
![Orignal Spending](https://github.com/PGrickswim/School_District_Analysis/blob/main/Resources/SpendingPerStudentBefore.png)

- Spending Per Student After 9th Grade Thomas High School Removals
![Final Spending](https://github.com/PGrickswim/School_District_Analysis/blob/main/Resources/SpendingPerStudentAfter.png)

#### Scores By School Size
Similarly to the Spending changes for the impact of Thomas' removed scores, the difference in Scores by its school size category is also minute. While there is a slight change in the Medium (1000-2000) schools' scores and pass % due to this, it is so small that when scores are rounded to the nearest tenth and % Passing is rounded to the nearest percent, the difference is not visible.

- Scores by School Size, before 9th Grade Thomas High School Removals
![Orignal By School Size](https://github.com/PGrickswim/School_District_Analysis/blob/main/Resources/SchoolSizeBefore.png)

- Scores by School Size, After 9th Grade Thomas High School Removals
![Final By School Size](https://github.com/PGrickswim/School_District_Analysis/blob/main/Resources/SchoolSizeAfter.png)


#### Scores By School Type
As the distinction between Charter and District schools are an even broader one than the previous breakouts, it is no surprise that the removal of 9th Grade Thomas High School Scores again does not have an impact here, either. See below, where Thomas High School, which is a charter school, does not impact the averages overall when rounded to this level of precision.

- Scores by School Type, before 9th Grade Thomas High School Removals
![Orignal By School Type](https://github.com/PGrickswim/School_District_Analysis/blob/main/Resources/CDBefore.png)

- Scores by School Type, After 9th Grade Thomas High School Removals
![Final By School Type](https://github.com/PGrickswim/School_District_Analysis/blob/main/Resources/CDAfter.png)

## Summary

There are many changes in the updated school district analysis after reading and math scores for the ninth grade students at Thomas High school have been replaced with NaNs. While the changes below are substantial in a way, their exclusion does not impact the overall scores reportable at the district level in a material way. The most notable changes are:

- The number of students at Thomas High School with reportable scores changed from 1,635 to 1,174, as 461 ninth graders were removed.
- With 9th Graders removed, the average math score changed from 83.42 to 83.35, a decrease of 0.07.
- With 9th Graders removed, the average reading score changed from 83.85 to 83.90, an increase of 0.05.
- With 9th Graders removed, the % Passing Math decreased from 93.27% to 93.19%.
- With 9th Graders removed, the % Passing Reading decreased from 97.31% to 97.02%.
- With 9th Graders removed. the overall passing percentage at Thomas High School decrease from 90.95% to 90.63%.

The academic dishonesty at Thomas High School is an unfortunate situation. Thomas, a charter school in the PyCity School District, is one of the best performing schools. Removing the dishonestly obtained results damaged the district's performance much less than the reputational damage from dishonesty within the halls of Thomas High School has caused.
