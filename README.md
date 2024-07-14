[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/WfNmjXUk)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15407779&assignment_repo_type=AssignmentRepo)
# SE-Assignment-6
 Assignment: Introduction to Python
Instructions:
Answer the following questions based on your understanding of Python programming. Provide detailed explanations and examples where appropriate.

 Questions:

(1). Python Basics:
   - What is Python, and what are some of its key features that make it popular among developers? Provide examples of use cases where Python is particularly effective.

### What is Python?

Python is a high-level, interpreted programming language known for its simplicity and readability. Created by Guido van Rossum and first released in 1991, Python emphasizes code readability and ease of use, which makes it a popular choice for both beginners and experienced developers.

### Key Features of Python

1. **Readability and Simplicity:**
   - Python syntax is clear and straightforward, which makes the code easy to read and write.
   ```python
   print("Hello, World!")
   ```

2. **Interpreted Language:**
   - Python is an interpreted language, meaning that it is executed line-by-line, which makes debugging easier.
   ```python
   x = 5
   y = 10
   print(x + y)  # Output: 15
   ```

3. **Dynamic Typing:**
   - Variables in Python do not need explicit declaration to reserve memory space, and the type is determined at runtime.
   ```python
   a = 5       # a is an integer
   a = "Hello" # now a is a string
   ```

4. **Extensive Standard Library:**
   - Python has a vast standard library that supports many common programming tasks such as file I/O, system calls, and even Internet protocols.
   ```python
   import os
   print(os.getcwd())  # Output: Current working directory
   ```

5. **Object-Oriented:**
   - Python supports object-oriented programming (OOP) with classes and objects.
   ```python
   class Dog:
       def __init__(self, name):
           self.name = name

       def bark(self):
           print(f"{self.name} says woof!")

   my_dog = Dog("Buddy")
   my_dog.bark()  # Output: Buddy says woof!
   ```

6. **Cross-Platform:**
   - Python can run on various operating systems, such as Windows, macOS, and Linux, without requiring any changes to the code.

7. **Support for Multiple Paradigms:**
   - Python supports multiple programming paradigms, including procedural, object-oriented, and functional programming.
   ```python
   # Functional programming example
   def add(x, y):
       return x + y

   result = add(5, 3)
   print(result)  # Output: 8
   ```

8. **Large Community and Ecosystem:**
   - Python has a large and active community, which contributes to a rich ecosystem of libraries, frameworks, and tools.

### Use Cases Where Python is Particularly Effective

1. **Web Development:**
   - Python frameworks like Django and Flask are used to build robust web applications.
   ```python
   from flask import Flask
   app = Flask(__name__)

   @app.route('/')
   def home():
       return "Hello, Flask!"

   if __name__ == "__main__":
       app.run(debug=True)
   ```

2. **Data Analysis and Scientific Computing:**
   - Libraries such as Pandas, NumPy, and SciPy are used extensively for data manipulation and scientific computing.
   ```python
   import pandas as pd

   data = {
       'Name': ['Alice', 'Bob', 'Charlie'],
       'Age': [24, 27, 22]
   }

   df = pd.DataFrame(data)
   print(df)
   ```

3. **Machine Learning and Artificial Intelligence:**
   - Python is the go-to language for machine learning and AI, with popular libraries like TensorFlow, Keras, and scikit-learn.
   ```python
   from sklearn.linear_model import LinearRegression
   import numpy as np

   X = np.array([[1, 1], [1, 2], [2, 2], [2, 3]])
   y = np.dot(X, np.array([1, 2])) + 3

   model = LinearRegression().fit(X, y)
   print(model.predict(np.array([[3, 5]])))  # Example prediction
   ```

4. **Automation and Scripting:**
   - Python is widely used for writing scripts to automate repetitive tasks.
   ```python
   import os

   for filename in os.listdir('.'):
       if filename.endswith('.txt'):
           print(f"Text file: {filename}")
   ```

5. **Game Development:**
   - Libraries like Pygame are used to develop 2D games.
   ```python
   import pygame

   pygame.init()
   screen = pygame.display.set_mode((640, 480))
   running = True

   while running:
       for event in pygame.event.get():
           if event.type == pygame.QUIT:
               running = False

   pygame.quit()
   ```

6. **Network Programming:**
   - Python provides libraries for network programming and building network applications.
   ```python
   import socket

   s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
   s.connect(("www.example.com", 80))
   s.sendall(b"GET / HTTP/1.1\r\nHost: www.example.com\r\n\r\n")
   data = s.recv(1024)
   print(data)
   s.close()
   ```

Python’s versatility and ease of use make it suitable for a wide range of applications, from simple scripts to complex web applications and machine learning models.











Qn (2). Installing Python:
   - Describe the steps to install Python on your operating system (Windows, macOS, or Linux). Include how to verify the installation and set up a virtual environment.


   ### Installing Python on Various Operating Systems

#### 1. Windows

**Step 1: Download Python Installer**
- Go to the official [Python website](https://www.python.org/).
- Navigate to the Downloads section and select the latest Python release for Windows.

**Step 2: Run the Installer**
- Open the downloaded .exe file.
- Check the box that says "Add Python to PATH" at the bottom of the installer window.
- Click "Install Now" for a simple installation or "Customize installation" if you need specific settings.

**Step 3: Verify Installation**
- Open Command Prompt (search for `cmd` in the Start menu).
- Type `python --version` or `python -V` and press Enter. You should see the version number of Python.

**Step 4: Install `pip`**
- `pip` is usually installed with Python. Verify by running `pip --version` in Command Prompt.
- If not installed, download `get-pip.py` from [pip’s official site](https://pip.pypa.io/en/stable/installing/) and run `python get-pip.py`.

**Step 5: Set Up a Virtual Environment**
- Navigate to your project directory in Command Prompt.
- Create a virtual environment by running:
  ```sh
  python -m venv env
  ```
- Activate the virtual environment:
  ```sh
  .\env\Scripts\activate
  ```

#### 2. macOS

**Step 1: Download Python Installer**
- Go to the official [Python website](https://www.python.org/).
- Navigate to the Downloads section and select the latest Python release for macOS.

**Step 2: Run the Installer**
- Open the downloaded .pkg file and follow the on-screen instructions to install Python.

**Step 3: Verify Installation**
- Open Terminal.
- Type `python3 --version` and press Enter. You should see the version number of Python.

**Step 4: Install `pip`**
- `pip` is usually installed with Python. Verify by running `pip3 --version` in Terminal.
- If not installed, use `easy_install` to install `pip`:
  ```sh
  sudo easy_install pip
  ```

**Step 5: Set Up a Virtual Environment**
- Navigate to your project directory in Terminal.
- Create a virtual environment by running:
  ```sh
  python3 -m venv env
  ```
- Activate the virtual environment:
  ```sh
  source env/bin/activate
  ```

#### 3. Linux (Ubuntu/Debian)

**Step 1: Update Package List**
- Open Terminal and run:
  ```sh
  sudo apt update
  ```

**Step 2: Install Python**
- Install Python by running:
  ```sh
  sudo apt install python3
  ```

**Step 3: Verify Installation**
- Verify by typing `python3 --version` and pressing Enter. You should see the version number of Python.

**Step 4: Install `pip`**
- Install `pip` by running:
  ```sh
  sudo apt install python3-pip
  ```
- Verify `pip` installation by running `pip3 --version`.

**Step 5: Set Up a Virtual Environment**
- Install the virtual environment package:
  ```sh
  sudo apt install python3-venv
  ```
- Navigate to your project directory in Terminal.
- Create a virtual environment by running:
  ```sh
  python3 -m venv env
  ```
- Activate the virtual environment:
  ```sh
  source env/bin/activate
  ```

### Verifying Installation and Setting Up a Virtual Environment

**Verifying Installation:**
- After installing Python, verify it by opening your command line interface (Command Prompt on Windows, Terminal on macOS/Linux) and typing:
  ```sh
  python --version  # or python3 --version on macOS/Linux
  ```
  This should return the installed version of Python.

**Setting Up a Virtual Environment:**
1. **Create a Virtual Environment:**
   ```sh
   python -m venv env  # or python3 -m venv env on macOS/Linux
   ```
2. **Activate the Virtual Environment:**
   - **Windows:**
     ```sh
     .\env\Scripts\activate
     ```
   - **macOS/Linux:**
     ```sh
     source env/bin/activate
     ```
3. **Deactivate the Virtual Environment:**
   ```sh
   deactivate
   ```

By following these steps, you can install Python on your operating system, verify the installation, and set up a virtual environment for your projects.











Qn (3). Python Syntax and Semantics:
   - Write a simple Python program that prints "Hello, World!" to the console. Explain the basic syntax elements used in the program.
'''
print('Hello, World!')

'''

   print() Function:

The print() function is a built-in Python function used to output text to the console.
In this example, print() is used to display the string "Hello, World!".
Strings:

A string is a sequence of characters enclosed in quotation marks. In Python, you can use either single (') or double (") quotation marks to define a string.
Here, "Hello, World!" is a string literal enclosed in double quotation marks.
Function Call:

In Python, you call a function by typing the function name followed by parentheses ().
The parentheses can contain arguments that you pass to the function. In this case, the string "Hello, World!" is passed as an argument to the print() function.





Qn (4). Data Types and Variables:
   - List and describe the basic data types in Python. Write a short script that demonstrates how to create and use variables of different data types.


   
Basic Data Types in Python
Python has several built-in data types, which can be broadly categorized into the following groups:

Numeric Types:

int: Represents integers, which are whole numbers without a fractional part.
float: Represents floating-point numbers, which are numbers with a decimal point.
complex: Represents complex numbers, which have a real part and an imaginary part.
Sequence Types:

str: Represents strings, which are sequences of characters.
list: Represents ordered collections of items, which can be of different data types.
tuple: Represents ordered, immutable collections of items, which can be of different data types.
Mapping Type:

dict: Represents unordered collections of key-value pairs.
Set Types:

set: Represents unordered collections of unique items.
frozenset: Represents immutable sets.
Boolean Type:

bool: Represents Boolean values, which can be either True or False.
None Type:

NoneType: Represents the absence of a value or a null value. It has a single value, None.
Script Demonstrating Variables of Different Data Types
Here's a short Python script that demonstrates how to create and use variables of different data types:

python
Copy code
# Numeric Types
int_var = 10                # Integer
float_var = 20.5








5. Control Structures:
   - Explain the use of conditional statements and loops in Python. Provide examples of an `if-else` statement and a `for` loop.


   ### 4. Data Types and Variables

#### Basic Data Types in Python

1. **Integer (`int`):**
   - Whole numbers, positive or negative, without a decimal point.
   ```python
   age = 25
   ```

2. **Float (`float`):**
   - Numbers with a decimal point.
   ```python
   height = 5.9
   ```

3. **String (`str`):**
   - A sequence of characters enclosed in quotation marks.
   ```python
   name = "Alice"
   ```

4. **Boolean (`bool`):**
   - Represents `True` or `False`.
   ```python
   is_student = True
   ```

5. **List (`list`):**
   - An ordered collection of items, which can be of different types.
   ```python
   numbers = [1, 2, 3, 4, 5]
   ```

6. **Tuple (`tuple`):**
   - An ordered, immutable collection of items.
   ```python
   coordinates = (10.0, 20.0)
   ```

7. **Dictionary (`dict`):**
   - A collection of key-value pairs.
   ```python
   student = {"name": "Alice", "age": 25}
   ```

8. **Set (`set`):**
   - An unordered collection of unique items.
   ```python
   unique_numbers = {1, 2, 3, 4, 5}
   ```

### Script Demonstrating Variables of Different Data Types

```python
# Integer
age = 25
print("Age:", age)

# Float
height = 5.9
print("Height:", height)

# String
name = "Alice"
print("Name:", name)

# Boolean
is_student = True
print("Is student:", is_student)

# List
numbers = [1, 2, 3, 4, 5]
print("Numbers:", numbers)

# Tuple
coordinates = (10.0, 20.0)
print("Coordinates:", coordinates)

# Dictionary
student = {"name": "Alice", "age": 25}
print("Student:", student)

# Set
unique_numbers = {1, 2, 3, 4, 5}
print("Unique numbers:", unique_numbers)
```

### 5. Control Structures

#### Conditional Statements

Conditional statements allow you to execute certain blocks of code based on conditions. The primary conditional statements in Python are `if`, `elif`, and `else`.

**Example of an `if-else` Statement:**

```python
age = 18

if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```

#### Loops

Loops are used to repeat a block of code multiple times. Python supports `for` and `while` loops.

**Example of a `for` Loop:**

```python
numbers = [1, 2, 3, 4, 5]

for number in numbers:
    print("Number:", number)
```

**Example of a `while` Loop:**

```python
count = 0

while count < 5:
    print("Count:", count)
    count += 1
```

### Detailed Explanation of Control Structures

- **`if` Statement:**
  - The `if` statement evaluates a condition. If the condition is `True`, the block of code inside the `if` statement is executed.
  - Example:
    ```python
    number = 10
    if number > 5:
        print("Number is greater than 5")
    ```

- **`elif` Statement:**
  - Short for "else if," `elif` allows you to check multiple expressions for `True` and execute a block of code as soon as one of the conditions is `True`.
  - Example:
    ```python
    number = 10
    if number > 10:
        print("Number is greater than 10")
    elif number == 10:
        print("Number is exactly 10")
    else:
        print("Number is less than 10")
    ```

- **`else` Statement:**
  - The `else` statement catches anything which isn't caught by the preceding conditions.
  - Example:
    ```python
    number = 4
    if number > 10:
        print("Number is greater than 10")
    else:
        print("Number is 10 or less")
    ```

- **`for` Loop:**
  - The `for` loop iterates over a sequence (like a list, tuple, dictionary, set, or string) and executes a block of code for each item in the sequence.
  - Example:
    ```python
    fruits = ["apple", "banana", "cherry"]
    for fruit in fruits:
        print(fruit)
    ```

- **`while` Loop:**
  - The `while` loop repeats as long as a certain condition is `True`.
  - Example:
    ```python
    count = 1
    while count < 6:
        print(count)
        count += 1
    ```

These control structures are fundamental to controlling the flow of a Python program, allowing you to make decisions and repeat actions as necessary.





Qn (6). Functions in Python:
   - What are functions in Python, and why are they useful? Write a Python function that takes two arguments and returns their sum. Include an example of how to call this function.



### Functions in Python

#### What are Functions?

Functions in Python are reusable blocks of code that perform a specific task. They can take inputs (arguments), process them, and return an output (result). Functions help in organizing code, making it more readable, maintainable, and reusable.

#### Why are Functions Useful?

1. **Code Reusability:**
   - Functions allow you to write code once and reuse it multiple times without duplicating the code.

2. **Modularity:**
   - Breaking a program into smaller, manageable functions makes it easier to understand, test, and debug.

3. **Abstraction:**
   - Functions provide a way to abstract complex operations, allowing you to use them without needing to understand their internal workings.

4. **Improved Readability:**
   - Well-named functions can make code self-documenting and more understandable.

### Writing a Function to Calculate the Sum of Two Arguments

Here is an example of a simple Python function that takes two arguments and returns their sum:

```python
def add_numbers(a, b):
    """
    This function takes two arguments and returns their sum.
    
    Parameters:
    a (int or float): The first number.
    b (int or float): The second number.
    
    Returns:
    int or float: The sum of the two numbers.
    """
    return a + b
```

#### Example of How to Call This Function

To call the function `add_numbers`, you need to pass two arguments to it. The function will return their sum, which you can print or store in a variable.

```python
# Example of calling the function

# Call the function with integers
result = add_numbers(5, 3)
print("The sum is:", result)  # Output: The sum is: 8

# Call the function with floats
result = add_numbers(2.5, 4.7)
print("The sum is:", result)  # Output: The sum is: 7.2
```

### Detailed Explanation

- **Function Definition:**
  ```python
  def add_numbers(a, b):
  ```
  - `def` is the keyword used to define a function.
  - `add_numbers` is the name of the function.
  - `a` and `b` are parameters that the function accepts.

- **Docstring:**
  ```python
  """
  This function takes two arguments and returns their sum.
  
  Parameters:
  a (int or float): The first number.
  b (int or float): The second number.
  
  Returns:
  int or float: The sum of the two numbers.
  """
  ```
  - A docstring is a string literal that appears right after the function definition. It is used to document the function’s purpose, parameters, and return value.

- **Function Body:**
  ```python
  return a + b
  ```
  - The body of the function performs the addition of `a` and `b` and returns the result.

- **Calling the Function:**
  ```python
  result = add_numbers(5, 3)
  ```
  - The function `add_numbers` is called with arguments `5` and `3`.
  - The returned value (`8`) is stored in the variable `result`.
  - The `print` statement displays the result.

By using functions, you can break down complex problems into simpler, more manageable tasks, making your code cleaner and more efficient.




7. Lists and Dictionaries:
   - Describe the differences between lists and dictionaries in Python. Write a script that creates a list of numbers and a dictionary with some key-value pairs, then demonstrates basic operations on both.



### Differences Between Lists and Dictionaries in Python

#### Lists

- **Ordered:**
  - Lists maintain the order of elements as they are inserted. The elements can be accessed by their index.
- **Mutable:**
  - Lists are mutable, meaning their elements can be changed, added, or removed.
- **Homogeneous or Heterogeneous:**
  - Lists can contain elements of different data types, including integers, strings, and even other lists.

Example of a List:
```python
numbers = [1, 2, 3, 4, 5]
```

#### Dictionaries

- **Unordered:**
  - Dictionaries do not maintain any order for the elements. Starting from Python 3.7, dictionaries are insertion-ordered, but traditionally they are considered unordered.
- **Mutable:**
  - Dictionaries are mutable, meaning their elements (key-value pairs) can be changed, added, or removed.
- **Key-Value Pairs:**
  - Dictionaries contain key-value pairs where each key must be unique and immutable (e.g., strings, numbers, or tuples), but values can be of any data type and can be duplicated.

Example of a Dictionary:
```python
student = {"name": "Alice", "age": 25, "grade": "A"}
```

### Script Demonstrating Lists and Dictionaries

```python
# Creating a list of numbers
numbers = [1, 2, 3, 4, 5]
print("Original list:", numbers)

# Basic operations on the list
# Adding an element to the list
numbers.append(6)
print("After appending 6:", numbers)

# Removing an element from the list
numbers.remove(3)
print("After removing 3:", numbers)

# Accessing an element by index
print("Element at index 2:", numbers[2])

# Slicing the list
print("Slicing from index 1 to 3:", numbers[1:4])

# Creating a dictionary with key-value pairs
student = {
    "name": "Alice",
    "age": 25,
    "grade": "A"
}
print("Original dictionary:", student)

# Basic operations on the dictionary
# Adding a new key-value pair
student["major"] = "Computer Science"
print("After adding major:", student)

# Removing a key-value pair
del student["age"]
print("After deleting age:", student)

# Accessing a value by key
print("Student's name:", student["name"])

# Checking if a key exists in the dictionary
print("Is 'grade' a key in the dictionary?", "grade" in student)

# Iterating over the dictionary
print("Iterating over dictionary:")
for key, value in student.items():
    print(key, ":", value)
```

### Explanation of Script

#### List Operations

1. **Creating a List:**
   ```python
   numbers = [1, 2, 3, 4, 5]
   ```
   - Creates a list of numbers.

2. **Appending an Element:**
   ```python
   numbers.append(6)
   ```
   - Adds the element `6` to the end of the list.

3. **Removing an Element:**
   ```python
   numbers.remove(3)
   ```
   - Removes the first occurrence of the element `3` from the list.

4. **Accessing an Element by Index:**
   ```python
   numbers[2]
   ```
   - Accesses the element at index `2` (the third element).

5. **Slicing the List:**
   ```python
   numbers[1:4]
   ```
   - Slices the list to get elements from index `1` to `3` (inclusive of the start index, exclusive of the end index).

#### Dictionary Operations

1. **Creating a Dictionary:**
   ```python
   student = {
       "name": "Alice",
       "age": 25,
       "grade": "A"
   }
   ```
   - Creates a dictionary with key-value pairs.

2. **Adding a Key-Value Pair:**
   ```python
   student["major"] = "Computer Science"
   ```
   - Adds a new key-value pair `"major": "Computer Science"` to the dictionary.

3. **Removing a Key-Value Pair:**
   ```python
   del student["age"]
   ```
   - Removes the key-value pair with the key `"age"` from the dictionary.

4. **Accessing a Value by Key:**
   ```python
   student["name"]
   ```
   - Accesses the value associated with the key `"name"`.

5. **Checking for a Key:**
   ```python
   "grade" in student
   ```
   - Checks if the key `"grade"` exists in the dictionary.

6. **Iterating Over the Dictionary:**
   ```python
   for key, value in student.items():
       print(key, ":", value)
   ```
   - Iterates over the dictionary, printing each key and its corresponding value.

This script demonstrates the creation and manipulation of lists and dictionaries in Python, showcasing the differences and basic operations you can perform with each data type.

qn (8). Exception Handling:
   - What is exception handling in Python? Provide an example of how to use `try`, `except`, and `finally` blocks to handle errors in a Python script.

   ### Exception Handling in Python

**Exception handling** is a mechanism in Python that allows you to manage errors gracefully without crashing the program. It enables you to write code that can respond to runtime errors and continue execution or provide meaningful error messages.

### Key Components of Exception Handling

- **`try` Block:** This block contains code that might raise an exception.
- **`except` Block:** This block defines how to handle the exception if it occurs.
- **`finally` Block:** This block is executed regardless of whether an exception occurred or not. It is typically used for cleanup actions.

### Example of Exception Handling

Here’s a simple Python script demonstrating how to use `try`, `except`, and `finally` blocks:

```python
def divide_numbers(num1, num2):
    try:
        result = num1 / num2
    except ZeroDivisionError:
        print("Error: Cannot divide by zero.")
        return None
    except TypeError:
        print("Error: Please provide numbers only.")
        return None
    else:
        print("Division successful!")
        return result
    finally:
        print("Execution of divide_numbers() complete.")

# Example calls
print(divide_numbers(10, 2))  # Should print: 5.0
print(divide_numbers(10, 0))  # Should print an error message
print(divide_numbers(10, "a"))  # Should print an error message
```

### Explanation of the Example

1. **Function Definition:**
   ```python
   def divide_numbers(num1, num2):
   ```
   - Defines a function that takes two arguments to perform division.

2. **`try` Block:**
   ```python
   try:
       result = num1 / num2
   ```
   - Attempts to divide `num1` by `num2`. If `num2` is zero, a `ZeroDivisionError` will be raised.

3. **`except` Block:**
   - **Handling ZeroDivisionError:**
     ```python
     except ZeroDivisionError:
         print("Error: Cannot divide by zero.")
     ```
     - Catches the exception when trying to divide by zero and prints an error message.

   - **Handling TypeError:**
     ```python
     except TypeError:
         print("Error: Please provide numbers only.")
     ```
     - Catches exceptions when non-numeric types are passed to the function.

4. **`else` Block:**
   ```python
   else:
       print("Division successful!")
       return result
   ```
   - Executes if no exceptions are raised in the `try` block, indicating successful division.

5. **`finally` Block:**
   ```python
   finally:
       print("Execution of divide_numbers() complete.")
   ```
   - This block runs regardless of whether an exception occurred or not, useful for cleanup actions or final messages.

### Output of Example Calls

1. **Successful Division:**
   ```plaintext
   Division successful!
   Execution of divide_numbers() complete.
   5.0
   ```

2. **Division by Zero:**
   ```plaintext
   Error: Cannot divide by zero.
   Execution of divide_numbers() complete.
   None
   ```

3. **Passing a Non-Numeric Value:**
   ```plaintext
   Error: Please provide numbers only.
   Execution of divide_numbers() complete.
   None
   ```

### Summary

Exception handling in Python is crucial for building robust applications. By using `try`, `except`, and `finally` blocks, you can manage errors gracefully and maintain the flow of your program.





9. Modules and Packages:
   - Explain the concepts of modules and packages in Python. How can you import and use a module in your script? Provide an example using the `math` module.


### Modules and Packages in Python

#### Modules

- **Definition:** 
  - A module is a file containing Python code, such as functions, classes, or variables, which can be reused in other scripts.
- **Purpose:** 
  - Modules help in organizing and managing large codebases by breaking the code into smaller, manageable, and reusable parts.

#### Packages

- **Definition:** 
  - A package is a collection of related modules organized in directories that include a special `__init__.py` file, indicating that the directory should be treated as a package.
- **Purpose:** 
  - Packages allow for a hierarchical structuring of the module namespace using dot notation.

### Importing and Using a Module

To import and use a module in your script, you use the `import` statement. 

### Example Using the `math` Module

The `math` module provides mathematical functions, such as trigonometric functions, logarithms, and more.

```python
import math

# Using the math module
number = 16
square_root = math.sqrt(number)
print(f"The square root of {number} is {square_root}")

angle = math.pi / 4  # 45 degrees in radians
cosine = math.cos(angle)
print(f"The cosine of 45 degrees is {cosine}")
```

### Explanation

1. **Importing the `math` Module:**
   ```python
   import math
   ```
   - Imports the `math` module, making its functions available in the script.

2. **Using `math.sqrt()`:**
   ```python
   square_root = math.sqrt(number)
   ```
   - Calculates the square root of `number` using the `sqrt()` function from the `math` module.

3. **Using `math.cos()`:**
   ```python
   cosine = math.cos(angle)
   ```
   - Calculates the cosine of `angle` (in radians) using the `cos()` function from the `math` module.

### Summary

- **Modules** are single files of Python code that provide reusable components.
- **Packages** are collections of modules organized in directories with an `__init__.py` file.
- Use the `import` statement to include modules in your scripts and access their functions.




10. File I/O:
    - How do you read from and write to files in Python? Write a script that reads the content of a file and prints it to the console, and another script that writes a list of strings to a file.


### Reading from a File

```python
# Reading from a file and printing its content
with open('example.txt', 'r') as file:
    content = file.read()
    print(content)
```

### Writing to a File

```python
# Writing a list of strings to a file
lines = ["First line", "Second line", "Third line"]

with open('output.txt', 'w') as file:
    for line in lines:
        file.write(line + '\n')
```










# Submission Guidelines:
- Your answers should be well-structured, concise, and to the point.
- Provide code snippets or complete scripts where applicable.
- Cite any references or sources you use in your answers.
- Submit your completed assignment by [due date].


