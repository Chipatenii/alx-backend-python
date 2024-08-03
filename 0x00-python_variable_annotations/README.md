---

# Python Type Annotations

This repository is dedicated to exploring and demonstrating type annotations in Python 3, duck typing principles, and code validation using mypy.

## Table of Contents

- [Overview](#overview)
- [Type Annotations in Python 3](#type-annotations-in-python-3)
- [Function Signatures and Variable Types](#function-signatures-and-variable-types)
- [Duck Typing](#duck-typing)
- [Validating Code with mypy](#validating-code-with-mypy)
- [Variable Annotations](#variable-annotations)

## Overview

This repository provides examples and explanations on how to use type annotations in Python to improve code clarity and maintainability. It also covers the concept of duck typing and how to validate type annotations using mypy.

## Type Annotations in Python 3

Type annotations in Python 3 allow you to specify the expected data types of variables, function parameters, and return values. This can help with code readability and provide better support from IDEs and type checkers.

## Function Signatures and Variable Types

Here's an example of how to use type annotations for function signatures and variable types:

```python
def add(a: int, b: int) -> int:
    return a + b

x: int = 10
y: int = 20
result: int = add(x, y)
```

In this example, `a` and `b` are expected to be integers, and the function `add` will return an integer.

## Duck Typing

Duck typing is a concept related to dynamic typing, where the type or class of an object is determined by its behavior (methods and properties) rather than its explicit inheritance from a particular class.

Example:

```python
class Duck:
    def quack(self):
        print("Quack!")

class Person:
    def quack(self):
        print("I'm quacking like a duck!")

def make_quack(thing):
    thing.quack()

d = Duck()
p = Person()

make_quack(d)  # Quack!
make_quack(p)  # I'm quacking like a duck!
```

## Validating Code with mypy

Mypy is a static type checker for Python. It can be used to ensure your type annotations are correct and consistent throughout your code.

To install mypy:

```bash
pip install mypy
```

To check your code with mypy:

```bash
mypy your_script.py
```

Example:

```python
# your_script.py

def add(a: int, b: int) -> int:
    return a + b

result = add(1, '2')  # mypy will catch this type error
```

Running `mypy your_script.py` will report a type error because `b` is expected to be an integer, not a string.

## Variable Annotations

Variable annotations provide a way to specify the expected type of a variable. This can be particularly useful for improving code readability and type checking.

Example:

```python
x: int = 10
y: float = 20.5
name: str = "Alice"
```
