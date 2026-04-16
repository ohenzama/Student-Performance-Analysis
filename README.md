# Student Performance Analysis


<h2>Tools Used</h2>
- <b>Excel:</b> Data Cleaning, EDA

<h2>Skills Highlighted</h2>
- <b>Inferential statistics (t-tests and ANOVA) </b>
<br />
- <b>Data Visualization </b>


<h2>Dataset and Description</h2>
<b>Source: </b> 
<b>Size: </b> [12470, 19]
<b>Description:</b> Two real datasets were merged and anonymized to create this dataset. Features include a number of student characteristics that might impact a student's academic perfomance. Each row represents a student. 
<b>Goal:</b> Determine which features hold a significant impact on the student's academic performance. 

<br />
<br />
<b>Key Features: </b>

- StudyHours – Number of study hours per week.
- Attendance – Percentage of classes attended.
- Resources – Availability and use of academic resources (e.g., library, notes).
- Extracurricular – Participation in extracurricular activities (Yes/No).
- Motivation – Self-reported motivation level (numeric scale).
Internet – Access to the internet for study purposes (Yes/No).
Gender – Student’s gender (Male/Female).
Age – Age of student (18–30 years).
LearningStyle – Preferred learning style (e.g., Visual, Auditory, Kinesthetic, Reading/Writing).
OnlineCourses – Participation in online courses (Yes/No).
Discussions – Boolean. Whether or not a student engages in study group discussions or forums.
AssignmentCompletion – Rate of completing assignments on time (numeric scale).
ExamScore – Score obtained in the main exam.
EduTech – Usage of educational technology tools/platforms.
StressLevel – Self-reported stress level (numeric scale).
FinalGrade – Final course grade (target variable for prediction).

<br />
<br />


<h2>Data Cleaning and Pre-Processing</h2>
-Removed NA values
-Removed duplicate values
-Created a boolean column titled **College Age?** which returned 1 for students within college age and 0 otherwise
- Created pivot tables that, for each level of each categorical variable, computed average final grade. Then, for each categorical variable, the difference of average final grades between each level was computed. In order to reduce the number of statistical tests conducted, chose to only do tests on the top 5 variables that exhibited the greatest average difference within their levels. These variables turned out to be: **Learning Style, Discussions, Internet, Gender,** and **Edutech**.

<h2>Exploratory Data Analysis</h2>


<h2>Statistical Tests</h2>
Performed two-sided two-sample t-tests on the variables **Learning Style, Discussions, Internet, Gender,** and **Edutech** to test if there existed a significant difference in mean final grade. The only variable where the null hypothesis was rejected was the **Discussions** variable *(p < 9.32796580121045E-06)*

<h2>Results and Insights</h2>
The tests returned with only one significant group, with a p value of so and so. The others were not significant, with p values of so and so. So we conclude that the other groups aren't that significant in impacting test scores, and we should double down / focus on the significant feature 




<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
