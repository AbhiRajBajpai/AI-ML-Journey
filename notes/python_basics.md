# 🐍 Python Basics – Complete Notes

A beginner-friendly, structured guide to Python fundamentals.  
These notes document my learning journey in **Python**, serving as a quick reference for anyone starting out.

---

## 1️⃣ Introduction to Python
- High-level, interpreted, dynamically typed language.
- Beginner-friendly, widely used in AI, ML, Web Dev, Data Science.
- No need to compile; code runs line by line.
- File extension: `.py`

👉 Run Python file:  
```bash
python filename.py

2️⃣ Variables & Data Types

#Variables
#Containers for storing data.
#No need to declare type explicitly.


x = 10        # integer
name = "Abhi" # string
pi = 3.14     # float
is_active = True  # boolean


Data Types

Numeric → int, float, complex

Text → str

Boolean → True / False

Sequence → list, tuple, range

Mapping → dict

Set → set, frozenset



## 🖼️ Python Data Types Hierarchy

flowchart TD
    A[Python Data Types] --> B[Numeric]
    A --> C[Text]
    A --> D[Boolean]
    A --> E[Sequence]
    A --> F[Set]
    A --> G[Mapping]

    B --> B1[int]
    B --> B2[float]
    B --> B3[complex]

    C --> C1[str]

    D --> D1[True/False]

    E --> E1[list]
    E --> E2[tuple]
    E --> E3[range]

    F --> F1[set]
    F --> F2[frozenset]

    G --> G1[dict]


👉 Check type:

print(type(x))


3️⃣ Type Casting

# Convert between data types

x = "10"
y = int(x)    # string → integer
z = float(y)  # integer → float

print(type(x), type(y), type(z))

4️⃣ Comments & Docstrings

# This is a single-line comment

"""
This is a multi-line comment
or docstring. 
Useful for explaining code.
"""

def add(a, b):
    """Returns the sum of two numbers."""
    return a + b

5️⃣ Input & Output

name = input("Enter your name: ")  # takes string input
print("Hello", name)               # output

6️⃣ Operators
Arithmetic
+, -, *, /, // (floor div), % (mod), ** (power)

Comparison
==, !=, >, <, >=, <=

Logical
and, or, not

Assignment
=, +=, -=, *=, /=

7️⃣ Strings

s = "Python"
print(s[0])      # P
print(s[-1])     # n
print(len(s))    # 6
print(s.upper()) # "PYTHON"
print(s.lower()) # "python"
print(s[0:3])    # "Pyt"


👉 String formatting:

name = "Abhi"
age = 22
print(f"My name is {name}, I am {age} years old.")

8️⃣ Lists
#Ordered, mutable collection.

fruits = ["apple", "banana", "mango"]
fruits.append("orange")
fruits.remove("banana")
print(fruits[0])     # apple
print(fruits[-1])    # orange

9️⃣ Tuples
#Ordered, immutable collection.

coordinates = (10, 20)
print(coordinates[0])

🔟 Sets
#Unordered, no duplicates.

nums = {1, 2, 3, 2}
print(nums)   # {1, 2, 3}

1️⃣1️⃣ Dictionaries
#Key-Value pairs.

student = {"name": "Abhi", "age": 22}
print(student["name"])
student["age"] = 23

1️⃣2️⃣ Conditional Statements

x = 10
if x > 0:
    print("Positive")
elif x == 0:
    print("Zero")
else:
    print("Negative")

1️⃣3️⃣ Loops

For Loop

for i in range(5):
    print(i)

While Loop

count = 0
while count < 5:
    print(count)
    count += 1

1️⃣4️⃣ Special Keywords

for i in range(5):
    if i == 2:
        continue   # skips iteration
    if i == 4:
        break      # exits loop
    print(i)

def todo():
    pass  # placeholder for future code

1️⃣5️⃣ Functions

def greet(name):
    return f"Hello {name}"

print(greet("Abhi"))

👉 Default arguments:

def add(a, b=5):
    return a + b

1️⃣6️⃣ Global vs Local Variables

x = 10  # global

def func():
    x = 5  # local
    print("Inside function:", x)

func()
print("Outside function:", x)
👉 Use global keyword if you want to modify global variables inside a function.

1️⃣7️⃣ Exception Handling

try:
    x = int("abc")
except ValueError:
    print("Invalid number")
finally:
    print("Done")

1️⃣8️⃣ File Handling

# Write
with open("data.txt", "w") as f:
    f.write("Hello Python")

# Read
with open("data.txt", "r") as f:
    print(f.read())

1️⃣9️⃣ Iterators & Generators

nums = [1, 2, 3]
it = iter(nums)

print(next(it))  # 1
print(next(it))  # 2
print(next(it))  # 3

# Generator
def squares(n):
    for i in range(n):
        yield i**2

for val in squares(5):
    print(val)

2️⃣0️⃣ With Statement (Context Manager)

with open("file.txt", "w") as f:
    f.write("Hello Python")
# No need to explicitly close file

2️⃣1️⃣ Modules & Packages

import math
print(math.sqrt(16))  # 4.0
👉 Installing external modules:

bash

pip install module_name

2️⃣2️⃣ Object-Oriented Basics

class Student:
    def __init__(self, name):
        self.name = name
    
    def greet(self):
        print(f"Hi, I am {self.name}")

s1 = Student("Abhi")
s1.greet()

2️⃣3️⃣ Pythonic Features

List Comprehension

squares = [x**2 for x in range(5)]

Lambda Functions

add = lambda a, b: a + b
print(add(2, 3))

Map, Filter, Reduce

nums = [1, 2, 3, 4]
doubled = list(map(lambda x: x*2, nums))

2️⃣4️⃣ Virtual Environments

bash

# Create venv
python -m venv myenv

# Activate venv (Windows)
myenv\Scripts\activate

# Activate venv (Linux/Mac)
source myenv/bin/activate

# Deactivate
deactivate



## 🖼️ Python Workflow Diagram

```mermaid
flowchart LR
    A[👩 User Input] -->|input()| B[📥 Python Program]
    B --> C[⚙️ Processing<br>(Logic, Loops, Functions)]
    C --> D[📤 Output<br>(print, files, return)]



🎯 Conclusion
These are the complete Python basics that form the foundation for Data Science, Machine Learning, and AI.
I’ll keep updating this repository as I learn advanced topics. 🚀


