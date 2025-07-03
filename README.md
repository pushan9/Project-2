#Project Title: Task Manager with User Authentication & Expense Tracker

##Objective
To create a secure, user-specific system that allows individuals to:
•	Register/login with a unique username and password
•	Manage personal tasks: Add, view, complete, and delete
•	Log daily expenses with categories and descriptions
•	Track total spending against a monthly budget
•	Persist user data securely using CSV file handling
________________________________________
##User Authentication
•	Registration: 
o	User provides a username and password.
o	Passwords are hashed using SHA-256 before being saved in users.csv.
o	Duplicate usernames are not allowed.
•	Login: 
o	The entered username and hashed password are matched against stored records.
o	Only authenticated users gain access to their personal task and expense systems.
________________________________________
##Task Management Features
•	Each user's tasks are stored in a unique file: tasks_<username>.csv.
•	Tasks have the following structure: 
o	Task ID
o	Description
o	Status (Pending or Completed)
•	Users can: 
o	Add a new task
o	View all their tasks
o	Mark a task as completed by ID
o	Delete a task by ID
________________________________________
##Expense Tracker Features
•	Expenses are logged in: expenses_<username>.csv.
•	Each entry records: 
o	Date
o	Category (e.g., Food, Travel)
o	Amount
o	Description
•	Users can: 
o	Add a new expense
o	View all past expenses
o	Set and track a monthly budget 
	If spending exceeds the budget, a warning is shown
	If within budget, remaining balance is displayed
________________________________________
##Interactive Menu System
•	After login/registration, the user sees a Task Menu: 
o	Add Task
o	View Tasks
o	Complete Task
o	Delete Task
o	Go to Expense Tracker
o	Logout
•	In the Expense Tracker Menu, options include: 
o	Add Expense
o	View Expenses
o	Track Budget
o	Return to Task Menu
•	Data is continuously saved to user-specific CSV files, ensuring persistence.
________________________________________
##Files and Data Storage
File Name	Purpose
users.csv	Stores usernames and hashed passwords
tasks_<username>.csv	Stores each user's tasks
expenses_<username>.csv	Stores each user's expenses
________________________________________
##Technologies Used
•	Python (Standard Library) 
o	csv for reading/writing user data
o	hashlib for password security
o	os for file existence checks
•	Command-line interface (CLI)

