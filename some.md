# Control Flow and Conditionals in Python

## Topics Covered



**Example:**
```python
age = 20
if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```

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

**Example Input:**
```python
score = 67
```
**Expected Output:**
```text
Congratulations! You have passed the exam.
```

### 4. Categorizing Temperature
Create a program that categorizes a given temperature as `Hot`, `Moderate`, or `Cold` based on user-defined thresholds.

**Example Input:**
```python
temperature = 18  # Assume threshold: Cold < 15, Moderate 15-25, Hot > 25
```
**Expected Output:**
```text
The temperature is Moderate.
```

### 5. Sum of Numbers in a Range
Write a Python program that uses a `for` loop to calculate the sum of numbers in a given range.

**Example Input:**
```python
start = 1
end = 10
```
**Expected Output:**
```text
Sum of numbers from 1 to 10 is 55.
```

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

---
These exercises will help reinforce the concepts of control flow and conditional statements in Python. Happy coding!

