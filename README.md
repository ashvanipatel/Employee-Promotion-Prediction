1️⃣ Project Introduction 

My project is Employee Promotion Prediction using Machine Learning in PySpark.
The goal is to help HR identify which employees are likely to get promoted based on their past records, performance, experience, and training data.

Dataset used: employee_promotion.csv
Rows: 51,800 employees
Columns: 14 attributes

2️⃣ Objective of the Project

You can speak:

The objective of my project is to analyze employee data, identify key factors influencing promotion, and build a Random Forest model that predicts whether an employee should be promoted. Additionally, I created an interactive Power BI dashboard that shows employee distribution and promotion insights.

3️⃣ Steps I Followed 
🔹 Step 1: Data Loading & Inspection

I loaded the dataset using PySpark and checked:

Shape of the data

Column types

Missing values

Basic overview of the dataset

🔹 Step 2: Handling Missing Values

I fixed missing values in two ways:

Numeric columns → replaced using mean

Categorical columns → replaced with "Unknown"

🔹 Step 3: Encoding Categorical Columns

Spark ML requires number inputs only.

So I used:

StringIndexer

OneHotEncoder

To convert department, gender, region, etc. into numeric vectors.

🔹 Step 4: Feature Engineering

I combined all features using:

VectorAssembler → features column

🔹 Step 5: Model Selection

I used:

✔ Random Forest Classifier

Because:

It works well with mixed data

Handles categorical variables

Good accuracy

Resistant to overfitting

Parameters used:

100 Trees

Max Depth: 6

Seed: 42

🔹 Step 6: Train-Test Split

80% Training

20% Testing

🔹 Step 7: Model Training

Pipeline:

Indexer → OneHotEncoder → Assembler → RandomForest


This makes the process automated and efficient.

🔹 Step 8: Evaluation

I checked:

Accuracy

F1-Score

Results:

Accuracy ≈ 87%

F1 Score Good (Balanced despite imbalance)

This shows the model works well.

🔹 Step 9: Export Predictions for Power BI

I saved predictions as:

hr_predictions.csv


Then imported into Power BI for visualization.

4️⃣ Power BI Dashboard Explanation 
Dashboard 1: Employee Data Summary
<img width="865" height="486" alt="Screenshot 2025-11-14 132027" src="https://github.com/user-attachments/assets/555964d0-f8fc-466e-be59-6952d79b020e" />




Explain each element:

✔ Card 1 — Total Employees

→ Shows total 11.05K employees.

✔ Card 2 — Total Promotions

→ Shows total 4668 employees promoted.

✔ Card 3 — Model Accuracy

→ 87% accuracy from Random Forest.

✔ Card 4 — Promotion Rate

→ 8.52% overall.

Pie Chart — Employee Distribution by Department

Explain that this shows which department has more employees.

Pie Chart — Education Level Distribution

Shows employees’ qualification distribution.

Bar Chart — Promotion Rate by Department

Shows which department has higher promotion counts.

Table

Shows:

department

education

employee count

promoted count

Good for final HR insights.

5️⃣ Dashboard 2: Employee Demographics Page
<img width="864" height="488" alt="Screenshot 2025-11-13 202302" src="https://github.com/user-attachments/assets/c11a1864-70d0-4db7-8134-ea744bd957f9" />


Explain:

✔ Age Distribution

Majority employees are between 25–45.

✔ Length of Service Distribution

Most employees have 2–12 years of service.

✔ Gender Distribution

Pie chart:

70% male

30% female

✔ Performance Rating Distribution

→ Rating 3 and 5 have high counts.

✔ Region Distribution

→ Region_2, Region_7, Region_13 have highest numbers.

6️⃣ What Insights I Gave to HR 

Promotion rate is very low → only 8.52%.

Experience, performance rating, and training score strongly affect promotion.

Some departments like Sales & Marketing have more employees but fewer promotions.

Education level does not strongly impact promotion .

Region-wise distribution is highly imbalanced.

7️⃣ What I Learned 

You can say:

How to clean and preprocess real-world HR data

How to build machine learning pipelines in PySpark

How to evaluate ML models

How to create interactive dashboards in Power BI

How data-driven decisions help HR improve fairness and efficiency

8️⃣ Final Statement 

In summary, my project successfully combines big data processing in Spark, machine learning using Random Forest, and business insights using Power BI. This end-to-end system can help HR make data-driven promotion decisions.
