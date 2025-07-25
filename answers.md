# 1. Introduction to python
### 1. Running Python

**Q: How do you start Python in interactive mode?**
A: Open your terminal and type:

```bash
python
```
OR
```python
python3
```

**Q: How do you run a Python script named hello.py from the terminal?**
A:

```bash
python hello.py
```

**Q: What command is used to exit Python interactive mode?**
A: Use either of the following commands:

```python
exit()
```

or press:

```
Ctrl + Z (Windows) or Ctrl + D (Linux/macOS), then press Enter
```

---

### 2. Basic Syntax

**Q: Identify the error in the following code and fix it:**

```python
if 5 > 3:
print("Five is greater than three")
```

**A:** The print statement needs to be indented.

```python
if 5 > 3:
    print("Five is greater than three")
```

**Q: What will be the output of the following code?**

```python
name = "Alice"
age = 25
print("My name is" + name + "and I am" + age + "years old.")
```

**A:** This will raise a `TypeError` because you can't concatenate a string and an integer directly.
**Correct version:**

```python
print("My name is " + name + " and I am " + str(age) + " years old.")
```

**Output:**

```
My name is Alice and I am 25 years old.
```

**Q: What will happen if you don’t use indentation correctly in Python?**
A: Python will raise an `IndentationError`. Indentation is required to define the blocks of code.


# 2. Variables and Data Types

**Q: Create a list of 10 numbers ranging from 0 to 20, ensuring that at least 3 numbers appear more than once.**

```python
numbers = [3, 5, 7, 3, 12, 5, 19, 7, 3, 5]
```

**Q: Find the maximum and minimum numbers from the list.**

```python
print("Max:", max(numbers))
print("Min:", min(numbers))
```

**Q: Sort the list in ascending and descending order.**

```python
print("Ascending:", sorted(numbers))
print("Descending:", sorted(numbers, reverse=True))
```

**Q: Remove duplicate numbers from the list.**

```python
unique_numbers = list(set(numbers))
print("Unique Numbers:", unique_numbers)
```

**Q: Write a program to merge two lists without duplicates.**

```python
list1 = [1, 2, 3, 4]
list2 = [3, 4, 5, 6]
merged_list = list(set(list1 + list2))
print("Merged List:", merged_list)
```

**Q: Calculates their mean, median, and mode, and displays the results.**

```python
import statistics
print("Mean:", statistics.mean(numbers))
print("Median:", statistics.median(numbers))
print("Mode:", statistics.mode(numbers))
```

**Q: Create a tuple with at least 5 elements.**

```python
my_tuple = (10, 20, 30, 40, 50)
```

**Q: Convert the tuple into a list and add a new element.**

```python
tuple_to_list = list(my_tuple)
tuple_to_list.append(60)
```

**Q: Convert the modified list back into a tuple.**

```python
new_tuple = tuple(tuple_to_list)
```

**Q: Write a program to check if a given element exists in a tuple.**

```python
print(30 in my_tuple)
```

**Q: Count how many times an element appears in a tuple.**

```python
print(my_tuple.count(20))
```

**Q: Create a dictionary with key-value pairs.**

```python
student = {"name": "John", "age": 20, "grade": "A", "subject": "Math"}
```

**Q: Add a new key-value pair ("city": "New York") to the dictionary.**

```python
student["city"] = "New York"
```

**Q: Update the "age" key by increasing its value by 1.**

```python
student["age"] += 1
```

**Q: Remove the "grade" key from the dictionary.**

```python
del student["grade"]
```

**Q: Take a string as input and print it.**

```python
text = input("Enter a string: ")
print("You entered:", text)
```

**Q: Print it in reverse order.**

```python
print("Reversed:", text[::-1])
```

**Q: Convert the string into uppercase and lowercase.**

```python
print("Uppercase:", text.upper())
print("Lowercase:", text.lower())
```

**Q: Remove all spaces from the string.**

```python
print("No Spaces:", text.replace(" ", ""))
```

**Q: Replace all occurrences of "Python" with "Java" in a given string.**

```python
sentence = "Python is fun. I love Python!"
print(sentence.replace("Python", "Java"))
```



# 3.Control Flow and Conditionals

1. Checking Even or Odd Number
- Write a Python program that checks if a given number is even or odd using conditional statements.
```python
num = int(input("Enter a number: "))
if num % 2 == 0:
    print(f"{num} is Even")
else:
    print(f"{num} is Odd")
```
2. Print First 10 Prime Numbers
- Create a script that prints the first 10 prime numbers.
```python
count = 0
num = 2
while count < 10:
    for i in range(2, num):
        if num % i == 0:
            break
    else:
        print(num, end=" ")
        count += 1
    num += 1
```
3. Exam Pass or Fail
- Develop a script that determines whether a student has passed or failed an exam based on their score. Assume the passing mark is 50.
```python
score = int(input("Enter your score: "))
if score >= 50:
    print("You passed the exam!")
else:
    print("You failed the exam.")
```
4. Categorizing Temperature
- Create a program that categorizes a given temperature as Hot, Moderate, or Cold based on user-defined thresholds.
```python
temp = float(input("Enter the temperature in °C: "))
if temp >= 30:
    print("Hot")
elif 15 <= temp < 30:
    print("Moderate")
else:
    print("Cold")
```
5. Sum of Numbers in a Range
- Write a Python program that uses a for loop to calculate the sum of numbers in a given range.
```python
start = int(input("Enter start of range: "))
end = int(input("Enter end of range: "))
total = 0
for i in range(start, end + 1):
    total += i
print(f"Sum of numbers from {start} to {end} is {total}")
```

6. Iterating Through a Dictionary of Students
- Create a script that iterates through a dictionary of student names and their corresponding grades, displaying a message for each student's performance.
```python
students = {"Alice": 85, "Bob": 72, "Charlie": 90, "David": 45}

for name, grade in students.items():
    if grade >= 90:
        print(f"{name}: Outstanding!")
    elif grade >= 75:
        print(f"{name}: Excellent!")
    elif grade >= 60:
        print(f"{name}: Good job!")
    else:
        print(f"{name}: Needs Improvement.")

```
7. Finding the Largest Number
- Write a program that takes three numbers as input and determines the largest using conditional statements.
```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
c = int(input("Enter third number: "))

if a >= b and a >= c:
    largest = a
elif b >= a and b >= c:
    largest = b
else:
    largest = c

print(f"The largest number is {largest}")
```
8. Number Guessing Game
- Create a simple number guessing game where the user has to guess a number between 1 and 20. Use a while loop to allow multiple attempts until the user guesses correctly.
```python
import random

secret = random.randint(1, 20)
guess = 0

while guess != secret:
    guess = int(input("Guess a number between 1 and 20: "))
    if guess < secret:
        print("Too low!")
    elif guess > secret:
        print("Too high!")
    else:
        print("Congratulations! You guessed it.")
```
9. Multiplication Table
- Write a Python script that prints the multiplication table for a user-defined number up to 10.
```python
num = int(input("Enter a number to print its multiplication table: "))
for i in range(1, 11):
    print(f"{num} x {i} = {num * i}")
```
10. Using break and continue
- Write a program that prints numbers from 1 to 10, but stops at 6 using the break statement.
(a) Using break
```python
for i in range(1, 11):
    if i == 6:
        break
    print(i)
```
(b) Using continue
- Modify the program to skip even numbers using the continue statement.
```python
for i in range(1, 11):
    if i % 2 == 0:
        continue
    print(i)
```


# 4. Functions and Modules
### 1. Write a Python function that calculates and returns the square of a given number.

```python
def square(num):
    return num ** 2
```

---

### 2. Write a function that takes a person's name as input and prints a greeting message.

```python
def greet(name):
    print(f"Hello, {name}! Welcome.")
```

---

### 3. Define a function that takes a number as input and checks if it is even or odd.

```python
def check_even_odd(num):
    if num % 2 == 0:
        print(f"{num} is Even")
    else:
        print(f"{num} is Odd")
```

---

### 4. Develop a function that calculates the area of a rectangle, allowing users to specify the length and width as parameters.

```python
def area_of_rectangle(length, width):
    return length * width
```

---

### 5. Write a function that accepts a temperature in Celsius and returns the equivalent temperature in Fahrenheit.

```python
def celsius_to_fahrenheit(celsius):
    return (celsius * 9/5) + 32
```

---

### 6. Develop a function that takes a list of numbers and returns the maximum value in the list.

```python
def find_max(numbers):
    return max(numbers)
```

---

### 7. Create a function that accepts a string and a number n, and returns the string repeated n times.

```python
def repeat_string(s, n):
    return s * n
```

---

### 8. Write a function that takes two strings as input and returns a new string that concatenates the two inputs.

```python
def concatenate_strings(str1, str2):
    return str1 + str2
```

---

### 9. Define a function where a local variable has the same name as a global variable and demonstrate their differences.

```python
x = "Global Variable"

def show_variable():
    x = "Local Variable"
    print("Inside function:", x)

show_variable()
print("Outside function:", x)
```

---

### 10. Write a function that modifies a global variable inside it using the global keyword.

```python
count = 0

def increment():
    global count
    count += 1

increment()
print("Global count:", count)
```

---

### 11. Create a function that uses a nested function to access a variable defined in the outer function (closure concept).

```python
def outer_function(msg):
    def inner_function():
        print(f"Message: {msg}")
    return inner_function

greet_func = outer_function("Hello from closure!")
greet_func()
```

---

### 12. Create a Python module (math\_operations.py) containing functions for addition, subtraction, multiplication, and division. Import this module and use its functions.

```python
# math_operations.py
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b != 0:
        return a / b
    else:
        return "Cannot divide by zero"
```

---

### 13. Create a Python script that imports your custom module and uses its functions to perform calculations.

```python
# main_script.py
import math_operations

print(math_operations.add(5, 3))
print(math_operations.multiply(4, 2))
```

---

### 14. Write a module that contains a function to check if a number is prime. Import and use this module in another script.

```python
# prime_checker.py
def is_prime(num):
    if num < 2:
        return False
    for i in range(2, int(num**0.5)+1):
        if num % i == 0:
            return False
    return True
```

```python
# use_prime.py
import prime_checker

print(prime_checker.is_prime(7))  # True
print(prime_checker.is_prime(10)) # False
```

---

### 15. Develop a module (greetings.py) that defines a function to greet users based on the time of day (morning, afternoon, evening). Import and test it in a separate script.

```python
# greetings.py
def greet_by_time(hour):
    if 5 <= hour < 12:
        return "Good morning!"
    elif 12 <= hour < 18:
        return "Good afternoon!"
    elif 18 <= hour < 22:
        return "Good evening!"
    else:
        return "Hello!"
```

```python
# use_greetings.py
import greetings

print(greetings.greet_by_time(10))  # Good morning!
print(greetings.greet_by_time(15))  # Good afternoon!
print(greetings.greet_by_time(20))  # Good evening!
```



# 5. File Handling
**Q: Word Counter: Create a program that reads a text file, counts the number of words, and prints the result.**

```python
with open('sample.txt', 'r') as file:
    text = file.read()
    words = text.split()
    print("Word count:", len(words))
```

**Q: File Copy: Write a script that copies the content of one text file into another file, ensuring that the original file remains unchanged.**

```python
with open('original.txt', 'r') as original:
    content = original.read()

with open('copy.txt', 'w') as copy:
    copy.write(content)
```

**Q: File Renamer: Develop a program that renames a file based on user input.**

```python
import os
old_name = input("Enter the current file name: ")
new_name = input("Enter the new file name: ")
os.rename(old_name, new_name)
```

**Q: Text Search: Build a program that searches for specific words in a text file and displays line numbers where they occur.**

```python
word = input("Enter word to search: ")
with open('sample.txt', 'r') as file:
    for number, line in enumerate(file, 1):
        if word in line:
            print(f"Found in line {number}: {line.strip()}")
```

**Q: File Management System: Allows users to add, delete, and list files in a specific directory.**

```python
import os

def add_file(filename):
    with open(filename, 'w') as f:
        f.write('')

def delete_file(filename):
    os.remove(filename)

def list_files():
    print(os.listdir())
```

**Q: Log File Analyzer: Reads a log file, extracts error messages, and writes them to a separate file.**

```python
with open('log.txt', 'r') as log, open('errors.txt', 'w') as errors:
    for line in log:
        if 'ERROR' in line:
            errors.write(line)
```

**Q: CSV File Reader: Reads a CSV file and displays its content.**

```python
import csv
with open('data.csv', newline='') as csvfile:
    reader = csv.reader(csvfile)
    for row in reader:
        print(', '.join(row))
```

**Q: File Encryption: Encrypts file content using a character shift.**

```python
shift = 3
with open('plain.txt', 'r') as infile, open('encrypted.txt', 'w') as outfile:
    for line in infile:
        encrypted = ''.join(chr(ord(char) + shift) for char in line)
        outfile.write(encrypted)
```

**Q: File Backup Utility: Copies all files from one directory to another.**

```python
import shutil, os
source = 'original_dir'
destination = 'backup_dir'
os.makedirs(destination, exist_ok=True)
for file_name in os.listdir(source):
    full_file_name = os.path.join(source, file_name)
    if os.path.isfile(full_file_name):
        shutil.copy(full_file_name, destination)
```

**Q: File Metadata Extractor: Displays file size and creation date.**

```python
import os, time
for file in os.listdir('.'):
    if os.path.isfile(file):
        print(f"{file}: Size={os.path.getsize(file)} bytes, Created={time.ctime(os.path.getctime(file))}")
```

**Q: File Splitter: Splits a large file into smaller ones by line count.**

```python
def split_file(filename, lines_per_file):
    with open(filename) as f:
        lines = f.readlines()
    for i in range(0, len(lines), lines_per_file):
        with open(f'part_{i//lines_per_file}.txt', 'w') as f_out:
            f_out.writelines(lines[i:i+lines_per_file])
```

**Q: File Merger: Merges multiple text files into one.**

```python
with open('merged.txt', 'w') as outfile:
    for fname in ['file1.txt', 'file2.txt']:
        with open(fname) as infile:
            outfile.write(infile.read() + '\n')
```

**Q: File Compression: Removes extra spaces and newlines.**

```python
with open('original.txt', 'r') as infile, open('compressed.txt', 'w') as outfile:
    for line in infile:
        compressed = ' '.join(line.split())
        outfile.write(compressed)
```

**Q: File Comparison: Compares two files and highlights differences.**

```python
with open('file1.txt') as f1, open('file2.txt') as f2:
    for i, (l1, l2) in enumerate(zip(f1, f2), 1):
        if l1 != l2:
            print(f"Line {i} differs:\nFile1: {l1}File2: {l2}")
```

**Q: File Versioning: Saves versions of a file with timestamps.**

```python
import time, shutil
filename = 'important.txt'
timestamp = time.strftime('%Y%m%d-%H%M%S')
shutil.copy(filename, f"backup_{timestamp}.txt")
```



# 6. Exception Handling

## 1. Division with Exception Handling

```python
try:
    a = float(input("Enter numerator: "))
    b = float(input("Enter denominator: "))
    result = a / b
    print("Result:", result)
except ZeroDivisionError:
    print("Error: Division by zero is not allowed.")
except ValueError:
    print("Error: Invalid input. Please enter numbers.")
```

## 2. File Handling with Exception Handling

```python
try:
    with open("data.txt", "r") as file:
        content = file.read()
        print(content)
except FileNotFoundError:
    print("Error: File not found.")
```

## 3. Index Validation with Custom Exception

```python
class IndexOutOfRange(Exception):
    pass

def access_list(lst,idx):
    try:
        if idx >= len(lst) or idx < -len(lst):
            raise IndexOutOfRange("Index is out of range!")
        else:
            print(lst[idx])
    except IndexOutOfRange:
        print("Index is out of range!")



access_list([2,3,4,5], 4) 
```

## 4. Simple Calculator with Error Handling

```python
try:
    num1 = float(input("Enter first number: "))
    operator = input("Enter operator (+, -, *, /): ")
    num2 = float(input("Enter second number: "))

    if operator == "+":
        print("Result:", num1 + num2)
    elif operator == "-":
        print("Result:", num1 - num2)
    elif operator == "*":
        print("Result:", num1 * num2)
    elif operator == "/":
        print("Result:", num1 / num2)
    else:
        print("Invalid operator")
except ValueError:
    print("Error: Invalid input")
except ZeroDivisionError:
    print("Error: Division by zero")
```

## 5. Custom Exception for a Project

```python
class InvalidOperationError(Exception):
    pass

def perform_operation(op):
    if op not in ["start", "stop", "restart"]:
        raise InvalidOperationError("Unsupported operation.")
    else:
        print(f"Operation '{op}' performed successfully.")

try:
    perform_operation("pause")
except InvalidOperationError as e:
    print(e)
```

## 6. Logging for Debugging

```python
import logging

logging.basicConfig(filename='calculator.log', level=logging.DEBUG)

def calc(a, b, op):
    try:
        if op == "+":
            result = a + b
        elif op == "-":
            result = a - b
        elif op == "*":
            result = a * b
        elif op == "/":
            result = a / b
        else:
            raise ValueError("Invalid operation")
        logging.debug(f"{a} {op} {b} = {result}")
        return result
    except Exception as e:
        logging.error(f"Error occurred: {e}")
        return None

print(calc(10, 0, "/"))
```

## 7. Handling Multiple Exceptions

```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
    print("Result:", result)
except (ValueError, TypeError, ZeroDivisionError) as e:
    print("Error:", e)
```

## 8. Database Connection with Exception Handling

```python
class DatabaseConnectionError(Exception):
    pass

def connect_to_db(status):
    if status == "timeout":
        raise TimeoutError("Connection timed out")
    elif status == "error":
        raise DatabaseConnectionError("Failed to connect to database")
    else:
        print("Connected successfully")

try:
    connect_to_db("error")
except (TimeoutError, DatabaseConnectionError) as e:
    print("Database Error:", e)
```

## 9. Input Validation with Exception Handling

```python
class InvalidAgeError(Exception):
    pass

class InvalidEmailError(Exception):
    pass

def validate_input(age, email):
    if not age.isdigit() or int(age) < 0:
        raise InvalidAgeError("Invalid age provided.")
    if "@" not in email or "." not in email:
        raise InvalidEmailError("Invalid email format.")
    if age and email:
        print(f"{age} : {email}")

try:
    validate_input("twenty", "testemail.com")
except (InvalidAgeError, InvalidEmailError) as e:
    print(e)
```
OR
```python

#Email
class InvalidEmail(Exception):
    pass


def validate_email(email):
    # admin@dtechnologys.com 
    if '@' not in email or '.' not in email:
        raise InvalidEmail("Invalid email!")
    else:
        print(f"OK: {email}")

try:
    validate_email('admin@emailcom')
except InvalidEmail:
    print("Invalid email")

#Age
class InvalidAge(Exception):
    pass

def valid_age(age): #'admin' '10'
    if not str(age).isdigit() or int(age) < 0: #True
        raise InvalidAge("Invalid age")
    else:
        print(f"OK: {age}")
    
try:
    valid_age('12')
except InvalidAge:
    print("Invalid Age!")



```

## 10. Recursive Function with Exception Handling

```python
def factorial(n):
    try:
        if not isinstance(n, int):
            raise TypeError("Input must be an integer.")
        if n < 0:
            raise ValueError("Factorial not defined for negative numbers.")
        if n == 0:
            return 1
        return n * factorial(n - 1)
    except Exception as e:
        print("Error:", e)

print(factorial(-5))
```



# 7. python Libraries and Modules
### 1. Random Number Generator

**Question:** Write a Python program that uses the random module to generate a list of 10 random integers between 1 and 100 and then shuffles the list.

**Answer:**

```python
import random

numbers = [random.randint(1, 100) for _ in range(10)]
random.shuffle(numbers)
print("Shuffled Numbers:", numbers)
```

### 2. File Explorer

**Question:** Develop a script that uses the os module to list all files in a directory and display their sizes in bytes.

**Answer:**

```python
import os

directory = '.'
for filename in os.listdir(directory):
    filepath = os.path.join(directory, filename)
    if os.path.isfile(filepath):
        print(f"{filename}: {os.path.getsize(filepath)} bytes")
```

### 3. Math Operations

**Question:** Create a Python program that uses the math module to calculate the area of a circle given its radius.

**Answer:**

```python
import math

radius = float(input("Enter the radius: "))
area = math.pi * radius ** 2
OR
#area = math.pi * math.pow(radius, 2)
print(f"Area of the circle: {area:.2f}")
```

### 4. Date and Time

**Question:** Write a script that uses the datetime module to display the current date and time in the format YYYY-MM-DD HH\:MM\:SS.

**Answer:**

```python
from datetime import datetime

now = datetime.now()
print(now.strftime("%Y-%m-%d %H:%M:%S"))
```

### 5. NumPy Array Operations

**Question:** Develop a Python script that uses the NumPy library to create two arrays and perform element-wise addition and multiplication.

**Answer:**

```python
import numpy as np

a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

print("Addition:", a + b)
print("Multiplication:", a * b)
```

### 6. Custom Module

**Question:** Create a custom module named calculator.py with functions for addition, subtraction, multiplication, and division. Import and use this module in another script.

**Answer:**
**calculator.py**

```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    return a / b if b != 0 else 'Division by zero error'
```

**main.py**

```python
import calculator

print("Add:", calculator.add(10, 5))
print("Subtract:", calculator.subtract(10, 5))
print("Multiply:", calculator.multiply(10, 5))
print("Divide:", calculator.divide(10, 5))
```

### 7. Dependency Management

**Question:** What is the purpose of a requirements.txt file? Create a requirements.txt file for a project that requires the requests, numpy, and pandas libraries.

**Answer:**

* The `requirements.txt` file lists all the dependencies for a Python project so they can be easily installed using `pip install -r requirements.txt`.

**requirements.txt:**

```
requests
numpy
pandas
```

### 8. Virtual Environment

**Question:** Create a virtual environment for a project and install the flask library. Write a simple Flask application that displays "Hello, World!" when run.

**Answer:**

```sh
python -m venv myenv
source myenv/bin/activate  # or myenv\Scripts\activate on Windows
pip install flask
```

**app.py**

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello():
    return "Hello, World!"

if __name__ == '__main__':
    app.run(debug=True)
```



# 8. Date and Time
### Quiz and Solutions on Date and Time in Python

---

#### - Days Until Birthday
Write a Python script that calculates the number of days remaining until a specific date (e.g., a birthday) and displays it to the user.

```python
from datetime import datetime

birthday = datetime(2025, 12, 25)
now = datetime.now()
difference = birthday - now
print("Days until birthday:", difference.days)
```

#### - Time Zone Converter
Create a program that converts a given date and time from one time zone to another. Allow the user to input the date, time, and time zones.

```python
from datetime import datetime
import pytz

date_str = input("Enter date and time (YYYY-MM-DD HH:MM): ")
from_zone = pytz.timezone(input("Enter source time zone: "))
to_zone = pytz.timezone(input("Enter target time zone: "))

dt = datetime.strptime(date_str, "%Y-%m-%d %H:%M")
dt = from_zone.localize(dt)
converted = dt.astimezone(to_zone)
print("Converted Time:", converted)
```

#### - World Clock
Build a simple world clock application that displays the current time in multiple time zones (e.g., New York, London, Tokyo).

```python
from datetime import datetime
import pytz

zones = ['America/New_York', 'Europe/London', 'Asia/Tokyo']
for zone in zones:
    tz = pytz.timezone(zone)
    time = datetime.now(tz)
    print(f"Time in {zone}: {time.strftime('%Y-%m-%d %H:%M:%S')}")
```

#### - Meeting Duration Calculator
Write a script that calculates the difference in hours and minutes between two timestamps (e.g., for tracking meeting durations).
```python
from datetime import datetime

start = datetime.strptime("2025-06-05 14:00", "%Y-%m-%d %H:%M")
end = datetime.strptime("2025-06-05 15:45", "%Y-%m-%d %H:%M")
duration = end - start
hours, remainder = divmod(duration.seconds, 3600)
minutes = remainder // 60
print(f"Duration: {hours} hours and {minutes} minutes")
```

#### - Age Calculator
Develop a program that calculates a person’s age in years, months, and days based on their birthdate.

```python
from datetime import datetime

birthdate = datetime.strptime("2000-01-01", "%Y-%m-%d")
today = datetime.today()
age_days = (today - birthdate).days
years = age_days // 365
months = (age_days % 365) // 30
days = (age_days % 365) % 30
print(f"Age: {years} years, {months} months, {days} days")
```

#### - Leap Year Checker
Write a function that checks if a given year is a leap year.

Note: A leap year is a year that has 366 days instead of the usual 365 days. The extra day is added to the month of February, making it 29 days long instead of 28.

characteristics of a leap year:
It is divisible by 4,
except for years that are divisible by 100,
unless the year is also divisible by 400.
```python
def is_leap(year):
    return year % 4 == 0 and (year % 100 != 0 or year % 400 == 0)

print(is_leap(2024))
```

#### - Countdown Timer
Create a countdown timer that takes a future date and time as input and displays the remaining time in days, hours, minutes, and seconds.

```python
from datetime import datetime
import time

future = datetime.strptime("2025-06-06 18:00:00", "%Y-%m-%d %H:%M:%S")
while True:
    now = datetime.now()
    remaining = future - now
    if remaining.total_seconds() <= 0:
        print("Countdown complete!")
        break
    print("Remaining:", remaining)
    time.sleep(1)
```

#### - Date Difference
Write a program that calculates the difference between two dates in years, months, and days.

```python
from datetime import datetime
from dateutil.relativedelta import relativedelta

date1 = datetime.strptime("2000-01-01", "%Y-%m-%d")
date2 = datetime.today()
diff = relativedelta(date2, date1)
print(f"Difference: {diff.years} years, {diff.months} months, {diff.days} days")
```

#### - File Timestamps
Use the os and datetime modules to display the creation and modification timestamps of a file.
```python
import os
from datetime import datetime

file_path = "example.txt"
created = os.path.getctime(file_path)
modified = os.path.getmtime(file_path)
print("Created:", datetime.fromtimestamp(created))
print("Modified:", datetime.fromtimestamp(modified))
```

#### - Time-Based Greeting
Write a script that greets the user with "Good Morning," "Good Afternoon," or "Good Evening" based on the current time.

```python
from datetime import datetime

now = datetime.now()
hour = now.hour
if hour < 12:
    greeting = "Good Morning"
elif hour < 18:
    greeting = "Good Afternoon"
else:
    greeting = "Good Evening"
print(greeting)
```
