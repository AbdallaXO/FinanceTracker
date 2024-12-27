# Finance Tracker Application

## Overview
This is a simple command-line application for managing and visualizing personal financial transactions. The application allows users to add transactions, view transactions within a specified date range, and generate plots of income and expenses over time.

---

## Features
- **Add Transactions**: Record the date, amount, category, and description of financial transactions.
- **View Transactions**: Display a summary of income, expenses, and net savings for a given date range.
- **Plot Transactions**: Generate a visual representation of income and expenses over time.

---

## Requirements
The application requires the following:

- **Python 3.x**
- Required Python libraries:
  - `pandas`
  - `matplotlib`
  - `tkinter`

You can install the required libraries with the following command:
```bash
pip install pandas matplotlib
```

---

## File Structure
- `main.py`: Main script to run the application.
- `finance_data.csv`: CSV file to store financial transactions (automatically created if not found).
- `data_entry.py`: A helper module to handle user input for dates, amounts, categories, and descriptions.

---

## Usage
### 1. Clone the Repository
```bash
git clone <repository_url>
cd <repository_directory>
```

### 2. Run the Application
Run the following command in your terminal or command prompt:
```bash
python main.py
```

### 3. Main Menu Options
- **Option 1: Add a New Transaction**
  - Enter the transaction details (date, amount, category, description).
- **Option 2: View Transactions and Summary**
  - Specify a start and end date to view transactions.
  - A summary of total income, expenses, and net savings will be displayed.
  - Optionally, view a plot of income and expenses over time.
- **Option 3: Exit**
  - Exit the application.

---

## Example Interaction
```plaintext
1. Add a new transaction
2. View transaction and summary within a date range
3. Exit
Enter your choice (1-3): 1

Enter the date of the transaction (MM-DD-YYYY) or enter for today's date: 12-26-2024
Enter the amount: 1500
Enter the category (Income/Expense): Income
Enter a description: Freelance Payment
Entry added successfully.

1. Add a new transaction
2. View transaction and summary within a date range
3. Exit
Enter your choice (1-3): 2

Enter the start date (MM-DD-YYYY): 12-01-2024
Enter the end date (MM-DD-YYYY): 12-31-2024
Transactions From 12-01-2024 to 12-31-2024:

    date       amount category         description
12-26-2024   1500.00   Income   Freelance Payment

Summary:
Total Income: $1500.00
Total Expense: $0.00
Net Savings: $1500.00

Do you want to see a plot? (y/n): y
(Plot window appears)
```

---

## CSV File Details
The application saves all transactions in `finance_data.csv` with the following columns:
- **`date`**: The date of the transaction (format: MM-DD-YYYY).
- **`amount`**: The transaction amount.
- **`category`**: The type of transaction (`Income` or `Expense`).
- **`description`**: A brief description of the transaction.

---

## Plotting
When plotting is enabled, the application generates a line graph displaying:
- **Income**: Daily income plotted as a green line.
- **Expenses**: Daily expenses plotted as a red line.

---

## Troubleshooting
### Common Issues
1. **TclError: Can't find a usable init.tcl**
   - Ensure you have Tcl/Tk installed with your Python distribution.
   - Add `TCL_LIBRARY` and `TK_LIBRARY` environment variables pointing to the respective directories.

2. **Matplotlib backend errors**
   - Use a non-interactive backend for plotting by adding this line before importing `matplotlib.pyplot`:
     ```python
     import matplotlib
     matplotlib.use('Agg')
     ```

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes.

