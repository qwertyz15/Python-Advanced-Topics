# Decorators in Python

Decorators are a powerful and frequently discussed concept in Python interviews. They provide a way to modify or enhance the behavior of functions or methods. This README addresses common questions about decorators and provides insights into their usage.

## Table of Contents

- [What is a Decorator?](#what-is-a-decorator)
- [Defining and Using Decorators](#defining-and-using-decorators)
- [Example of a Simple Decorator](#example-of-a-simple-decorator)
- [Adding Functionality with Decorators](#adding-functionality-with-decorators)
- [Decorators with Arguments](#decorators-with-arguments)
- [Order of Execution with Multiple Decorators](#order-of-execution-with-multiple-decorators)
- [Creating Decorators with Parameters](#creating-decorators-with-parameters)
- [Practical Use Cases](#practical-use-cases)
- [Benefits for Code Organization and Reusability](#benefits-for-code-organization-and-reusability)
- [Built-in Decorators in Python](#built-in-decorators-in-python)

## What is a Decorator?

- A decorator is a function that takes another function (or method) as input, adds some functionality, and returns the modified function.

## Defining and Using Decorators

- Decorators are typically defined using the `@decorator_name` syntax above the function definition.
- They are applied to functions using the `@` symbol followed by the decorator name just before the function definition.

## Example of a Simple Decorator

```python
def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

@my_decorator
def say_hello():
    print("Hello!")

say_hello()
```

## Adding Functionality with Decorators

- Decorators wrap the original function with additional code, which can run before and/or after the original function is called. This allows you to enhance or modify the behavior of the original function.

## Decorators with Arguments

- Yes, decorators can accept arguments. To achieve this, you would create a decorator factory -- a function that returns a decorator.
- The factory can take arguments and return the actual decorator function.

## Order of Execution with Multiple Decorators

- Decorators are applied from the innermost (closest to the function) to the outermost (farthest from the function).
- For example: `@decorator1` `@decorator2` `@decorator3` `def my_function():`

## Creating Decorators with Parameters

```python
def repeat(num):
    def decorator(func):
        def wrapper(*args, **kwargs):
            for _ in range(num):
                func(*args, **kwargs)
        return wrapper
    return decorator

@repeat(num=3)
def say_hello(name):
    print(f"Hello, {name}!")

say_hello("Alice")
```

## Practical Use Cases

- Logging, authentication, memoization (caching), input validation, timing functions, modifying returned values, etc.

## Benefits for Code Organization and Reusability

- Decorators allow you to separate cross-cutting concerns (such as logging, validation) from your core logic, making your codebase cleaner and more modular.
- They promote code reuse since the same decorator can be applied to multiple functions.

## Built-in Decorators in Python

- Python has built-in decorators like `@staticmethod`, `@classmethod`, and `@property` for defining static methods, class methods, and properties in classes, respectively.

Practice creating decorators, explain their benefits, and demonstrate your ability to use them effectively to modify and enhance the behavior of functions.

Feel free to expand on the explanations, provide more examples, and explore further use cases.
