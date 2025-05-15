# Python_Project
 Python project idea for an Expense Tracker with Budget Monitoring, where users can track monthly expenses and get alerts if they are exceeding their budget.
budget = {"income": 0, "expenses": []}

# Add income
budget["income"] = float(input("Enter your total monthly income: "))

# Add expenses		
while True:
    item = input("Enter expense name (or 'done' to stop): ")
    if item.lower() == "done":
        break
    amount = float(input(f"Enter amount for {item}: "))
    budget["expenses"].append((item, amount))

# Calculate remaining balance
total_expense = sum(i[1] for i in budget["expenses"])
balance = budget["income"] - total_expense

# Display summary
print("\n--- Budget Summary ---")
print(f"Total Income: {budget['income']}")
print(f"Total Expenses: {total_expense}")
print(f"Remaining Balance: {balance}")
