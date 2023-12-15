# Budget App

This is the boilerplate for the Budget App project. Instructions for building your project can be found at https://www.freecodecamp.org/learn/scientific-computing-with-python/scientific-computing-with-python-projects/budget-app

# My collaboration in the project:

# Budget App

This Python budget app consists of a `Category` class and a function called `create_spend_chart`. The `Category` class allows you to create budget categories like food, clothing, and entertainment. You can perform various operations such as depositing money, withdrawing money, checking the balance, transferring funds between categories, and checking if there are enough funds for a withdrawal or transfer.

## Category Class

### Methods

- **`__init__(self, category):`**: Constructor method that initializes a budget category with a given name.
  
- **`deposit(self, amount, description=""):`**: Adds a deposit entry to the ledger.

- **`withdraw(self, amount, description=""):`**: Adds a withdrawal entry to the ledger, returns True if successful, False otherwise.

- **`get_balance(self):`**: Returns the current balance of the budget category.

- **`transfer(self, amount, budget_category):`**: Transfers funds to another budget category, returns True if successful, False otherwise.

- **`check_funds(self, amount):`**: Checks if there are enough funds for a given amount, returns True if sufficient, False otherwise.

- **`__str__(self):`**: String representation of the budget category, including a title line, ledger items, and total.

## create_spend_chart Function

### Parameters

- **`categories:`** A list of `Category` objects.

### Output

- Returns a string representing a bar chart showing the percentage spent in each category.

The chart includes labels 0 - 100 down the left side, bars made out of "o" characters, and category names written vertically below the bars. The title at the top says "Percentage spent by category."

## Example Usage

```python
from budget import Category, create_spend_chart

food_category = Category("Food")
clothing_category = Category("Clothing")
auto_category = Category("Auto")

# Perform operations on categories (deposits, withdrawals, transfers, etc.)

categories = [food_category, clothing_category, auto_category]
print(create_spend_chart(categories))
