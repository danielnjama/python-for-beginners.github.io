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

### 12. Create a Python script that imports your custom module and uses its functions to perform calculations.

```python
# main_script.py
import math_operations

print(math_operations.add(5, 3))
print(math_operations.multiply(4, 2))
```

---

### 13. Create a Python module (math\_operations.py) containing functions for addition, subtraction, multiplication, and division. Import this module and use its functions.

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


# 6. Exception Handling


# 7. python Libraries and Modules


# 8. Date and Time