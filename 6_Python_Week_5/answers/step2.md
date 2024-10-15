# Function questions:
Have a go at the following questions, they get the further down you go.

## Exercises:
### 1. Calculate Annual Interest:
* Write a function annual_interest(amount, rate, years) that calculates the total interest earned over a number of years using simple interest.
```python
def annual_interest(principal, rate, years):
    return principal * rate * years / 100
```

### 2. Calculate Total Savings:
* Write a function total_funds(funds_list) that takes a list of funds and returns the total funds.
```python
def total_funds(funds):
    total = 0
    for fund in funds:
        total += fund
    return total
```

### 3. Calculate Total Investment:
* Write a function total_investment(investments_list) that takes a list of investment amounts and returns the total amount invested.
* Use the function you wrote in step 2 to help you
```python
def total_investment(investments_list):
    return total_funds(investments_list)
```

### 4. Check Budget Surplus:
* Write a function is_budget_surplus(income, expenses) that takes two lists: monthly incomes and monthly expenses, and returns True if the total income is greater than the total expenses, otherwise False.
* Use the function you wrote in exercise 2 to help you
```python
def is_budget_surplus(income, expenses):
    total_income = total_funds(income)
    total_expenses = total_funds(expenses)
    return total_income > total_expenses
```

### 5. Average Monthly Income:
* Write a function average_income(income_list) that takes a list of monthly incomes and returns the average monthly income.
* Use the function you wrote in exercise 2 to help you
```python
def average_income(income_list):
    total = total_funds(income_list)
    return total / len(income_list)
```

### 6. Count High Expenses:
* Write a function count_high_expenses(expenses_list, threshold) that takes a list of expenses and a threshold value, and returns the count of expenses that are higher than the threshold.
```python
def count_high_expenses(expenses_list, threshold):
    count = 0
    for expense in expenses_list:
        if expense > threshold:
            count += 1
    return count
```

### 7. Monthly Expense Tracker:
* Write a function expense_tracker(expenses_list) that takes a list of monthly expenses and returns a list of booleans indicating whether each month’s expenses were below $1000.
```python
def expense_tracker(expenses_list):
    tracker = []
    for expense in expenses_list:
        tracker.append(expense < 1000)
    return tracker
```

### 8. Find Maximum Expense:
* Write a function max_expense(expenses_list) that takes a list of expenses and returns the maximum expense.
```python
def max_expense(expenses_list):
    max_exp = expenses_list
    for expense in expenses_list:
        if expense > max_exp:
            max_exp = expense
    return max_exp
```

### 9. Categorize Transactions:
* Write a function categorize_transactions(transactions_list) that takes a list of transaction amounts and returns a list of strings categorizing each transaction as ‘Income’ or ‘Expense’ based on whether the amount is positive or negative.
```python
def categorize_transactions(transactions_list):
    categories = []
    for transaction in transactions_list:
        if transaction > 0:
            categories.append('Income')
        else:
            categories.append('Expense')
    return categories
```

### 10. Calculate Profit or Loss:
* Write a function profit_or_loss(buy_prices, sell_prices) that takes two lists: buy prices and sell prices of stocks, and returns a list of profits or losses for each stock.
* (Hint) Use the technique from last week to write a for loop using range and len
```python
def profit_or_loss(buy_prices, sell_prices):
    profits_losses = []
    for i in range(len(buy_prices)):
        profit_loss = sell_prices[i] - buy_prices[i]
        profits_losses.append(profit_loss)
    return profits_losses
```