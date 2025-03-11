# Control Flow and Conditionals in Python

## Topics Covered

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


