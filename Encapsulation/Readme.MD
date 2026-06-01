# Encapsulation in Python – Bank Account Example

## Overview

This project demonstrates the concept of **Encapsulation** in Python using a simple Bank Account application.

Encapsulation is one of the fundamental principles of Object-Oriented Programming (OOP). It involves bundling data and methods that operate on that data within a class while restricting direct access to the internal state of the object.

In this example, the account balance is kept private using the double underscore (`__`) notation, and it can only be accessed or modified through public methods.

---

## What is Encapsulation?

Encapsulation helps to:

* Protect data from unauthorized access.
* Control how data is modified.
* Improve code security and maintainability.
* Hide implementation details from users.

---

## Technologies Used

* Python 3
* Object-Oriented Programming (OOP)

---

## Project Structure

```text
bank-encapsulation/
│
├── bank.py
└── README.md
```

---

## Class Design

```text
Bank
│
├── __balance (Private Attribute)
│
├── deposit(amount)
├── withdraw(amount)
└── getbalance()
```

---

## Implementation Details

### Private Attribute

```python
self.__balance = 0
```

The balance is declared as a private attribute using double underscores (`__`), preventing direct access from outside the class.

### Deposit Method

```python
def deposit(self, amount):
    if amount > 0:
        self.__balance += amount
```

Allows users to add money to the account after validating the amount.

### Withdraw Method

```python
def withdraw(self, amount):
    if amount > self.__balance:
        print("Insufficient balance")
```

Ensures that users cannot withdraw more money than is available in the account.

### Get Balance Method

```python
def getbalance(self):
    return self.__balance
```

Provides controlled access to the private balance.

---

## Sample Output

```text
Deposited: 1000
Withdrawn amount: 400
Current Balance: 600
```

---

## Key Learning Points

* Understanding Encapsulation in Python.
* Using private attributes with `__` (double underscore).
* Protecting object data from direct modification.
* Accessing private data through public methods.
* Implementing data validation within class methods.

---

## How to Run

1. Clone the repository:

```bash
git clone <repository-url>
```

2. Navigate to the project folder:

```bash
cd bank-encapsulation
```

3. Run the program:

```bash
python bank.py
```

---

## OOP Concept Demonstrated

✅ **Encapsulation**

The `Bank` class encapsulates the account balance by making it private and providing controlled access through methods like `deposit()`, `withdraw()`, and `getbalance()`.
