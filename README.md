# 1. Introduction to Python
Python is a high-level, interpreted, and general-purpose programming language known for its simplicity and readability. It has a wide range of applications:
1. **Web Development**: Django, Pyramid, Bottle, Tornado, Flask, web2py
2. **GUI Development**: tkInter, PyGObject, PyQt, PySide, Kivy, wxPython
3. **Scientific and Numeric**: SciPy, Pandas, IPython
4. **Software Development**: Buildbot, Trac, Roundup
5. **System Administration**: Ansible, Salt, OpenStack, xonsh

## 1.1 History and Overview of Python
Python was created by Guido van Rossum and first released in 1991. It is designed with an emphasis on code readability, and its syntax allows programmers to express concepts in fewer lines of code than languages like C++ or Java.

Example: Python's simple and readable syntax:

```python
#Hello World in Python
print("Hello, World!")
```

## 1.2 Installing Python and Setting up an IDE
Installing Python is a straightforward process, and there are different methods depending on your operating system. Below are the general steps for installing Python on Windows, macOS, and Linux.

**Windows:**
1. Download Python:
- Visit the official Python website: [Python Downloads.](https://www.python.org/downloads/)
- Click on the "Downloads" tab, and choose the latest version of Python (e.g., Python 3.9.7) for Windows.
- Select the executable installer suitable for your system architecture (32-bit or 64-bit).
2. Run the Installer:
- Run the downloaded installer executable.
- Check the box that says "Add Python x.x to PATH" during installation. This makes it easier to run Python from the command line.
3. Install Python:
- Click "Install Now" to start the installation process.
- The installer will install Python and related tools.
4. Verify Installation:
- Open a command prompt (CMD) or PowerShell and run the following to check if Python is installed and the version number.
```
python --version
or
python -V
```
**macOS:**
1. Homebrew (Recommended):
- Open Terminal.
- Install Homebrew (if not installed):
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
- Install Python:
```
brew install python
```
2. Verify Installation:
```
python3 --version
or
python3 -V
```

**Linux (Ubuntu/Debian as an example):**
1. Update Package List:
- Open Terminal and run the following:
```
sudo apt update
```
  
2. Install Python:
   
```
sudo apt install python3
```

4. Verify Installation by checking the version:

```
python3 --version
OR
python3 -V
```

You can choose to use Integrated Development Environments (IDEs) such as PyCharm, Visual Studio Code, the default text editor or simply work with Python on command line.

Example: Installing Python and running a simple script in a command prompt:

```bash
# Check if Python is installed
python --version

# Create a Python script (e.g., hello.py)
print("Hello from Python!")

# Run the script
python hello.py
````
## 1.3 Running Python Programs
Python programs can be executed in different ways, including the command line and using an IDE.

Example: Running a Python program on the command line. There are 2 ways to achieve this:
1. Launch the Python interpreter application. This provides an interface where you can write Python codes.
2. Launch your computer's command prompt/terminal and type in python3 or just python and press enter.

   Then input the commands as below. 

```python
a = 5

b = 10

result = a + b
print(result)
```
## 1.4 Basic Syntax and Data Types
Python supports various data types like integers, floats, strings, lists, dictionaries, and more. It also has simple and clear syntax rules.

Example: Working with basic data types:

```Python
# Integer('int'):: Whole numbers without any decimal point
age = 25

# Float('float'):: Numbers with a decimal point or in exponential form like 3.14, -0.001, 2.5e2
price = 19.99

# String('str')::A sequence of characters enclosed within single, double, or triple quotes
name = "John Doe"

# List('list')::Ordered collection of items, mutable(can be modified after creation) and enclosed within square brackets
fruits = ['apple', 'banana', 'cherry']

# Dictionary('dict')::Collection of key-value pairs, enclosed within curly braces
person = {'name': 'Alice', 'age': 30}

# Boolean
This takes True or False
eg: isPositive = True
# Tuple (tuple): Similar to lists but immutable( can't be modified after creation), enclosed within parentheses
fruits = ('apple', 'banana', 'cherry')
# Set (set):: Unordered collection of unique items, enclosed within curly braces or created using the set() function,
nums = {1, 2, 3}
```
*Exercises/Projects:*

1. Create a program that calculates the area of a rectangle and a circle. Ask the user for input and provide the results.
2. Write a simple Python program that prints "Hello, World!" to the console. Run the program and verify that it works as expected.
3. Write a Python program that converts temperatures between Celsius and Fahrenheit. Allow the user to input the temperature and the scale they are using (C or F), and then perform the conversion.
4. Build a simple calculator application in Python that can perform basic arithmetic operations (addition, subtraction, multiplication, division) based on user input. Ensure that the application handles user errors gracefully.





# 2.Variables and Data Structures

## 2.1 Variables and Naming Conventions
In Python, variables are used to store data. They must follow certain naming conventions, such as starting with a letter or underscore and consisting of letters, digits, and underscores.
### The do's and don'ts in naming Python variables
1. **Use Descriptive Names:** Choose variable names that clearly indicate the purpose or meaning of the variable. Make your variable names self-explanatory.
```python
# Good
total_price = 100.0

# Avoid
x = 100.0
```
2. **Follow Naming Conventions:** Adhere to Python's naming conventions, such as using lowercase letters for variable names (snake_case), CamelCase for class names, and UPPERCASE_SNAKE_CASE for constants.
```python
# Good
user_age = 25
class MyClass:
    # Class definition
PI = 3.14159

# Avoid
UserAge = 25
class my_class:
    # Class definition
pi = 3.14159
```
3. **Use Meaningful Names for Functions:** Function names should clearly describe what the function does. Avoid using single-letter or cryptic function names.
```python
# Good
def calculate_area(length, width):
    # Function body

# Avoid
def f(x, y):
    # Function body
```
4. **Avoid Using Reserved Words:** Do not use Python's reserved words or keywords as variable names. Reserved words include if, for, while, and so on.
```python
# Avoid
if = 5
```
5. **Make Use of Comments:** If a variable name alone is not sufficient to explain its purpose, use comments to provide additional context.
```python
total_cost = 100  # Total cost in dollars
```
6. **Avoid Single-Letter Variable Names:** Except for loop iterators (e.g., i, j, k), avoid using single-letter variable names. Single-letter variables are typically not descriptive.
```python
# Avoid
x = 10
y = "Alice"
```
7. **Don't Use Meaningless Names:** Avoid using names that do not convey any meaning or context about the variable's purpose.
```python
# Avoid
temp = 42
result = calculate()
```
8. **Avoid Excessive Abbreviations:** While concise names are good, excessive use of abbreviations can make your code less readable. Balance between brevity and clarity.
```python
# Avoid
usr_nm = "Alice"
```
9. **Don't Mix Different Naming Styles:** Stick to a consistent naming style throughout your code. Mixing styles can make your code inconsistent and harder to read
```python
# Avoid
userAge = 25
total_cost = 100
```
10. **Don't Use Inconsistent Capitalization:** Variable names should not differ only in capitalization, as it can lead to confusion.
```python
# Avoid
myVariable = 42
myvariable = "Hello"
```
12. **Don't Use Names That Clash with Built-in Functions:** Avoid naming variables with names that are already used as built-in functions or standard library functions. It can lead to unexpected behavior.
```python
# Avoid
sum = 10  # Overriding the built-in sum function
```


Example: Declaring and using variables with naming conventions:

```python
my_variable = 42
user_name = "Alice"
_total_count = 100
```
## 2.2 Numbers, Strings, Lists, Tuples, and Dictionaries
Python supports various data structures, including:

1. Numbers (integers, floats)
2. Strings (text)
3. Lists (ordered collections)
4. Tuples (immutable collections)
5. Dictionaries (key-value pairs)
6. Boolean - Takes in True or False

   
Example: Working with different data structures:

```python
# Numbers
integer_num = 42
float_num = 3.14

# Strings
text = "Hello, World!"

# Lists
fruits = ['apple', 'banana', 'cherry']

# Tuples
coordinates = (10, 20)

# Dictionaries
person = {'name': 'Alice', 'age': 30}
```
## 2.3 Working with Data Structures
You can manipulate and operate on data structures, such as adding, removing, or accessing elements within them.

# String Operations 

## **1. Introduction to Strings**
A **string** in Python is a sequence of characters enclosed in **single (`'`), double (`"`), or triple (`'''` or """) quotes**.

```python
text = "Hello, Python!"
print(text)
```

---

## **2. Common String Methods**

### **2.1 Changing Case**
- `upper()`: Converts all characters to **uppercase**
- `lower()`: Converts all characters to **lowercase**
- `title()`: Converts the first letter of each word to uppercase
- `capitalize()`: Converts only the first character to uppercase

```python
text = "hello world"
print(text.upper())      # HELLO WORLD
print(text.lower())      # hello world
print(text.title())      # Hello World
print(text.capitalize()) # Hello world
```

---

### **2.2 String Manipulation**
- `strip()`: Removes leading and trailing spaces
- `lstrip()`: Removes spaces from the left
- `rstrip()`: Removes spaces from the right
- `replace(old, new)`: Replaces occurrences of `old` with `new`

```python
text = "  Python is fun!  "
print(text.strip())   # "Python is fun!"
print(text.lstrip())  # "Python is fun!  "
print(text.rstrip())  # "  Python is fun!"
print(text.replace("fun", "awesome"))  # "  Python is awesome!  "
```

---

### **2.3 Checking and Finding Strings**
- `startswith(substring)`: Checks if a string starts with a given substring
- `endswith(substring)`: Checks if a string ends with a given substring
- `find(substring)`: Returns the index of the first occurrence of the substring (-1 if not found)
- `count(substring)`: Counts the occurrences of a substring

```python
text = "Hello, Python! Python is great."
print(text.startswith("Hello"))  # True
print(text.endswith("great."))   # True
print(text.find("Python"))       # 7 (first occurrence index)
print(text.count("Python"))      # 2
```

---

### **2.4 Splitting and Joining Strings**
- `split(separator)`: Splits a string into a list based on a separator
- `join(iterable)`: Joins a list of strings into a single string

```python
text = "apple,banana,orange"
fruits = text.split(",")  # ['apple', 'banana', 'orange']
print(fruits)

words = ["Python", "is", "awesome"]
sentence = " ".join(words)  # "Python is awesome"
print(sentence)
```

---

### **2.5 String Formatting**
- Using `format()`
- Using f-strings (Recommended)

```python
name = "Alice"
age = 25

# Using format()
print("My name is {} and I am {} years old.".format(name, age))

# Using f-strings (Python 3.6+)
print(f"My name is {name} and I am {age} years old.")
```

---

### **2.6 Checking for Alphanumeric Characters**
- `isalpha()`: Checks if the string contains only letters
- `isdigit()`: Checks if the string contains only digits
- `isalnum()`: Checks if the string contains only letters and digits

```python
text = "Python123"
print(text.isalpha())  # False (contains numbers)
print(text.isdigit())  # False (contains letters)
print(text.isalnum())  # True (only letters and digits)
```

---

## **3. String Indexing and Slicing**
- **Indexing** allows access to individual characters: `text[index]`
- **Slicing** allows extracting a portion of a string: `text[start:end:step]`

```python
text = "Python"
print(text[0])     # 'P'
print(text[-1])    # 'n' (last character)
print(text[0:4])   # 'Pyth' (from index 0 to 3)
print(text[::-1])  # 'nohtyP' (reverse the string)
```

---

## **4. Escape Characters**
- `\n`: New line
- `\t`: Tab space
- `\"`: Double quote
- `\'`: Single quote
- `\\`: Backslash

```python
text = "Hello\nWorld!"
print(text)
```
**Output:**
```
Hello
World!
```

---



## List Operations
```python
# Initialize a list
numbers = [1, 2, 3, 4, 5]

# Adding elements
numbers.append(6)  # Adds 6 to the end of the list
numbers.insert(2, 10)  # Inserts 10 at index 2
numbers.extend([7,9,10])  #Inserts(extends) a new list to the existing one
numbers + [10,20,30]      #Adds 2 or more list to form a single list.

# Removing elements
numbers.pop()  # Removes and returns the last element
numbers.pop(3)  #Removes and returns the element on index 3
numbers.remove(3)  # Removes the first occurrence of 3
del numbers[1]   # Deletes element at index 1

# Accessing elements
first_element = numbers[0]  # Access the first element
second_element = numbers[-1]  # Access the last element
range_of_elements = numbers[0:5]   #Access a list of elements from index 0 then nth-1 index, in this case index 4.

# Find Elements
index_of_10 = numbers.index(10)  # Finds index of first occurrence of 10
count_of_2 = numbers.count(2)  # Counts occurrences of 2


# Initialize a list
colors = ['red', 'green', 'blue']

# Modifying elements
colors[0] = 'yellow'  # Modifies the first element to 'yellow'
colors[1:3] = ['orange', 'purple']  # Replaces elements at index 1 and 2 with 'orange' and 'purple'

# Concatenating lists
more_colors = ['pink', 'brown']
all_colors = colors + more_colors  # Concatenates two lists

# Slicing lists
first_two = colors[:2]  # Retrieves the first two elements
last_two = colors[-2:]  # Retrieves the last two elements


# Length of a list
num_colors = len(colors)  # Returns the number of elements in the list

# Sorting lists
sorted_colors = sorted(colors)  # Returns a new list with elements sorted in ascending order
colors.sort()  # Sorts the list in place, ie colors will have updated to a list of sorted elements

# Reversing lists
reversed_colors = list(reversed(colors))  # Returns a new list with elements in reversed order
colors.reverse()  # Reverses the list in place
colors.sort(reverse=True) # Sorts in descending order
colors.reverse()  # Reverses the list


#Copying a List

new_color_list = colors.copy() # Creates a copy of the list

# Clearing lists
colors.clear()  # Removes all elements from the list
```

## Dictionary Operations

```python

# Define a dictionary
person = {'name': 'John', 'age': 30, 'city': 'New York'}

# Accessing values
name = person['name']  # Access the value associated with the 'name' key. 
age = person.get('age')  # Access the value associated with the 'age' key using get method

### Get method doesnt return an error incase the given key does not exist. The first method does!


# Adding or updating key-value pairs
person['email'] = 'john@example.com'  # Adds a new key 'email' with value 'john@example.com' or updates the existing email key with the new value.
person.update({'age': 31, 'city': 'San Francisco'})  # Updates existing keys 'age' and 'city' or adds new keys and values.

# Removing key-value pairs
del person['city']  # Removes the key 'city' and its associated value
age = person.pop('age')  # Removes the key 'age' and returns its associated value
person.popitem()    #removes the last inserted item

# Accessing keys and values
keys = person.keys()  # Returns a view object of all keys in the dictionary
values = person.values()  # Returns a view object of all values in the dictionary
items = person.items()  # Returns a view object of all key-value pairs in the dictionary

# Checking existence of keys
has_name = 'name' in person  # Checks if 'name' key exists in the dictionary
has_email = 'email' not in person  # Checks if 'email' key does not exist in the dictionary

# Iterating over keys, values, or items
for key in person:
    print(key)  # Prints each key in the dictionary

for value in person.values():
    print(value)  # Prints each value in the dictionary

for key, value in person.items():
    print(key, value)  # Prints each key-value pair in the dictionary

# Copying a Dictionary
new_person = person.copy()   #Creates a copy of the existing dictionary


# Clearing a Dictionary
person.clear()    #Clears the content of the dictionary
```

## 2.4 Type Conversion and Type-checking
Python allows you to convert between different data types and perform type-checking to ensure that a variable is of the expected type.

Example: Type conversion and type-checking:

```python
# Type conversion
num_str = str(42)
float_num = float("3.14")

# Type-checking
if isinstance(num_str, str):
    print("It's a string.")
else:
    print("It's not a string.")
```
# Python Data Types Assignments

## Assignment 1: List Operations
### **Task 1: Basic List Operations**
1. Create a list of 10 numbers ranging from 0 to 20, ensuring that at least 3 numbers appear more than once.
2. Find the maximum and minimum numbers from the list.
3. Sort the list in ascending and descending order.
4. Remove duplicate numbers from the list.
5. Write a program to merge two lists without duplicates.
6. Calculates their mean, median, and mode, and displays the results.

---

## Assignment 2: Tuple Operations
### **Task 2: Tuple Manipulation**
1. Create a tuple with at least 5 elements.
2. Convert the tuple into a list and add a new element.
3. Convert the modified list back into a tuple.
4. Write a program to check if a given element exists in a tuple.
5. Count how many times an element appears in a tuple.

---

## Assignment 3: Dictionary Operations
### **Task 3: Dictionary Manipulation**
1. Create a dictionary with the following key-value pairs:
   ```python
   student = {"name": "John", "age": 20, "grade": "A", "subject": "Math"}
   ```
2. Add a new key-value pair (`"city": "New York"`) to the dictionary.
3. Update the `"age"` key by increasing its value by 1.
4. Remove the `"grade"` key from the dictionary.


---

## Assignment 4: String Manipulations
### **Task 4: String Processing**
1. Write a program to:
   - Take a string as input and print it.
   - Print it in reverse order.
   - Convert the string into **uppercase** and **lowercase**.
   - Remove all spaces from the string.
   - Replace all occurrences of `"Python"` with `"Java"` in a given string.(Identify any string and repalce its occurence with a string of choice)

---



# 3.Control Flow and Conditionals

## Topics Covered

### 3.0 Comparison and Relational Operators
Before diving into conditionals, it's important to understand comparison and relational operators. These operators are used to compare values and return `True` or `False` based on the condition.

| Operator | Description | Example | Output |
|----------|-------------|---------|--------|
| `==` | Equal to | `5 == 5` | `True` |
| `!=` | Not equal to | `5 != 3` | `True` |
| `>` | Greater than | `7 > 4` | `True` |
| `<` | Less than | `3 < 8` | `True` |
| `>=` | Greater than or equal to | `6 >= 6` | `True` |
| `<=` | Less than or equal to | `2 <= 5` | `True` |

### 3.1 If Statements
The `if` statement is used to execute a block of code only if a specified condition is true.

**Example:**
```python
age = 18
if age >= 18:
    print("You are eligible to vote.")
```

### 3.2 Else and Elif Statements
The `else` statement provides an alternative execution path if the `if` condition is false. The `elif` statement allows checking multiple conditions.

**Example:**
```python
score = 75
if score >= 90:
    print("Excellent")
elif score >= 50:
    print("Good job")
else:
    print("Needs improvement")
```

### 3.3 Loops (for, while)
Loops allow repetitive execution of a block of code. The `for` loop is commonly used for iterating over sequences, while the `while` loop continues execution as long as a condition is true.

**Example (`for` loop):**
```python
for i in range(5):
    print(i)
```

**Example (`while` loop):**
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

### 3.4 Iterating through Lists and Dictionaries
Lists and dictionaries can be iterated over using loops to process each element.

**Example (List):**
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

**Example (Dictionary):**
```python
students = {"Alice": 85, "Bob": 72, "Charlie": 90}
for name, grade in students.items():
    print(f"{name}: {grade}")
```

### 3.5 Break and Continue Statements
The `break` statement exits a loop prematurely, while the `continue` statement skips the current iteration and moves to the next one.

**Example (`break`):**
```python
for num in range(10):
    if num == 5:
        break
    print(num)
```

**Example (`continue`):**
```python
for num in range(10):
    if num % 2 == 0:
        continue
    print(num)
```

### 3.6 Nested Conditionals
A conditional statement inside another conditional statement is called a nested conditional.

**Example:**
```python
age = 20
if age >= 18:
    if age >= 65:
        print("You are a senior citizen.")
    else:
        print("You are an adult.")
```

### 3.7 Logical Operators (`and`, `or`, `not`)
Logical operators are used to combine multiple conditions.

**Example:**
```python
age = 25
has_id = True
if age >= 18 and has_id:
    print("You can enter the club.")
```

### 3.8 Loop Control Statements (`pass` statement)
The `pass` statement is used when a statement is required syntactically but no code needs to be executed.

**Example:**
```python
for num in range(5):
    if num == 3:
        pass  # Placeholder for future code
    print(num)
```

### 3.9 Using `else` with Loops
The `else` block executes after the loop finishes, unless the loop is exited with `break`.

**Example:**
```python
for num in range(5):
    print(num)
else:
    print("Loop completed successfully.")
```



## Exercise Questions

### 1. Checking Even or Odd Number
Write a Python program that checks if a given number is even or odd using conditional statements.

**Example Input:**
```python
number = 7
```
**Expected Output:**
```text
7 is an odd number.
```

### 2. Print First 10 Prime Numbers
Create a script that prints the first 10 prime numbers.

**Expected Output:**
```text
2 3 5 7 11 13 17 19 23 29
```

### 3. Exam Pass or Fail
Develop a script that determines whether a student has passed or failed an exam based on their score. Assume the passing mark is 50.


### 4. Categorizing Temperature
Create a program that categorizes a given temperature as `Hot`, `Moderate`, or `Cold` based on user-defined thresholds.


### 5. Sum of Numbers in a Range
Write a Python program that uses a `for` loop to calculate the sum of numbers in a given range.


### 6. Iterating Through a Dictionary of Students
Create a script that iterates through a dictionary of student names and their corresponding grades, displaying a message for each student's performance.

**Example Dictionary:**
```python
students = {"Alice": 85, "Bob": 72, "Charlie": 90, "David": 45}
```
**Expected Output:**
```text
Alice: Excellent!
Bob: Good job!
Charlie: Outstanding!
David: Needs Improvement.
```

## Additional Practice Questions

### 7. Finding the Largest Number
Write a program that takes three numbers as input and determines the largest using conditional statements.

### 8. Number Guessing Game
Create a simple number guessing game where the user has to guess a number between 1 and 20. Use a `while` loop to allow multiple attempts until the user guesses correctly.

### 9. Multiplication Table
Write a Python script that prints the multiplication table for a user-defined number up to 10.

### 10. Using `break` and `continue`
- Write a program that prints numbers from 1 to 10, but stops at 6 using the `break` statement.
- Modify the program to skip even numbers using the `continue` statement.



# 4. Functions and Modules

## 4.1 Defining and Calling Functions
Functions are reusable blocks of code that perform specific tasks. You can define your own functions using the def keyword and call them to execute the code inside.


Example: Defining and calling a function:

```python
#Without a parameter
def greetings():
    print("Hello there")

# Calling the function
greetings()


#with a parameter
def greet(name):
    print(f"Hello, {name}!")

# Calling the function
greet("Alice")
```
## 4.2 Function Parameters and Return Values
Functions can accept parameters (inputs) and return values (outputs). You can pass data into a function, and it can provide a result back.

Example: Functions with parameters and return values:

```python
def add(a, b):
    result = a + b
    return result

sum_result = add(5, 3)
print(f"Sum: {sum_result}")
```
## 4.3 Scope and Lifetime of Variables
Variables can have different scopes, such as local and global. The scope of a variable determines where it can be accessed.

Example: Local and global variables:

```python
global_var = 10

def my_function():
    local_var = 5
    print(global_var)  # Accessing the global variable
    print(local_var)   # Accessing the local variable

my_function()
print(global_var)  # Accessing the global variable outside the function
```
## 4.4 Creating and Using Modules
Python modules are files containing Python code that can be used in other Python programs. You can create your own modules and import them into your scripts.


Example: Creating and using a module:

mymodule.py (module file):

```python
def greet(name):
    print(f"Hello, {name}!")


import mymodule

mymodule.greet("Bob")

OR

from mymodule import greet
greet('Bob')
```
## Python Functions and Modules - Exercise Questions

## 4.1 Defining and Calling Functions
1. Write a Python function that calculates and returns the square of a given number.
2. Write a function that takes a person's name as input and prints a greeting message.
3. Define a function that takes a number as input and checks if it is even or odd.


## 4.2 Function Parameters and Return Values
5. Develop a function that calculates the area of a rectangle, allowing users to specify the length and width as parameters.
6. Write a function that accepts a temperature in Celsius and returns the equivalent temperature in Fahrenheit.
7. Develop a function that takes a list of numbers and returns the maximum value in the list.
8. Create a function that accepts a string and a number `n`, and returns the string repeated `n` times.
9. Write a function that takes two strings as input and returns a new string that concatenates the two inputs.

## 4.3 Scope and Lifetime of Variables
10. Define a function where a local variable has the same name as a global variable and demonstrate their differences.
11. Write a function that modifies a global variable inside it using the `global` keyword.
12. Create a function that uses a nested function to access a variable defined in the outer function (closure concept).

## 4.4 Creating and Using Modules
13. Create a Python script that imports your custom module and uses its functions to perform calculations.
14. Create a Python module (`math_operations.py`) containing functions for addition, subtraction, multiplication, and division. Import this module and use its functions.
15. Write a module that contains a function to check if a number is prime. Import and use this module in another script.
16. Develop a module (`greetings.py`) that defines a function to greet users based on the time of day (morning, afternoon, evening). Import and test it in a separate script.

---


# 5. File Handling

## 5.1 Reading and Writing Text Files
Python provides built-in functions for reading and writing text files. You can open a file, read its content, and write data to it.


Example: Reading and writing text files:

Reading a text file:

```python
# Open a file for reading
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```
Writing to a text file:

```python
# Open a file for writing. This overwrites all the content!
with open("output.txt", "w") as file:
    file.write("This is a line of text.")
```

### Append Mode ("a"):
This mode adds new content to the end of the file without deleting existing data.
```python
with open("output.txt", "a") as file:
    file.write("\nThis is a new line of text.")

```
### Read and Write Mode ("r+")
This allows reading and writing without deleting existing content. You can control the file pointer to modify specific parts.
```python
with open("output.txt", "r+") as file:
    content = file.read()  # Read existing content
    file.seek(0, 2)  # Move to end of file
    file.write("\nAppending with r+ mode.")
```






# 5.2 Working with Binary Files
Binary files store data in a format that is not human-readable. You can work with binary files, such as images, audio, or data files, using Python.

Example: Working with binary files (e.g., images):

```python
# Read and write binary files
with open("image.jpg", "rb") as binary_file:
    image_data = binary_file.read()

with open("new_image.jpg", "wb") as new_binary_file:
    new_binary_file.write(image_data)
```

## 5.3 File Operations and Error Handling
Python allows you to perform operations like renaming, deleting, or checking if a file exists. Additionally, error handling using try and except blocks is essential when working with files to handle exceptions.

Example: File operations and error handling:

```python
import os

# Check if a file exists
if os.path.exists("example.txt"):
    print("File exists.")

# Rename a file
os.rename("example.txt", "new_example.txt")

# Delete a file
os.remove("new_example.txt")

# Error handling when opening a file
try:
    with open("nonexistent_file.txt", "r") as file:
        content = file.read()
except FileNotFoundError:
    print("File not found.")
```
## 5.4 Using the with Statement (Context Managers)
The with statement is used to ensure that a file is properly closed after usage. It simplifies file handling and eliminates the need to explicitly close files.


Example: Using the with statement:

```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
# File is automatically closed when exiting the `with` block
```
*Exercises/Projects:*

1. Create a program that reads a text file, counts the number of words, and prints the result.
2. Write a script that copies the content of one text file into another file, ensuring that the original file remains unchanged.
3. Develop a program that renames a file based on user input. Allow the user to specify the old and new file names.
4. Build a Python program that searches for specific words or phrases in a text file and displays the line numbers where they occur.
5. Create a simple file management system that allows users to add, delete, and list files in a specific directory.


# 6. Exception Handling

## 6.1 Understanding Exceptions
In Python, exceptions are events that occur during the execution of a program and disrupt its normal flow. Understanding different types of exceptions is the first step in effective exception handling.


Example: Understanding exceptions:

```python
# Example of a division by zero exception
try:
    result = 10 / 0
except ZeroDivisionError as e:
    print(f"Exception: {e}")
```
## 6.2 Handling Exceptions (try, except, finally)
Python provides a mechanism to handle exceptions using try, except, and optionally finally blocks. This allows you to gracefully handle errors and prevent program crashes.


Example: Handling exceptions with try, except, and finally:

```python
try:
    result = 10 / 0
except ZeroDivisionError as e:
    print(f"Exception: {e}")
finally:
    print("Execution completed.")
```
# 6.3 Custom Exception Classes
You can create custom exception classes to handle specific errors in your code. This allows you to provide more context and control over the exception handling.

Example: Creating and using a custom exception class:

```python
class CustomError(Exception):
    def __init__(self, message):
        super().__init__(message)

try:
    raise CustomError("This is a custom exception.")
except CustomError as e:
    print(f"Custom Exception: {e}")
```

# 6.4 Debugging Techniques
Effective debugging techniques help identify and resolve issues in your code. Python provides tools like print statements, debugging modules, and IDEs with debugging support.


Example: Using print statements for debugging:

```python
def divide(a, b):
    result = None
    try:
        result = a / b
    except ZeroDivisionError as e:
        print(f"Exception: {e}")
    print(f"Result: {result}")

divide(10, 0)
```
*Exercises/Projects:*

1. Create a program that takes two numbers from the user and performs a division operation. Implement exception handling to handle division by zero.
2. Develop a script that reads a file and handles the "FileNotFoundError" exception by providing a user-friendly error message.
3. Write a function that takes a list and an index as input. Implement exception handling to ensure the index is valid, and if not, raise a custom "IndexOutOfRange" exception.
4. Build a simple calculator application that can perform basic arithmetic operations (addition, subtraction, multiplication, division). Implement error handling for invalid inputs.
5. Create a custom exception class for a specific application or project, and then write a program that raises and handles that exception.


# 7. Working with Python Libraries and Modules

## 7.1 Introduction to Standard Libraries
Python's standard library contains a wide range of modules and packages that provide useful functionalities. These modules are available by default with your Python installation.


Example: Using standard library modules:

```python
import random

# Generate a random number between 1 and 100
random_number = random.randint(1, 100)
print(random_number)

# Select a random element from a list
my_list = [1, 2, 3, 4, 5]
random_element = random.choice(my_list)
print(random_element)


# Shuffle a list in place
my_list = [1, 2, 3, 4, 5]
random.shuffle(my_list)
print(my_list)



# Select a random sample of elements from a list
my_list = [1, 2, 3, 4, 5]
random_sample = random.sample(my_list, 3)  # Select 3 random elements
print(random_sample)


# Generate a random float within a specified range
random_float = random.uniform(1.5, 2.5)
print(random_float)
```
## 7.2 Working with Built-in Modules (e.g., math, datetime)
Python has several built-in modules for mathematical operations, date and time handling, and more. You can use these modules to simplify your code.


Example: Using built-in modules:

```python
import math
import datetime

# Calculate the square root of a number
sqrt_result = math.sqrt(16)
print(sqrt_result)

# Exponential function (e^x)
exp_result = math.exp(2)
print(exp_result)

# Natural logarithm (base e)
log_result = math.log(8)
print(log_result)

# Logarithm with a specified base
log_base2_result = math.log(8, 2)
print(log_base2_result)


# Square root
sqrt_result = math.sqrt(25)
print(sqrt_result)

# Power (x^y)
power_result = math.pow(2, 3)
print(power_result)

# Alternatively, you can use the ** operator for power
power_result_alt = 2 ** 3
print(power_result_alt)

# Pi and Euler's number (e)
pi_value = math.pi
e_value = math.e

# Get the current date and time
current_time = datetime.datetime.now()
print(current_time)
```
## 7.3 Introduction to Third-Party Libraries (e.g., NumPy, pandas)
Third-party libraries like NumPy, pandas, and many others provide specialized functionalities for data manipulation, scientific computing, and more. You can install and use these libraries in your projects.


Example: Using third-party libraries (assuming you've installed NumPy and pandas):

```python
import numpy as np
import pandas as pd

# Create a NumPy array
array = np.array([1, 2, 3, 4, 5])

# Create a pandas DataFrame
data = {'Name': ['Alice', 'Bob'], 'Age': [25, 30]}
df = pd.DataFrame(data)
print(df)
```
## 7.4 Creating and Importing Custom Modules
You can create your own custom modules to organize and reuse your code. These modules can be imported and used in other Python scripts.


Example: Creating and importing a custom module:

my_module.py (custom module):

```python
def greet(name):
    print(f"Hello, {name}!")

# Importing the custom module in another script
import my_module

my_module.greet("Alice")
```
## 7.5 Installing External Packages with pip
Python's package manager, pip, allows you to easily install external packages and libraries from the Python Package Index (PyPI).

Example: Installing an external package with pip:

```bash
# Install the requests library
pip install requests
```
## 7.6 Virtual Environments
Using virtual environments is essential to manage dependencies and isolate packages for different projects.


Example: Creating and activating a virtual environment (assuming you have virtualenv installed):

```bash
# Create a new virtual environment
virtualenv myenv

# Activate the virtual environment (on Windows)
myenv\Scripts\activate

# Activate the virtual environment (on macOS and Linux)
source myenv/bin/activate

#Once activated, install the packages using pip
```

*Exercises/Projects:*

1. Write a Python program that uses the random module from the Standard Library to generate random numbers.
2. Develop a script that uses the os module to list files in a directory and check their file sizes.
3. Create a Python program that calculates the square root of a number using the math module.
4. Write a script that displays the current date and time using the datetime module.
5. Develop a Python script that uses the NumPy library to perform basic array operations (e.g., addition, multiplication).
6. What is the purpose of a requirements.txt file, and how can it be used to manage project dependencies?
7. Create a requirements.txt file that lists the packages required for a sample project.  



# 8. Working with Dates and Times

## 8.1 Python's datetime Module
Python's datetime module provides classes for working with dates and times. You can use it to create, manipulate, and display date and time information.


Example: Working with dates and times using the datetime module:

```python
from datetime import datetime

# Get the current date and time
current_datetime = datetime.now()
print(current_datetime)

# Create a specific date and time
custom_datetime = datetime(2023, 11, 6, 14, 30)
print(custom_datetime)

# Parse a string to a datetime object
date_string = "2023-11-15 08:30:00"
parsed_datetime = datetime.strptime(date_string, "%Y-%m-%d %H:%M:%S")
print("Parsed Datetime:", parsed_datetime)


# Calculate future dates
current_datetime = datetime.now()
future_datetime = current_datetime + timedelta(days=7)
print("Future Date:", future_datetime)
```
## 8.2 Formatting and Parsing Dates
You can format date and time objects into human-readable strings and parse strings to create date and time objects using format codes.


Example: Formatting and parsing dates:

```python
from datetime import datetime

# Format a date and time as a string
current_datetime = datetime.now()
formatted_date = current_datetime.strftime("%Y-%m-%d %H:%M:%S")
print(formatted_date)

# Parse a string to a date and time object
date_str = "2023-11-06 14:30:00"
parsed_date = datetime.strptime(date_str, "%Y-%m-%d %H:%M:%S")
print(parsed_date)
```
## 8.3 Time Zones and Date Arithmetic
Working with time zones and performing date arithmetic can be crucial for handling time-related data accurately.


Example: Handling time zones and date arithmetic:

```python
from datetime import datetime, timedelta
import pytz  # Requires the pytz library

# Create a datetime object with a specific time zone
tz = pytz.timezone('US/Eastern')
ny_time = datetime.now(tz)

# Perform date arithmetic
one_week_ago = ny_time - timedelta(weeks=1)
print(f"One week ago: {one_week_ago}")
```

## 8.4 Time module
The time module in Python provides functions for working with time, independent of the date. Here are some common use cases and examples of how to use the time module:
```python
import time

# Get the current time in seconds since the epoch
current_time = time.time()
print("Current Time (seconds since epoch):", current_time)

# Pause the execution of the program for a specified number of seconds
print("Start")
time.sleep(3)  # Sleep for 3 seconds
print("End after sleeping for 3 seconds")


# Format the current time
current_time = time.localtime()
formatted_time = time.strftime("%Y-%m-%d %H:%M:%S", current_time)
print("Formatted Time:", formatted_time)


# Measure the time taken for a code block to execute
start_time = time.time()
# Code block to measure
time.sleep(2)
end_time = time.time()

elapsed_time = end_time - start_time
print("Elapsed Time:", elapsed_time, "seconds")


# Measure clock time
start_clock = time.time()
time.sleep(2)
end_clock = time.time()

# Measure process time
start_process = time.process_time()
time.sleep(2)
end_process = time.process_time()

print("Clock Time:", end_clock - start_clock, "seconds")
print("Process Time:", end_process - start_process, "seconds")

```
*Exercises/Projects:*

1. Create a Python script that calculates the number of days remaining until a specific date (e.g., a birthday) and displays it to the user.
2. Write a program that converts between different time zones. Allow the user to input a date and time, and then convert it to another time zone.
3. Build a simple world clock application that displays the current time.
4. Create a script that calculates the difference in hours and minutes between two timestamps (e.g., for tracking meeting durations).


---
---
---
---
---
---
---
---
---
# Python Practice Exercises

## 1. Python Basics

### 1.1 Python Syntax and Comments
1. Write a Python program to print "Hello, World!".
2. Add a comment to the above program explaining what it does.

### 1.2 Variables and Data Types
3. Create a variable `name` and assign your name to it. Print the variable.
4. Create variables `a`, `b`, and `c` with values 10, 20.5, and "Python" respectively. Print their types using `type()`.

### 1.3 Numbers
5. Write a program to add two integers and print the result.
6. Write a program to multiply a float and an integer, then print the result.

### 1.4 Strings
7. Create a string `s = "Python"` and print its length using `len()`.
8. Concatenate two strings `s1 = "Hello"` and `s2 = "World"` and print the result.

### 1.5 Booleans
9. Create two variables `x = True` and `y = False`. Print the result of `x and y`.
10. Print the result of `not x`.

### 1.6 Basic Input and Output
11. Write a program that takes user input for their name and prints "Hello, [Name]!".
12. Write a program that takes two numbers as input and prints their sum.

### 1.7 Type Conversion
13. Convert the string `"123"` to an integer and print it.
14. Convert the integer `456` to a string and print it.

---

## 2. Operators in Python

### 2.1 Arithmetic Operators
15. Write a program to calculate the remainder when 15 is divided by 4 using the modulus operator.
16. Write a program to calculate the square of a number using the exponentiation operator.

### 2.2 Comparison Operators
17. Compare two numbers `a = 10` and `b = 20` using the `>` operator and print the result.
18. Check if two strings `s1 = "Python"` and `s2 = "python"` are equal (case-sensitive).

### 2.3 Assignment Operators
19. Use the `+=` operator to add 5 to a variable `x = 10` and print the result.
20. Use the `*=` operator to multiply a variable `y = 3` by 4 and print the result.

### 2.4 Logical Operators
21. Check if `a = 10` is greater than 5 and less than 20 using logical operators.
22. Check if `b = 0` is not equal to 1 or greater than -1.

### 2.5 Membership and Identity Operators
23. Check if the letter `'a'` is in the string `"Python"` using the `in` operator.
24. Check if two variables `x = [1, 2, 3]` and `y = [1, 2, 3]` are the same object using the `is` operator.

---

## 3. Control Flow

### 3.1 Conditional Statements
25. Write a program to check if a number is positive, negative, or zero.
26. Write a program to check if a year is a leap year.

### 3.2 Loops
27. Write a `for` loop to print numbers from 1 to 10.
28. Write a `while` loop to print numbers from 10 to 1.

### 3.3 Using `break` and `continue`
29. Write a program to print numbers from 1 to 10 but skip the number 5 using `continue`.
30. Write a program to stop printing numbers when reaching 7 using `break`.

### 3.4 Nested Loops and Conditional Statements
31. Write a program to print a multiplication table for numbers 1 to 5 using nested loops.
32. Write a program to find all prime numbers between 1 and 50.

---

## 4. Data Structures in Python

### 4.1 Lists
33. Create a list `numbers = [1, 2, 3, 4, 5]` and print the second element.
34. Add the number 6 to the end of the list `numbers` and print the updated list.

### 4.2 Tuples
35. Create a tuple `t = (1, 2, 3)` and try to change its second element to 5. Observe the result.
36. Convert the tuple `t` to a list and print it.

### 4.3 Dictionaries
37. Create a dictionary `student = {"name": "John", "age": 21}` and print the value of the key `"age"`.
38. Add a new key-value pair `"grade": "A"` to the dictionary `student` and print the updated dictionary.

### 4.4 Working with Strings
39. Convert the string `"Hello World"` to uppercase using `.upper()`.
40. Replace the word `"World"` with `"Python"` in the string `"Hello World"`.

---

## 5. Functions in Python

### 5.1 Defining Functions
41. Write a function `greet()` that prints "Hello, World!".
42. Write a function `add(a, b)` that returns the sum of two numbers.

### 5.2 Function Parameters and Arguments
43. Write a function `multiply(a, b=2)` that multiplies two numbers, with `b` having a default value of 2.
44. Write a function `power(x, y)` that returns `x` raised to the power of `y`.

### 5.3 Return Values
45. Write a function `is_even(n)` that returns `True` if `n` is even, otherwise `False`.
46. Write a function `factorial(n)` that returns the factorial of `n`.

---

## 6. Error and Exception Handling

### 6.1 Using `try`, `except`, and `finally`
47. Write a program to handle a `ZeroDivisionError` when dividing by zero.
48. Write a program to handle a `ValueError` when converting a string to an integer.

### 6.2 Raising Exceptions
49. Write a function `check_positive(n)` that raises a `ValueError` if `n` is negative.
50. Write a program to catch a custom exception and print a message.

---

## 7. Working with Files

### 7.1 Reading from a File
51. Write a program to read a file `example.txt` and print its contents.
52. Write a program to count the number of lines in a file.

### 7.2 Writing to a File
53. Write a program to write "Hello, File!" to a file `output.txt`.
54. Write a program to append "New Line" to an existing file `output.txt`.

### 7.3 File Modes and Exceptions
55. Write a program to handle a `FileNotFoundError` when trying to open a non-existent file.
56. Write a program to read a file in binary mode and print its contents.

---

## 8. Python Modules and Packages

### 8.1 Importing Modules
57. Write a program to use the `math` module to calculate the square root of 16.
58. Write a program to use the `random` module to generate a random number between 1 and 10.

### 8.2 Creating and Using Custom Modules
59. Create a custom module `mymodule.py` with a function `greet()` that prints "Hello from mymodule!". Import and use it in another program.
60. Write a program to install and use an external library like `requests` using `pip`.

---

## Mixed Challenges
61. Write a program to reverse a string without using built-in functions.
62. Write a program to find the largest number in a list.
63. Write a program to count the frequency of each element in a list.
64. Write a program to check if a string is a palindrome.
65. Write a program to sort a dictionary by its values.
66. Write a program to merge two dictionaries.
67. Write a program to find the second largest number in a list.
68. Write a program to remove duplicates from a list.
69. Write a program to find the common elements between two lists.
70. Write a program to calculate the sum of digits of a number.
71. Write a program to check if a number is an Armstrong number.
72. Write a program to generate the Fibonacci sequence up to `n` terms.
73. Write a program to find the factorial of a number using recursion.
74. Write a program to flatten a nested list.
75. Write a program to find the longest word in a sentence.
76. Write a program to count the number of vowels in a string.
77. Write a program to check if two strings are anagrams.
78. Write a program to find the intersection of two sets.
79. Write a program to find the union of two sets.
80. Write a program to find the difference between two sets.
81. Write a program to check if a number is a perfect number.
82. Write a program to find the GCD of two numbers.
83. Write a program to find the LCM of two numbers.
84. Write a program to convert a decimal number to binary.
85. Write a program to convert a binary number to decimal.
86. Write a program to check if a number is a prime number.
87. Write a program to find the sum of all prime numbers between 1 and 100.
88. Write a program to find the sum of all even numbers in a list.
89. Write a program to find the sum of all odd numbers in a list.
90. Write a program to find the average of numbers in a list.
91. Write a program to find the median of numbers in a list.
92. Write a program to find the mode of numbers in a list.
93. Write a program to find the standard deviation of numbers in a list.
94. Write a program to find the variance of numbers in a list.
95. Write a program to find the correlation coefficient between two lists.
96. Write a program to find the covariance between two lists.
97. Write a program to find the Pearson correlation coefficient between two lists.
98. Write a program to find the Spearman correlation coefficient between two lists.
99. Write a program to find the Kendall correlation coefficient between two lists.
100. Write a program to find the rank of a matrix.
