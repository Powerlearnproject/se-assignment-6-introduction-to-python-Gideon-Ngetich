[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/WfNmjXUk)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15306640&assignment_repo_type=AssignmentRepo)
# SE-Assignment-6
 Assignment: Introduction to Python
Instructions:
Answer the following questions based on your understanding of Python programming. Provide detailed explanations and examples where appropriate.

 Questions:

1. Python Basics:
   - What is Python, and what are some of its key features that make it popular among developers? Provide examples of use cases where Python is particularly effective.

   =>Python is a high-level, interpreted programming language renowned for its readability, simplicity, and versatility, making it a favorite among developers. Its intuitive syntax enhances code readability, which is particularly beneficial for beginners and experienced programmers alike. Python's interpreted nature allows for immediate execution of code line by line, simplifying debugging and testing processes. Additionally, dynamic typing provides flexibility by allowing variable types to be determined at runtime. These features, combined with Python's extensive standard library and active community support, make it suitable for a wide range of applications, from web development to data science and automation.

2. Installing Python:
   - Describe the steps to install Python on your operating system (Windows, macOS, or Linux). Include how to verify the installation and set up a virtual environment.

   => # Update package list
         sudo apt update

         # Install Python 3.9
         sudo apt install python3.9

         # Verify Python installation
         python3.9 --version

         # Install venv module (if not already installed)
         sudo apt install python3.9-venv

         # Create a new directory for your project
         mkdir myproject
         cd myproject

         # Create a virtual environment named 'venv'
         python3.9 -m venv venv

         # Activate the virtual environment
         source venv/bin/activate

         # Verify the virtual environment
         which python

3. Python Syntax and Semantics:
   - Write a simple Python program that prints "Hello, World!" to the console. Explain the basic syntax elements used in the program.

   => # This is a single-line comment
      print("Hello, World!")

      1. Comments:
         In Python, comments start with the # symbol. Anything following this symbol on the same line is considered a comment and is ignored by the Python interpreter.
         Comments are used to explain the code and make it more readable.
      2. print() Function:
         The print() function is used to output text or other values to the console.
      3. String Literals:
         A string literal is a sequence of characters enclosed in quotes.

4. Data Types and Variables:
   - List and describe the basic data types in Python. Write a short script that demonstrates how to create and use variables of different data types.

   => Integer (int):
      Represents whole numbers, positive or negative, without decimals.
      Example: 10, -5, 0

      Floating Point (float):

         Represents real numbers with a decimal point.
         Example: 10.5, -3.14, 0.0

      String (str):

         Represents sequences of characters enclosed in single or double quotes.
         Example: "Hello", 'Python'

      Boolean (bool):

         Represents one of two values: True or False.
         Example: True, False

      List (list):

         Represents an ordered collection of items which can be of different types.
         Example: [1, 2, 3], ['a', 'b', 'c']

      Tuple (tuple):

         Represents an ordered collection of items similar to a list, but immutable (cannot be changed).
         Example: (1, 2, 3), ('a', 'b', 'c')

      Dictionary (dict):

         Represents a collection of key-value pairs.
         Example: {'name': 'Alice', 'age': 25}, {'a': 1, 'b': 2}

      Set (set):

         Represents an unordered collection of unique items.
         Example: `{1, 2, 3}`, `{'a', 'b', 'c'}`

      # Integer
      age = 30
      print(f"Age: {age}, Type: {type(age)}")

      # Floating Point
      height = 5.9
      print(f"Height: {height}, Type: {type(height)}")

      # String
      name = "Alice"
      print(f"Name: {name}, Type: {type(name)}")

      # Boolean
      is_student = True
      print(f"Is Student: {is_student}, Type: {type(is_student)}")

      # List
      fruits = ["apple", "banana", "cherry"]
      print(f"Fruits: {fruits}, Type: {type(fruits)}")

      # Tuple
      coordinates = (10.0, 20.0)
      print(f"Coordinates: {coordinates}, Type: {type(coordinates)}")

      # Dictionary
      person = {"name": "Bob", "age": 25}
      print(f"Person: {person}, Type: {type(person)}")

      # Set
      unique_numbers = {1, 2, 3, 4, 5}
      print(f"Unique Numbers: {unique_numbers}, Type: {type(unique_numbers)}")


5. Control Structures:
   - Explain the use of conditional statements and loops in Python. Provide examples of an `if-else` statement and a `for` loop.

      =>
      Conditional statements in Python allow you to execute certain blocks of code based on whether a condition is true or false. The primary conditional statements are if, elif, and else.
      
      example
      # Example of if-else statement
      age = 20

      if age >= 18:
         print("You are an adult.")
      else:
         print("You are a minor.")

      Loops are used to execute a block of code repeatedly. The two main types of loops in Python are for loops and while loops.

      # Example of for loop
      fruits = ["apple", "banana", "cherry"]

      for fruit in fruits:
         print(fruit)



6. Functions in Python:
   - What are functions in Python, and why are they useful? Write a Python function that takes two arguments and returns their sum. Include an example of how to call this function.

   => Functions in Python are reusable blocks of code designed to perform a specific task. They allow you to break down complex problems into smaller, manageable pieces, making your code more modular, readable, and easier to maintain.

   def add_numbers(a, b):
    return a + b

   result = add_numbers(5, 3)
   print(f"The sum of 5 and 3 is: {result}")

7. Lists and Dictionaries:
   - Describe the differences between lists and dictionaries in Python. Write a script that creates a list of numbers and a dictionary with some key-value pairs, then demonstrates basic operations on both.

   List: An ordered collection of items, which can be of different types, and is indexed by integers starting from 0.

   my_list = [1, 2, 3, 4, 5]

   Dictionary: An unordered collection of key-value pairs, where each key is unique and is used to access its corresponding value.

   my_dict = {'name': 'Alice', 'age': 25, 'city': 'New York'}

8. Exception Handling:
   - What is exception handling in Python? Provide an example of how to use `try`, `except`, and `finally` blocks to handle errors in a Python script.

   =>Exception handling in Python is a mechanism to handle errors that occur during the execution of a program. It allows a program to continue running or to gracefully handle errors without crashing. 

   example

   def divide_numbers(a, b):
    try:
        result = a / b
    except ZeroDivisionError as e:
        print(f"Error: Cannot divide by zero. Exception: {e}")
        result = None
    except TypeError as e:
        print(f"Error: Invalid input type. Exception: {e}")
        result = None
    else:
        print("Division successful!")
    finally:
        print("Execution of the divide_numbers function is complete.")
    return result


9. Modules and Packages:
   - Explain the concepts of modules and packages in Python. How can you import and use a module in your script? Provide an example using the `math` module.

   => A module in Python is a file containing Python code. This code can define functions, classes, and variables.

   example
   import math

   number = 25
   sqrt_value = math.sqrt(number)

   print(f"The square root of {number} is: {sqrt_value}")


10. File I/O:
    - How do you read from and write to files in Python? Write a script that reads the content of a file and prints it to the console, and another script that writes a list of strings to a file.

    To read from a file in Python, you typically follow these steps:

    Open the File: Use the open() function with the file path and mode ('r' for reading).
    Read from the File: Use methods like read(), readline(), or readlines() to read the content.
    Close the File: Always close the file using the close() method to free up system resources.

         file_path = 'sample.txt'  # Replace with your file path
      try:
         file = open(file_path, 'r')

         # Read the entire content of the file
         file_content = file.read()

         # Print the content to the console
         print("Content of the file:")
         print(file_content)

      except FileNotFoundError:
         print(f"Error: The file '{file_path}' was not found.")
      except IOError:
         print(f"Error: Could not read from the file '{file_path}'.")
      finally:
         # Close the file to release resources
         if 'file' in locals() and not file.closed:
            file.close()


# Submission Guidelines:
- Your answers should be well-structured, concise, and to the point.
- Provide code snippets or complete scripts where applicable.
- Cite any references or sources you use in your answers.
- Submit your completed assignment by [due date].


