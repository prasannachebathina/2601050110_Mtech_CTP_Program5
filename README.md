# Banking Management System

## Aim

To develop a simple Banking Management System demonstrating **abstraction, inheritance, dataclasses, and full type hints** in Python.

## Objective

The system manages different types of bank accounts using object-oriented programming.

The parent class `BankAccount` contains common banking operations, while child classes implement their own interest calculation.

## Class Structure

```text
                BankAccount
                Abstract Class
                      |
             ┌────────┴────────┐
             ↓                 ↓
       SavingsAccount     CurrentAccount
```

## Concepts Used

### 1. Abstraction

`BankAccount` is an abstract class.

```python
class BankAccount(ABC):
```

The `calculate_interest()` method is declared as an abstract method.

```python
@abstractmethod
def calculate_interest(self) -> float:
    pass
```

### 2. Inheritance

`SavingsAccount` and `CurrentAccount` inherit from `BankAccount`.

```python
class SavingsAccount(BankAccount):
```

```python
class CurrentAccount(BankAccount):
```

### 3. Dataclass

The `@dataclass` decorator is used to reduce boilerplate code.

```python
@dataclass
class BankAccount(ABC):
```

### 4. Type Hints

The program uses type hints throughout the classes and methods.

Example:

```python
def deposit(self, amount: float) -> None:
```

## Algorithm / Procedure

1. Create an abstract `BankAccount` class.
2. Define account number, holder name and balance.
3. Define deposit and withdrawal methods.
4. Define abstract `calculate_interest()` method.
5. Create `SavingsAccount` by inheriting `BankAccount`.
6. Create `CurrentAccount` by inheriting `BankAccount`.
7. Implement interest calculation in both child classes.
8. Create account objects.
9. Perform deposit and withdrawal operations.
10. Display account details and interest.

## Data

### Savings Account

```text
Account Number = 101
Holder Name = Rahul
Initial Balance = ₹10,000
Deposit = ₹2,000
Withdrawal = ₹1,000
Interest Rate = 4%
```

### Current Account

```text
Account Number = 102
Holder Name = Priya
Initial Balance = ₹20,000
Deposit = ₹5,000
Withdrawal = ₹3,000
Interest Rate = 2%
```

## Result

### Savings Account

```text
Final Balance = ₹11,000
Interest = ₹440
```

### Current Account

```text
Final Balance = ₹22,000
Interest = ₹440
```

## Sample Output

```text
Deposited: ₹2000.00
Withdrawn: ₹1000.00

Account Number: 101
Holder Name: Rahul
Balance: ₹ 11000.00
Savings Interest: ₹ 440.00

Deposited: ₹5000.00
Withdrawn: ₹3000.00

Account Number: 102
Holder Name: Priya
Balance: ₹ 22000.00
Current Interest: ₹ 440.00
```

## Inference

The Banking Management System demonstrates abstraction by defining a common abstract account class and inheritance by deriving SavingsAccount and CurrentAccount from it.

Common operations such as deposit, withdrawal and display are reused from the parent class.

## Conclusion

The Banking Management System is successfully implemented using Python object-oriented programming. Abstraction provides a common structure for bank accounts, while inheritance allows different account types to reuse and extend the common functionality.
