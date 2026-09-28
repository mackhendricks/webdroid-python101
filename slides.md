---
theme: default
title: Python 101 - From Zero to Functions
titleTemplate: '%s'
info: |
  # Python 101
  A 3-hour hands-on workshop for beginners.
class: text-center
highlighter: shiki
lineNumbers: true
drawings:
  persist: false
transition: slide-left
mdc: true
---

# Python 101

## From Zero to Functions in 3 Hours

**Learn it. Run it. Change it. Break it. Fix it.**

<div class="mt-10 text-lg opacity-80">
Hands-on beginner workshop • No local Python installation required
</div>

<!--
Welcome everyone. Set expectations: this is a hands-on workshop, not a lecture marathon.
Students will type and run code throughout the session.
-->

---
layout: center
---

# Today's Goal

By the end of this workshop, you will be able to **read, write, run, and modify basic Python programs**.

<div class="mt-10 text-2xl">
🐍 Variables → Data Types → Operators → Functions → Built-ins → Packages
</div>

<!--
Emphasize that mastery is not the goal today. Confidence and a mental model are.
-->

---

# 3-Hour Agenda

| Time | Topic |
|---|---|
| 0:00–0:30 | Introductions • Programming in the age of AI • Why Python |
| 0:30–1:00 | Data Types • Variables • Operators |
| 1:00–1:30 | 🧪 Lab 1: Types, Variables & Operators |
| 1:30–2:00 | Functions • Parameters • Calling Functions |
| 2:00–2:30 | 🧪 Lab 2: Functions |
| 2:30–3:00 | Built-in Functions • Modules • `pip` • What's Next |

---
layout: section
---

# Part 1
## Why Programming? Why Python?

**30 minutes**

---

# Introductions

### Tell us three things

1. **Your name**
2. **What brought you here?**
3. **One thing you'd love to make a computer do for you**

<div class="mt-12 p-5 border rounded-xl text-xl">
There are no “non-technical” answers.
</div>

<!--
Budget ~10 minutes depending on class size. If the room is large, have students pair-share for 3 minutes, then take 4-5 examples.
-->

---

# What Is Programming?

Programming is giving a computer a **precise sequence of instructions**.

```text
INPUT  →  INSTRUCTIONS  →  OUTPUT
```

### Everyday analogy

```text
Ingredients → Recipe → Meal
Data        → Program → Result
```

<v-click>

Computers are extremely fast — but extremely literal.

</v-click>

---

# Why Learn Programming in the Age of AI?

AI can generate code. You still need to know how to:

- Describe the problem clearly
- Recognize whether the output makes sense
- Test what the code actually does
- Debug failures
- Change generated code safely
- Combine small pieces into useful systems

<div class="mt-8 text-2xl font-bold">
AI changes how we program — not the value of understanding programs.
</div>

<!--
Ask: “Would you use a calculator without understanding what + and × mean?”
AI can accelerate a programmer, but the human still needs a model of the problem and enough knowledge to verify the result.
-->

---

# AI as Your Programming Partner

### Good uses

- “Explain this error in beginner language.”
- “Give me a hint, not the answer.”
- “What does this line do?”
- “Create three test cases for this function.”

### Be careful with

- Copying code you don't understand
- Assuming generated code is correct
- Sharing passwords, keys, or private data

<div class="mt-6 p-4 border rounded-xl">
<strong>Workshop rule:</strong> Type, run, inspect, and change the code yourself.
</div>

---

# Why Python?

Python is a general-purpose language used for:

<div class="grid grid-cols-2 gap-5 mt-8 text-xl">
<div class="p-5 border rounded-xl">🤖 AI & Machine Learning</div>
<div class="p-5 border rounded-xl">📊 Data & Analytics</div>
<div class="p-5 border rounded-xl">🌐 Web Applications</div>
<div class="p-5 border rounded-xl">⚙️ Automation</div>
<div class="p-5 border rounded-xl">🔬 Science & Research</div>
<div class="p-5 border rounded-xl">🛠️ DevOps & Scripting</div>
</div>

---

# Your First Python Program

```python {1|2|all}
name = "Python programmer"
print("Hello,", name)
```

### Output

```text
Hello, Python programmer
```

<v-click>

Two lines. Already we have a **variable**, **data**, and a **function call**.

</v-click>

---

# Our Coding Lab

We'll use **Programiz Online Python Compiler** for today's exercises.

### Open

**https://www.programiz.com/python-programming/online-compiler/**

### Workflow

```text
TYPE CODE → RUN → READ OUTPUT → CHANGE CODE → RUN AGAIN
```

<div class="mt-8 p-4 border rounded-xl">
No Python installation is required for today's labs.
</div>

<!--
Have everyone open the compiler now. Confirm the room can run print("Hello!") before moving on.
-->

---
layout: section
---

# Part 2
## Data Types, Variables & Operators

**30 minutes**

---

# Variables: Give Data a Name

```python
name = "Jordan"
age = 22
hourly_rate = 18.50
is_student = True
```

Think of a variable as a **label attached to a value**.

```text
name ─────────► "Jordan"
age  ─────────► 22
```

### Read assignment as

> “Set `age` equal to `22`.”

---

# Variable Naming

```python
first_name = "Jordan"    # good
student_age = 22         # good
hourly_rate = 18.50      # good
```

Avoid:

```python
2name = "Jordan"         # starts with a number
first-name = "Jordan"    # hyphen means subtraction
class = "Python 101"     # reserved keyword
```

### Python convention

Use descriptive **snake_case** names.

---

# Four Data Types to Know Today

| Type | Meaning | Example |
|---|---|---|
| `str` | Text | `"Detroit"` |
| `int` | Whole number | `42` |
| `float` | Decimal number | `19.95` |
| `bool` | True/False | `True` |

```python
city = "Detroit"
students = 20
price = 19.95
class_started = True
```

---

# Ask Python: What Type Is This?

```python
city = "Detroit"
students = 20
price = 19.95
class_started = True

print(type(city))
print(type(students))
print(type(price))
print(type(class_started))
```

### Predict before you run it.

<!--
Use this as a 2-minute micro-exercise. Ask students to predict the four outputs, then run it.
-->

---

# Strings vs Numbers

These look similar to humans — not to Python.

```python
age_number = 25
age_text = "25"
```

```python
print(age_number + 5)  # 30
print(age_text + "5")  # 255
```

<v-click>

Quotes matter. `"25"` is **text**, not a number.

</v-click>

---

# Arithmetic Operators

```python
print(10 + 3)   # addition
print(10 - 3)   # subtraction
print(10 * 3)   # multiplication
print(10 / 3)   # division
print(10 // 3)  # floor division
print(10 % 3)   # remainder
print(10 ** 3)  # exponent
```

### Question

Where might `%` — the remainder operator — be useful?

---

# Operators with Variables

```python
hours = 8
hourly_rate = 20

pay = hours * hourly_rate

print(pay)
```

### Output

```text
160
```

<v-click>

Programming becomes useful when we combine **data + operations**.

</v-click>

---

# Comparison Operators

Comparisons produce a Boolean: `True` or `False`.

```python
age = 21

print(age == 21)  # equal to
print(age != 18)  # not equal to
print(age > 18)   # greater than
print(age < 65)   # less than
print(age >= 21)  # greater than or equal
print(age <= 21)  # less than or equal
```

<div class="mt-5 p-4 border rounded-xl">
`=` assigns a value. &nbsp;&nbsp; `==` compares two values.
</div>

---

# Getting Input from a User

```python
name = input("What is your name? ")
print("Hello,", name)
```

`input()` returns a **string**.

```python
age = int(input("How old are you? "))
print("Next year you will be", age + 1)
```

### New idea: type conversion

`int("25")` → `25`

---

# Mini Challenge

What will this print?

```python
x = 10
y = 4

result = x * 2 + y
print(result)
print(result > 20)
```

<v-click>

```text
24
True
```

</v-click>

---
layout: section
---

# Lab 1
## Types, Variables & Operators

**30 minutes**

---

# 🧪 Lab 1: Personal Budget Calculator

### Goal

Build a small program that calculates money left after expenses.

### Step 1 — Create variables

```python
name = "Mack"
income = 1000.00
rent = 400.00
food = 150.00
transportation = 75.00
```

### Step 2 — Calculate expenses

```python
total_expenses = rent + food + transportation
money_left = income - total_expenses
```

---

# 🧪 Lab 1: Display the Results

Add:

```python
print("Budget for:", name)
print("Income:", income)
print("Expenses:", total_expenses)
print("Money left:", money_left)
```

### Checkpoint

Your program should calculate the result — **don't type the answer directly**.

---

# 🧪 Lab 1: Make It Interactive

Replace some hard-coded values with `input()`.

```python
name = input("Your name: ")
income = float(input("Monthly income: "))
rent = float(input("Rent: "))
food = float(input("Food: "))
```

Then calculate and display the result.

### Why `float()`?

Because `input()` gives us text, but we need numbers for arithmetic.

---

# 🧪 Lab 1: Level Up

If you finish early, add:

```python
savings_rate = (money_left / income) * 100
print("Percent left:", savings_rate)
```

Then answer:

- What happens if income is `0`?
- What happens if expenses exceed income?
- Can you add another expense category?
- Can you make the output easier to read?

<!--
Give students ~18-20 minutes to code. Circulate. Use the remaining time to have 2-3 students share what they changed.
Do not immediately fix errors for them; ask them to read the error and identify the line first.
-->

---

# Lab 1 Debrief

### What did we use?

```text
Variables      → income, rent, food
Data types     → str, float
Operators      → +, -, /, *
Built-ins      → input(), print(), float()
```

### Most important habit

> Change one thing → Run → Observe

---
layout: section
---

# Part 3
## Functions, Parameters & Function Calls

**30 minutes**

---

# Why Functions?

Imagine writing this five times:

```python
print("--------------------")
print("Welcome to Python!")
print("--------------------")
```

A function lets us give reusable instructions a name.

```python
def show_welcome():
    print("--------------------")
    print("Welcome to Python!")
    print("--------------------")
```

---

# Anatomy of a Function

```python {1|2|3|all}
def greet(name):
    message = "Hello, " + name
    return message
```

```text
def        → define a function
greet      → function name
name       → parameter
return     → send a result back
```

### Defining is not the same as calling.

---

# Calling a Function

```python
def greet(name):
    return "Hello, " + name

message = greet("Avery")
print(message)
```

### Follow the data

```text
"Avery" → name → "Hello, Avery" → message → print()
```

---

# Parameters vs Arguments

```python
def greet(name):
    return "Hello, " + name

print(greet("Taylor"))
```

- `name` is a **parameter** — the placeholder in the definition.
- `"Taylor"` is an **argument** — the actual value supplied when calling it.

---

# Multiple Parameters

```python
def calculate_pay(hours, rate):
    pay = hours * rate
    return pay

weekly_pay = calculate_pay(40, 25)
print(weekly_pay)
```

### Predict

What does `calculate_pay(10, 15)` return?

---

# `return` vs `print()`

```python
def add_bad(a, b):
    print(a + b)


def add_good(a, b):
    return a + b
```

`print()` **displays** a value.

`return` gives a value **back to the caller**, so we can keep using it.

```python
total = add_good(10, 5)
final = total * 2
print(final)
```

---

# Functions Can Call Functions

```python
def calculate_subtotal(price, quantity):
    return price * quantity


def calculate_tax(subtotal, tax_rate):
    return subtotal * tax_rate

subtotal = calculate_subtotal(20, 3)
tax = calculate_tax(subtotal, 0.06)

print(subtotal + tax)
```

<div class="mt-6 text-xl">
Big programs are built from small pieces.
</div>

---

# Scope: Inside vs Outside

```python
def greet():
    message = "Hello!"
    print(message)

greet()
```

`message` is created **inside** the function.

```python
print(message)  # NameError
```

### Key idea

Variables created inside a function are normally **local** to that function.

---
layout: section
---

# Lab 2
## Build with Functions

**30 minutes**

---

# 🧪 Lab 2: Tip Calculator

### Goal

Turn a calculation into reusable functions.

Start with:

```python
def calculate_tip(bill, tip_percent):
    tip = bill * (tip_percent / 100)
    return tip
```

Test it:

```python
print(calculate_tip(50, 20))
```

Expected result: `10.0`

---

# 🧪 Lab 2: Add a Total Function

Write this function yourself:

```python
def calculate_total(bill, tip):
    # your code here
```

Then use both functions:

```python
bill = 50
tip = calculate_tip(bill, 20)
total = calculate_total(bill, tip)

print("Tip:", tip)
print("Total:", total)
```

---

# 🧪 Lab 2: Make It Interactive

Ask the user for values:

```python
bill = float(input("Bill amount: "))
tip_percent = float(input("Tip percent: "))
```

Then call your functions.

### Success criteria

Your program should work with **different bill amounts** without changing the function code.

---

# 🧪 Lab 2: Level Up

Choose one challenge:

### A — Split the bill

```python
def split_bill(total, people):
    # return amount per person
```

### B — Add tax

```python
def calculate_tax(amount, tax_rate):
    # return tax amount
```

### C — Friendly summary

Create a function that prints a receipt-like summary.

<!--
Give ~20 minutes for coding, 5 minutes pair review, 5 minutes debrief.
Ask students to test with at least 3 sets of inputs.
-->

---

# Lab 2 Debrief

A function is a small machine:

```text
        arguments
           ↓
   ┌───────────────┐
   │   FUNCTION    │
   │ instructions  │
   └───────────────┘
           ↓
       return value
```

### Ask yourself

**What goes in? What happens? What comes out?**

---
layout: section
---

# Part 4
## Built-in Functions, Modules & `pip`

**30 minutes**

---

# You've Already Used Built-ins

Python comes with useful functions ready to call.

```python
print("Hello")
input("Name: ")
type(42)
int("42")
float("19.95")
str(100)
```

You didn't write these functions.

**Python provides them for you.**

---

# More Useful Built-in Functions

```python
numbers = [8, 3, 12, 5]

print(len(numbers))
print(min(numbers))
print(max(numbers))
print(sum(numbers))
print(sorted(numbers))
```

### Predict the output before running it.

---

# Lists: A Quick Preview

A list stores multiple values.

```python
scores = [85, 92, 78, 95]

print(scores)
print(len(scores))
print(sum(scores))
```

We can combine built-ins:

```python
average = sum(scores) / len(scores)
print(average)
```

---

# Modules: Python's Toolboxes

Python's standard library contains modules you can import.

```python
import random

number = random.randint(1, 10)
print(number)
```

Another example:

```python
import math

print(math.sqrt(81))
```

### `import` makes another toolbox available to your program.

---

# Standard Library vs External Packages

### Standard library

Comes with Python:

```python
import math
import random
import datetime
```

### External packages

Installed separately:

```text
requests
pandas
numpy
flask
```

This is where a package manager becomes useful.

---

# What Is `pip`?

`pip` is Python's commonly used package installer.

In a terminal, you might run:

```bash
python -m pip install requests
```

Then in Python:

```python
import requests
```

### Mental model

```text
PyPI → pip → your Python environment → import package
```

<!--
Explain that the browser compiler used in today's labs is intentionally simple. Package installation varies by online environment, so this is a conceptual demonstration.
-->

---

# Packages Unlock Ecosystems

| Goal | Examples |
|---|---|
| HTTP / APIs | `requests`, `httpx` |
| Data | `pandas`, `numpy` |
| Web apps | `flask`, `fastapi` |
| Testing | `pytest` |
| AI / ML | `transformers`, `torch` |

<div class="mt-8 p-4 border rounded-xl">
Don't memorize package names. Learn to ask: <strong>“Has someone already built a tool for this?”</strong>
</div>

---

# Quick Built-in Challenge

Run this:

```python
scores = [72, 91, 88, 64, 95]

highest = max(scores)
lowest = min(scores)
average = sum(scores) / len(scores)

print("Highest:", highest)
print("Lowest:", lowest)
print("Average:", average)
```

### Change the list and run it again.

What stayed the same? What changed?

---

# Reading Errors Is Programming

```python
print(student_name)
```

```text
NameError: name 'student_name' is not defined
```

Don't read an error as:

> “I can't program.”

Read it as:

> “Python is telling me where my assumptions and the program disagree.”

---

# A Simple Debugging Loop

```text
1. READ the error
       ↓
2. FIND the line
       ↓
3. CHECK names, types, syntax, values
       ↓
4. CHANGE one thing
       ↓
5. RUN again
```

### AI tip

Paste the **error + relevant code**, then ask for an explanation before asking for a fix.

---

# What You Can Do Now

You can:

- Store information in variables
- Recognize common Python data types
- Perform calculations and comparisons
- Get user input
- Define and call functions
- Pass arguments through parameters
- Return values
- Use Python built-in functions
- Import modules
- Explain what `pip` and packages are for

---

# Your Next 7 Days

### Don't just watch tutorials — build tiny programs.

1. Calculator
2. Tip calculator
3. Unit converter
4. Random number game
5. Simple budget calculator
6. Grade calculator
7. Rewrite one project using functions

<div class="mt-8 text-xl font-bold">
15–30 minutes of coding each day beats one giant study session.
</div>

---

# Final Challenge

Can you explain this program to someone else?

```python
def calculate_average(scores):
    return sum(scores) / len(scores)

scores = [90, 82, 95, 88]
average = calculate_average(scores)

print("Average:", average)
```

### If you can explain it, change it, and debug it — you're programming.

---
layout: center
class: text-center
---

# You Wrote Python Today. 🐍

## Keep building.

**Questions?**

<div class="mt-10 opacity-70">
Python 101 • 3-Hour Hands-On Workshop
</div>
