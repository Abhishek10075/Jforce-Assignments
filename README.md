# Jforce-Assignments
This repository contains my solutions for the JForce recruitment tasks. The projects demonstrate my expertise in handling complex data structures and building high-performance NLP models.

JForce AI & Data Engineering Assignments
This repository contains my solutions for the JForce recruitment tasks. The projects demonstrate my expertise in handling complex data structures and building high-performance NLP models.

Project 1: Student Attempt Tracking (Data Engineering)
Task: Create a summary table for students who have attempted the same subject multiple times, keeping only the latest 3 marks.

Logic & Approach:

Date Sorting: First, I converted the 'Date' column to a datetime object and sorted the records so that the most recent attempts appear first.

Grouping & Ranking: Used groupby on 'Roll No' and 'Subject' combined with cumcount() to rank each attempt (0 = Latest, 1 = Second Latest, 2 = Third Latest).

Data Pivoting: I filtered for the top 3 attempts and transformed the rows into columns (M1, M2, M3).

Missing Values: Handled cases where a student had fewer than 3 attempts by filling the remaining columns with 0, as per the requirement.

Tech Stack: Python, Pandas.

Project 2: Consumer Complaint Classifier (NLP)
Task: Build an AI model to predict 'Product' and 'Sub-Product' categories from customer complaint text ("Issue" and "Sub-Issue").

Logic & Approach:

Text Preprocessing: Built a pipeline for noise removal, tokenization, and Lemmatization to ensure the model focuses on the root meaning of words.

Advanced Vectorization: Implemented TF-IDF with N-grams (n=5). By using 5-grams, the model can understand long phrases (e.g., "unauthorized transactions on my card") instead of just single words.

Model Selection: Used a Multi-Output XGBoost Classifier. This allows the system to predict both the Product and Sub-Product simultaneously using a single efficient model.

Results:

Product Accuracy: 99%.

Sub-Product Accuracy: Optimized through N-gram context.

Tech Stack: XGBoost, Scikit-learn, NLTK, Matplotlib.
