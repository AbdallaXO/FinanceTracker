Finance Tracker - Python Application
This is a Python application for managing your finances. It allows you to record transactions, view them within a date range, and visualize income and expenses over time.

Features
Add new transactions with date, amount, category, and description.
View transactions and summary (total income, expense, and net savings) within a specified date range.
Generate a plot showing income and expense trends over time.
Requirements
Python 3.x
pandas
csv
datetime
matplotlib.pyplot (optional for plotting)
tkinter (optional for user interface in future development)
Usage
Clone this repository or download the files.
Install the required libraries:
Bash

pip install pandas csv datetime matplotlib.pyplot tkinter (if desired)
Run the application:
Bash

python main.py
How it works
The application utilizes the CSV class to manage the transaction data stored in a CSV file (finance_data.csv). You can add new transactions using the add function and view past transactions within a date range using the get_transactions function.

The plot_transactions function (requires matplotlib.pyplot) visualizes your income and expense trends over time.

The main function provides an interactive menu where you can choose to add a new transaction, view past transactions, or exit the program.

