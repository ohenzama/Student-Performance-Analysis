# Student Performance Analysis


<h2>Tools Used</h2>
<b>Excel:</b> Data Cleaning, Exploratory Data Analysis, Inferential statistics (t-tests and ANOVA)

<h2>Dataset and Description</h2>

[Source](https://www.kaggle.com/datasets/adilshamim8/student-performance-and-learning-style/data)

<b>Size: </b> [12470, 19]

<b>Description:</b> Two real datasets were merged and anonymized to create this dataset. Features include a number of student characteristics that might impact a student's academic perfomance. Each row represents a student. 

<b>Goal:</b> Determine which features hold a significant impact on the student's academic performance. 

<b>Features: </b>

- StudyHours – Number of study hours per week.
- Attendance – Percentage of classes attended.
- Resources – Availability and use of academic resources (e.g., library, notes).
- Extracurricular – Participation in extracurricular activities (Yes/No).
- Motivation – Self-reported motivation level (numeric scale).
- Internet – Access to the internet for study purposes (Yes/No).
- Gender – Student’s gender (Male/Female).
- Age – Age of student (18–30 years).
- LearningStyle – Preferred learning style (e.g., Visual, Auditory, Kinesthetic, Reading/Writing).
- OnlineCourses – Participation in online courses (Yes/No).
- Discussions – Boolean. Whether or not a student engages in study group discussions or forums.
- AssignmentCompletion – Rate of completing assignments on time (numeric scale).
- ExamScore – Score obtained in the main exam.
- EduTech – Usage of educational technology tools/platforms.
- StressLevel – Self-reported stress level (numeric scale).
- FinalGrade – Final course grade (target variable for prediction. 0=A, 1=B, 2=C, 3=D).


<h2>Data Cleaning and Pre-Processing</h2>
- Removed NA values

- Removed duplicate values

- Created a boolean column titled **College Age?** which returned 1 for students within college age and 0 otherwise

- Added ID column
  
- Created pivot tables that, for each level of each categorical variable, computed average final grade. Then, for each categorical variable, the difference of average final grades between each level was computed. In order to reduce the number of statistical tests conducted, chose to only do tests on the top 5 variables that exhibited the greatest average difference within their levels. These variables turned out to be: **Learning Style, Discussions, Internet, Gender,** and **Edutech**.

<h2>Exploratory Data Analysis</h2>


<img width="936" height="287" alt="Screenshot 2026-04-16 at 5 49 17 PM" src="https://github.com/user-attachments/assets/0678e006-70ee-4e94-9a6b-e85deb7eb41d" />

Explored final grade segmented by various numerical student behaviors, Min-Max standardized for comparison. A few notable observations is how final grade letter decreased with study hours, and how stress level increased with decresing final grade letter. 

<img width="749" height="452" alt="Screenshot 2026-04-16 at 5 49 40 PM" src="https://github.com/user-attachments/assets/17899060-7642-4397-8d95-7f34db9121bf" />

We explored the correlation between final grade letter and exam scores per age, Min-Max Standardizing the score in order to compare them in a line graph. 

We noticed that there’s a related trend between exam score and final grades per age group, as usually, they share either positive and negative trends per age group, with the exception of age 26.


<h2>Statistical Tests</h2>

<img width="767" height="407" alt="Screenshot 2026-04-16 at 5 48 31 PM" src="https://github.com/user-attachments/assets/b7318033-1703-4c7a-b5b8-f0d963a4e0e8" />

Performed one ANOVA and 4 two-sided two-sample t-tests on the variables **Learning Style, Discussions, Internet, Gender,** and **Edutech** to test if there existed a significant difference in mean final grade. The only variable where the null hypothesis was rejected was the **Discussions** variable *(p = 9.32796580121045E-06)*

<h2>Results and Insights</h2>
The tests returned with only one significant group, with a p value of 9.32796580121045E-06.
The others were not significant, meaning we didn't have enough evidence to reject the hypothesis that the mean final grades score within their respective levels were different. Thus, the test suggests that final exam scores don't significantly differ among students with different learning styles, genders, internet access, and educational technology preferences. However, whether or not a student engages in discussion is shown to have an impact on final exam scores. Thus, **one possible solution to improving final exam scores among students is to mandate productive study groups or discussions among the students.**

Note: We have limited insight on the overall relevance of these results, as these results might be due to the particular subject of the final exams, like English, which the scores were recorded from. The dataset source and description provides no information on the school subject(s) the scores were derived from. 




<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
