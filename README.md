Project Overview

The Study Weakness Analyzer is a Python-based utility created to help students move beyond "digital participation" and achieve true "digital literacy". Instead of using a generic schedule, this tool uses custom logic to prioritize subjects where performance is low and difficulty is high.
By turning raw academic data into an actionable roadmap, it addresses the gap between just using technology and using it to make responsible, informed decisions about learning.

Key Features: 
(1)Weighted Time Allocation: Automatically calculates a balanced 6-hour daily study plan based on current marks and subject difficulty.

(2)Weakness Identification: Manually identifies and flags "Weak" subjects (marks < 50) to ensure students focus on high-risk areas first.

(3)Improvement Prediction: Features a basic predictive logic that estimates potential score boosts 
based on the allocated study hours.

(4)Text-Based Visualization: Includes a built-in performance bar chart using ASCII characters ( ) to compare marks across subjects without needing external libraries.

(5)Zero-Dependency Design: Built entirely using core Python (lists, loops, and conditionals) to demonstrate fundamental logic building.

How It Works
Input: The user enters the number of subjects, current marks (out of 100), and a difficulty rating (1-5).
Analysis: The script calculates a "Study Gap" for each subject and normalizes the results into a 6-hour window.
Classification: Subjects are tagged as Strong, Average, or Weak based on the input scores.
Output: A detailed study plan is printed, showing exactly how many hours to spend on each subject per day.

Technical Implementation
Language: Python 3.x
Concepts Used: Dynamic list storage, score normalization algorithms, and conditional status mapping.
