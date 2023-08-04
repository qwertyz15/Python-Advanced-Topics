# Closures and Scopes in Python

Closures and scopes are fundamental concepts in Python that deal with how variables are accessed and preserved in different contexts. This README addresses common questions about closures and scopes and provides insights into their usage.

## Table of Contents

- [What is a Closure in Python?](#what-is-a-closure-in-python)
- [The Concept of Lexical Scope](#the-concept-of-lexical-scope)
- [Difference Between Closures and Regular Functions](#difference-between-closures-and-regular-functions)
- [Example of a Closure](#example-of-a-closure)
- [The Purpose of the `nonlocal` Keyword](#the-purpose-of-the-nonlocal-keyword)
- [Global and Local Scope](#global-and-local-scope)
- [Variable Name Resolution in Different Scopes](#variable-name-resolution-in-different-scopes)
- [The `global` Keyword](#the-global-keyword)
- [The LEGB Rule in Python Scoping](#the-legb-rule-in-python-scoping)
- [Lifetime of a Variable in Python](#lifetime-of-a-variable-in-python)
- [Relation Between Closures and Decorators](#relation-between-closures-and-decorators)
- [Implications of Using Mutable Objects within Closures](#implications-of-using-mutable-objects-within-closures)

## What is a Closure in Python?

- A closure is a function that remembers the values in the enclosing scope even if they are not present in memory. It "closes over" the variables it needs.

## The Concept of Lexical Scope

- Lexical scope refers to the idea that a nested function has access to the variables in its containing (enclosing) function's scope.

## Difference Between Closures and Regular Functions

- A closure "closes over" variables from its enclosing scope, even after the enclosing function has finished executing. A regular function doesn't do this.

## Example of a Closure

```python
def outer_function(x):
    def inner_function(y):
        return x + y
    return inner_function

closure = outer_function(10)
result = closure(5)  # Result will be 15
```

## The Purpose of the `nonlocal` Keyword

- The `nonlocal` keyword allows you to modify a variable in an outer (but non-global) scope. It is often used in closures.

## Global and Local Scope

- The global scope is the outermost scope, applicable throughout the entire program.
- The local scope is within a function or block and contains variables that are only accessible within that function or block.

## Variable Name Resolution in Different Scopes

- Python searches for variable names first in the local scope, then in any enclosing (non-global) scopes, and finally in the global scope.

## The `global` Keyword

- The `global` keyword is used to indicate that a variable is in the global scope, not a local scope.

## The LEGB Rule in Python Scoping

- The LEGB rule defines the order in which Python searches for variable names: Local, Enclosing, Global, Built-in.

## Lifetime of a Variable in Python

- The lifetime of a variable is the period during which the variable exists in memory. It starts when the variable is created and ends when it's deleted or goes out of scope.

## Relation Between Closures and Decorators

- Closures are often used to implement decorators. A decorator is a function that takes another function as input and returns a modified version of that function, often with added functionality. Closures help capture the original function and any additional arguments.

## Implications of Using Mutable Objects within Closures

- If mutable objects like lists or dictionaries are used in a closure and modified within the closure, the modifications will persist across calls to the closure.

Understanding closures and scopes is important for writing clean, modular, and maintainable code. Be ready to provide examples and explain how closures capture and preserve variables from their enclosing scopes.
