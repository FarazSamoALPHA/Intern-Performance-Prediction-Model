# Intern-Performance-Prediction-Model
What is this project about?
This project uses Machine Learning to predict how well an intern will perform during their internship. Instead of waiting until the end to evaluate someone, this model can predict early whether an intern is likely to excel or struggle — based on their work habits and feedback.

Why did we build this?
In any organization, internship programs are important. But managers often struggle to identify which interns need extra support and which ones are naturally performing well. Manually tracking everyone is time-consuming. So we built an automated prediction system that does this job using data and machine learning.

What data did we use?
We used the following information about each intern:

Task Completion Rate — What percentage of assigned tasks did the intern finish?
Average Completion Time — How many hours did they take per task? Faster is better.
Feedback Rating — What rating did their manager give them? (Scale of 1 to 5)
Attendance Rate — How regularly did they show up? (In percentage)
Tasks Assigned vs Completed — How many tasks were given and how many were actually done?
Communication Score — How well did they communicate with the team?
Initiative Score — Did they take initiative or wait to be told everything?


What does the model do?
The model takes all of the above information and calculates a Performance Score for each intern. Based on this score, every intern is placed into one of three categories:
CategoryScoreMeaningExcellent75 and aboveThis intern is doing great and is likely to be a top performerAverage55 to 74This intern is doing okay but has room to improveNeeds ImprovementBelow 55This intern is struggling and needs extra guidance and support

Which Machine Learning model did we use and why?
We used Random Forest Regressor because:

It works very well with tabular data like ours
It does not overfit easily compared to a single Decision Tree
It tells us which features matter the most (Feature Importance)
It gives accurate predictions even when features have different scales


How did we measure if the model is good?
We used three standard evaluation metrics:

R2 Score — Tells us how well the model explains the data. Closer to 1.0 is better.
MAE (Mean Absolute Error) — On average, how far off are our predictions?
RMSE (Root Mean Squared Error) — Similar to MAE but penalizes big mistakes more heavily.

We also used 5-Fold Cross Validation to make sure our model performs consistently and is not just memorizing the training data.

What did we find out? (Feature Importance)
After training the model, we checked which factors affect intern performance the most. The results showed:

Feedback Rating from the manager is the most important factor
Task Completion Rate comes second
Attendance Rate also plays a significant role
Average Completion Time has a negative effect — slower interns score lower


What is the final output?
The model produces a list of all interns with:

Their predicted performance score
Their category (Excellent, Average, or Needs Improvement)
A chart showing Actual vs Predicted scores
A bar chart showing the distribution of categories
A list of the Top 5 and Bottom 5 interns

This helps managers take action early — either reward top performers or provide extra training to those who are struggling.

Summary in one line:

We built a Machine Learning model using Random Forest that analyzes intern work data and predicts their performance — helping organizations identify top talent and support struggling interns early.

