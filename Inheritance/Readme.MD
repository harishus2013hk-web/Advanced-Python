# Inheritance in Python – Hybrid Inheritance Example

## Overview

This project demonstrates the concept of **Inheritance** in Python using a Hybrid Inheritance example.

Inheritance is an Object-Oriented Programming (OOP) principle that allows a class to inherit properties and methods from another class, promoting code reusability and hierarchical relationships between classes.

In this example, the `Bat` class inherits features from both `Mammal` and `Bird`, while both classes inherit from `Animal`.

---

## What is Inheritance?

Inheritance allows:

* Reusing existing code.
* Creating hierarchical class relationships.
* Extending functionality without modifying existing code.
* Reducing code duplication.

---

## Types of Inheritance Demonstrated

### Hierarchical Inheritance

```text
Animal
├── Bird
└── Mammal
```

Both `Bird` and `Mammal` inherit from `Animal`.

### Multiple Inheritance

```text
Bird      Mammal
   \      /
     \  /
      Bat
```

`Bat` inherits from both `Bird` and `Mammal`.

### Hybrid Inheritance

A combination of hierarchical and multiple inheritance forms **Hybrid Inheritance**.

---

## Class Structure

```text
Animal
│
├── Bird
│   └── fly()
│
├── Mammal
│   └── walk()
│
└── Bat
    ├── eat()   (from Animal)
    ├── walk()  (from Mammal)
    ├── fly()   (from Bird)
    └── sound()
```

---

## Implementation Details

### Parent Class

```python
class Animal:
    def eat(self):
        print("Animal eats")
```

Provides a common behavior for all animals.

### Child Classes

```python
class Bird(Animal):
    def fly(self):
        print("Bird flies")

class Mammal(Animal):
    def walk(self):
        print("Mammal walks")
```

Both classes inherit the `eat()` method from `Animal`.

### Hybrid Inheritance Class

```python
class Bat(Mammal, Bird):
    def sound(self):
        print("Bat screeches")
```

The `Bat` class inherits methods from:

* `Animal`
* `Bird`
* `Mammal`

and adds its own behavior.

---

## Sample Output

```text
Animal eats
Mammal walks
Bird flies
Bat screeches
```

---

## Method Resolution Order (MRO)

Python determines the order of method lookup using the Method Resolution Order (MRO).

```python
print(Bat.mro())
```

Output:

```text
[Bat, Mammal, Bird, Animal, object]
```

This order is used when searching for inherited methods.

---

## Key Learning Points

* Understanding Inheritance in Python.
* Using Parent and Child classes.
* Implementing Hierarchical Inheritance.
* Implementing Multiple Inheritance.
* Understanding Hybrid Inheritance.
* Learning about Method Resolution Order (MRO).

---

## How to Run

1. Clone the repository:

```bash
git clone <repository-url>
```

2. Navigate to the project directory:

```bash
cd inheritance-hybrid-example
```

3. Run the program:

```bash
python inheritance.py
```

---

## OOP Concept Demonstrated

✅ **Inheritance**

This project demonstrates how a class can inherit attributes and methods from multiple parent classes, showcasing **Hybrid Inheritance** in Python.
