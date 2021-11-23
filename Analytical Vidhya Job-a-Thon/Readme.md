# JOB-A-THON PROJECT ANALYSIS REPORT(19-11-2021 to 21-11-2021)

## Problem statement
				    The given problem is to found whether the employee will leave the company or not. As the employee are leaving the salary to the Human resources (HR) is increasing. We need to predict will the employee will be in the company or not based on the factors given in the problem statement and the given data set.
				    
## Approach
•	The target variable is not given in the data set. So, based on the LastWorkingDate, I have decoded the Target variable 
i.e., If the employee doesn’t have last working date, the employee is still working, else the employee left. 
•	Based on that, I created target variable. 1(If the employee left), 0(If the employee is still working)

	Exploratory Data Analysis
		•	There are more number of male employees than female.
		•	The average salary of Female employees is more than that of Male
		•	Majority of the Employees with salary less than 75,000 left the company
		•	Employees from the city c5 have more salary
		•	There are more Employees with Bachelor’s Degree
		•	Majority of the employees with the Master degree whose salary is less than 60,000 left the company.
		•	The employees with the Master degree have the more salary
		•	The employees with joining designation '1' are more
		•	The average salary of employees with the joining designation 5 is more




## Data Pre-Processing
•	Label Encoding: - As there are categorical columns, I have converted them into numerical as the Machine Learning algorithm doesn’t take input categorical columns.
•	SMOTE: - There is an imbalance in the target variable between 1 & 0. So, I have performed SMOTE to balance the target variable.
•	Scaling: - There is a difference in the values of the independent variables. To bring them into a measurable scale, StandardScaler is used.
•	GroupBy: - Since there are multiple records for each Employee ID, Grouping is performed by combining the matching records and taking the average of the Total_Business_Value.
•	Cleaning: - I have removed Employee_Id, joining date, from the training data as they do not contribute in predicting the attrition of the Employee.

## Conclusion:
	Among all the models used to predict the Employee Attrition (Random Forest, Logistic Regression, Decision Tree, Grid Search, Support Vector Machine, AdaBoost). Support Vector Machine shown accuracy of 81% and when submitted in portal it gave an accuracy of 72%. 
	So, using Support Vector Machine Model is the best approach in predicting the attrition of an Employee.
