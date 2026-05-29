# 🐍 Python Notes

> Personal study notes covering the fundamentals of Python programming.

---

## 📚 Table of Contents

1. [Introduction to Python](#1-introduction-to-python)
   - [What is the Python Software Foundation?](#what-is-the-python-software-foundation)
   - [Uses of Python](#uses-of-python)
   - [Installation](#installation)
   - [Ways to Run Python](#ways-to-run-python)
2. [Output — The `print()` Function](#2-output--the-print-function)
   - [Basic Usage](#basic-usage)
   - [Print Function Syntax & Parameters](#print-function-syntax--parameters)
   - [sep Parameter](#sep-parameter)
   - [end Parameter](#end-parameter)
   - [String Concatenation](#string-concatenation)
   - [Challenges](#challenges-output)
3. [Input — The `input()` Function](#3-input--the-input-function)
   - [Input Syntax](#input-syntax)
   - [Storing Input in a Variable](#storing-input-in-a-variable)
   - [New Line Character](#new-line-character)
   - [Type Conversion Functions](#type-conversion-functions)
   - [Mathematical Operators in Python](#mathematical-operators-in-python)
   - [The `round()` Function](#the-round-function)
   - [Challenges](#challenges-input)
4. [Strings](#4-strings)
   - [Multi-line Strings](#multi-line-strings)
   - [Escape Characters](#escape-characters)
   - [Challenges](#challenges-strings)

---

## 1. Introduction to Python

- Developed by **Guido van Rossum**
- Currently managed by the **Python Software Foundation (PSF)**
- Python is a **case-sensitive** language
- Has two major versions: **Python 2.x** and **Python 3.x**
  - Python 2.x is now **discontinued**
  - Code written in Python 2.x will **not** run in Python 3.x

### What is the Python Software Foundation?

The PSF is a non-profit corporation that:
- Holds the intellectual property rights behind the Python programming language
- Manages open source licensing for Python versions
- Owns and protects Python-related trademarks
- Runs the North American **PyCon** conference annually
- Supports Python conferences worldwide and funds Python-related development through grants

### Uses of Python

| Domain | Details |
|---|---|
| **Web Development** | Frameworks: Django, Flask, Pylons, Web2py. Sites like Mozilla, Reddit, and Instagram are built with Python. |
| **Computer Graphics** | GUIs, desktop applications, game development. Libraries: Tkinter, TK, wxPython, Jython, Pygame |
| **Data Science / AI** | Machine learning, data analysis, automation |

### Installation

- Download from [python.org](https://www.python.org)
- During setup, check **"Add Python to PATH"** (recommended)
- You can choose **Install Now** (default) or **Customize installation**

**Check your Python version in Command Prompt / Terminal:**

```bash
python -V
# or
python --version
```

### Ways to Run Python

| Method | Tools |
|---|---|
| **Terminal / CMD** | Interactive shell, Terminal, Editor |
| **IDLE** | Built-in shell + editor that comes with Python |
| **IDEs** | PyCharm, Spyder, Atom, Jupyter Notebook, etc. |
| **Virtual Lab / Online Judge** | HackerRank and similar platforms |

#### Interactive Mode

Python provides a **Python Interactive Shell** (also called REPL — Read, Evaluate, Print, Loop). You can launch it by typing `python` in your terminal. It lets you run Python code line by line immediately.

---

## 2. Output — The `print()` Function

### Basic Usage

In Python 3, `print` was changed from a **statement** (Python 2) to a **function** (Python 3). You must always enclose the values inside round parentheses `()`.

```python
print("This is Python 3 print function")
print(s)       # prints the value of variable s
print(5)       # prints the integer 5
```

The `print()` function can accept **any number of values**, separated by commas:

```python
a = 3.14
b = "age"
c = 32
print("a = ", a, b, c)
# Output: a =  3.14 age 32
```

### Print Function Syntax & Parameters

```python
print(value/values, sep=' ', end='\n', file=sys.stdout, flush=False)
```

| Parameter | Default | Description |
|---|---|---|
| `value/values` | *(required)* | One or more values to print. Can be strings, integers, floats, variables, expressions, lists, etc. |
| `sep` | `' '` (single space) | Separator inserted **between** values when multiple values are passed |
| `end` | `'\n'` (newline) | String appended **after** the last value is printed |
| `file` | `sys.stdout` | The output stream (usually the console) |
| `flush` | `False` | Whether to forcibly flush the stream |

> [!NOTE]
> All parameters except `value/values` are **optional** because they have default values.

---

### sep Parameter

`sep` stands for **separator**. Its default value is a single blank space `' '`, which is why a space automatically appears between values separated by commas in `print()`.

```python
# Using sep's default value
print(1, 2, 3, 4)
# Output: 1 2 3 4

# Using a custom sep value
print(1, 2, 3, 4, sep=':')
# Output: 1:2:3:4
```

> [!IMPORTANT]
> `sep` only works when **at least 2 values** are passed to `print()`. If you pass only one value, the separator has nothing to sit between and will have no effect.
>
> ```python
> print("Hello", sep="#")
> # Output: Hello     ← sep="#" has no effect here (only 1 value)
>
> print("Hello", 2, sep="#")
> # Output: Hello#2   ← sep="#" works because there are 2 values
> ```

---

### end Parameter

`end` controls what is printed **after** the last value. Its default is `'\n'` (a newline character), which is why consecutive `print()` calls each appear on a new line.

```python
print("Hello")
print("World")
# Output:
# Hello
# World
```

This is different from C, where:
```c
printf("Hello");
printf("World");
// Output: HelloWorld  (no automatic newline)
```

In Python, `print("Hello")` is internally treated as `print("Hello\n")` due to the default `end='\n'`.

**Custom `end` example — print on same line:**
```python
for i in range(1, 10):
    print(i, end=' ')
# Output: 1 2 3 4 5 6 7 8 9
```

> [!TIP]
> When `"Hello"+"World"` is used inside `print()`, it is treated as **one single value** (string concatenation happens first), so `sep` will not apply:
> ```python
> print("Hello" + "World", sep="\n", end="#")
> # Output: HelloWorld#   ← sep has no effect; end="#" replaces the newline
> ```

---

### String Concatenation

The `+` operator joins (concatenates) strings together.

```python
print("Hello" + "World")
# Output: HelloWorld
```

> [!NOTE]
> Unlike the comma `,` in `print()`, the `+` operator does **not** add a space between strings. The result is joined directly.

---

### Challenges (Output)

**Challenge 1:** Print `1 2 3 4 5 6 7 8 9` on a single line.

```python
# ❌ Wrong approach — prints each number on a new line
for i in range(1, 10):
    print(i)

# ❌ Also wrong — sep only works with 2+ values; here only 1 value is passed each loop
for i in range(1, 10):
    print(i, sep=" ")

# ✅ Correct — use end=' ' to prevent the default newline
for i in range(1, 10):
    print(i, end=' ')
# Output: 1 2 3 4 5 6 7 8 9
```

**Challenge 2:** Ask the user for a number `x` and print `x, 2x, 3x, 4x, 5x` separated by `---`.

```
Input Format  : Enter a number
Constraints   : 0 < n < 10^8
Output Format : 7---14---21---28---35
```

```python
n = int(input('Enter a number: '))
print(n, n*2, n*3, n*4, n*5, sep='---')

# Example:
# Enter a number: 5
# Output: 5---10---15---20---25
```

---

## 3. Input — The `input()` Function

Programs need input from various sources: keyboard, mouse, database, another computer, or the internet. Since the keyboard is the most common, Python provides the `input()` function.

### Input Syntax

```python
input(prompt)
```

- `input` is the function name — every function uses parentheses `()`
- `prompt` is the optional message displayed to the user before they type their data
- Once `input()` is called, the program **pauses** until the user enters something and presses Enter
- The `input()` function **always returns the user's input as a string**, regardless of what the user types

```python
name = input("May I know your name? ")
print("It's a pleasure to meet you " + name + "!")

age = input("Your age, please? ")
print("So, you're " + age + " years old, " + name + "!")
```

> [!NOTE]
> Notice the blank space before the closing `"` in the prompt strings (e.g., `"May I know your name? "`). This adds a space between the prompt and what the user types, making it readable.

---

### Storing Input in a Variable

```python
name = input('Enter your name : ')
print('hello I am', name)

# Output:
# Enter your name : Sujal
# hello I am Sujal
```

> [!NOTE]
> The comma `,` in `print('hello I am', name)` automatically adds a space before `name`. So even though there is no space after `"am"` inside the string, the output shows `hello I am Sujal` with a proper space.

> [!IMPORTANT]
> **All input is stored as a string.** Whether the user types `4`, `3.14`, or `True`, Python stores it as `"4"`, `"3.14"`, or `"True"`. Use type conversion functions (see below) to convert them.

---

### New Line Character

`\n` is the **new line character**. It can be used inside the `input()` prompt to move the cursor to the next line before the user types.

```python
# Without \n — user types on the same line as the prompt
input('Enter your name : ')
# Output: Enter your name : ____

# With \n — user types on the line below the prompt
input('Enter your name : \n')
# Output:
# Enter your name :
# ____
```

---

### Type Conversion Functions

In C, format specifiers like `%d`, `%s`, `%f` define what type of input to accept — but if the wrong type is entered, **the program crashes**. Python solves this by always reading input as a string and letting you convert it explicitly.

| Function | Converts to | Example |
|---|---|---|
| `int()` | Integer | `int("4")` → `4` |
| `float()` | Float | `float("3.14")` → `3.14` |
| `complex()` | Complex number | `complex("2+3j")` → `(2+3j)` |

```python
# Long way
n = input('Enter any Integer: ')
x = int(n)

# Short way — wrap input() inside int()
n = int(input('Enter any Integer: '))

# Even shorter — do the multiplication inline
n = 2 * int(input('Enter any Integer: '))
# or with extra clarity:
n = 2 * (int(input('Enter any Integer: ')))
```

> [!TIP]
> You can nest `input()` inside a conversion function. Whatever the user types will be immediately converted to the desired type and stored in the variable.

---

### Mathematical Operators in Python

| Operation | Python Symbol | Example |
|---|---|---|
| Addition | `+` | `5 + 3` → `8` |
| Subtraction | `-` | `5 - 3` → `2` |
| Multiplication | `*` | `5 * 3` → `15` |
| Division | `/` | `6 / 3` → `2.0` |
| Exponentiation (Power) | `**` | `2 ** 3` → `8` |

> [!NOTE]
> `/` is the **division symbol** (e.g., `6/3`).
> `\` is the **backslash** and is used as an escape character — it is **not** a division symbol.

---

### The `round()` Function

```python
round(number, ndigits=None)
```

- If `ndigits` is omitted (default is `None`), rounds to the nearest whole number
- If `ndigits` is specified, rounds to that many decimal places

```python
n = 5.55555
round(n)      # Output: 6  (no decimals, ndigits defaults to None)
round(n, 2)   # Output: 5.56
```

> [!TIP]
> If you don't know the syntax of a built-in function, use `help()` in the IDLE shell or terminal:
> ```python
> help(round)
> help(input)
> ```
> Functions like `input()`, `print()`, and `round()` are part of Python's **built-ins module** and are available by default — no import needed.

---

### Challenges (Input)

**Challenge 1:** Accept an integer from the user and print double the value.

```
Input Format  : Enter any Integer: 4
Constraints   : 0 < n < 10^8
Output Format : Double = 8
```

```python
# ❌ Wrong — input is stored as a string, so n*2 repeats the string
n = input('Enter any Integer: ')
d = n * 2
print('Double =', d)
# Enter any Integer: 4
# Output: Double = 44  ← '4' repeated twice, not 4+4

# ✅ Correct — convert input to int first
n = int(input('Enter any Integer: '))
d = n * 2
print('Double =', d)
# Enter any Integer: 4
# Output: Double = 8
```

**Challenge 2:** Find the power of a number.

```
Input Format  : Enter Base: 2
               Enter Exponent: 3
Output Format : 2 power 3 is 8
```

```python
base = int(input('Enter Base: '))
exp = int(input('Enter Exponent: '))
print(base, 'power', exp, 'is', base ** exp)
# Output: 2 power 3 is 8
```

**Challenge 3:** Calculate the volume of a sphere. Formula: `V = (4/3) × π × r³`

```
Input Format  : Input radius
Constraints   : Print volume up to 3 decimals
Output Format : Print volume of a sphere
```

```python
# ❌ Approximate — uses 3.14 instead of the exact value of Pi
r = int(input())
v = 4/3 * 3.14 * r**3
print('Volume of a sphere with radius', r, 'is', round(v, 3))

# ✅ Correct — import math to get the precise value of Pi
import math
r = int(input())
v = 4/3 * math.pi * r**3
print('Volume of a sphere with radius', r, 'is', round(v, 3))
```

> [!NOTE]
> `import math` can be placed on **any line** of the file — it does not have to be at the top. However, it must appear **before** you use `math.pi` or any other `math` function.
>
> The exact value of `math.pi` is: `3.141592653589793`

---

## 4. Strings

A **string** is a sequence of characters enclosed in quotes. Python supports:

| Quote Style | Usage |
|---|---|
| `'single quotes'` | Single-line strings |
| `"double quotes"` | Single-line strings |
| `'''triple single quotes'''` | Multi-line strings |
| `"""triple double quotes"""` | Multi-line strings |

### Multi-line Strings

Single and double quotes can only be used on **one line**. For strings that span multiple lines (like an address), use **triple quotes**.

```python
# ❌ Wrong — single/double quotes cannot span multiple lines
address = 'Nepal
Butwal - 07'

# ✅ Correct — use triple quotes for multi-line strings
addr = '''Nepal, Butwal
Near Golpark'''
print(addr)

# Output:
# Nepal, Butwal
# Near Golpark
```

---

### Escape Characters

The **backslash** `\` is the escape character. It tells Python: *"don't treat the character that follows as a special character — print it literally."*

> [!NOTE]
> This technique is common in languages like **Java** and **C** because they don't support triple quotes.

| Escape Sequence | Meaning |
|---|---|
| `\'` | Literal single quote `'` |
| `\"` | Literal double quote `"` |
| `\\` | Literal backslash `\` |
| `\n` | New line |
| `\t` | Tab |

```python
print("Didnt Hamlet say \"To be or not to be\"?")
# Output: Didnt Hamlet say "To be or not to be"?
```

---

### Challenges (Strings)

**Challenge 1:** Print the following string:
```
Didn't Hamlet say To be or not to be?
```
```python
print("Didn't Hamlet say To be or not to be?")
# Use double quotes on the outside since the string contains a single quote (apostrophe)
```

**Challenge 2:** Print the following string:
```
Didnt Hamlet say "To be or not to be"?
```
```python
# Option 1 — use single quotes on the outside since the string contains double quotes
print('Didnt Hamlet say "To be or not to be"?')

# Option 2 — use escape characters
print("Didnt Hamlet say \"To be or not to be\"?")
```

**Challenge 3:** Print the following string (contains both `'` and `"`):
```
Didn't Hamlet say "To be or not to be"?
```
```python
# Use triple quotes — they can contain both single and double quotes inside
print('''Didn't Hamlet say "To be or not to be"?''')
```

> [!TIP]
> **Rule of thumb for quote selection:**
> - String contains `'` → wrap in `"double quotes"`
> - String contains `"` → wrap in `'single quotes'`
> - String contains both `'` and `"` → use `'''triple quotes'''`
> - Alternatively, you can always use escape characters `\'` or `\"`

---

*Notes compiled from Python beginner lectures. Happy coding! 🚀*
