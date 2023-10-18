# Python Basics Course for C Programmers
![image](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/40px-Python-logo-notext.svg.png)
## Table of Contents
- [Python Introduction: Why Choose Python?](#python-introduction-why-choose-python)
- [Installing Python](#installing-python)
- [Your First Python Program](#your-first-python-program)
- [General Python Concepts](#general-python-concepts)
- [Python Data Structures](#python-data-structures)
- [Existing Python Functions](#existing-python-functions)
- [Introduction to PIP](#introduction-to-pip)
- [Build a "Guess the Number" Game](#build-a-guess-the-number-game)
- [Using Python to Fetch Data from an API](#using-python-to-fetch-data-from-an-api)

---

## Python Introduction: Why Choose Python?
Python, with its simple and readable syntax, is one of the most popular programming languages today. It's versatile, powerful, and ideal for various applications from web development to data analysis.
- **History:** Python was created in the late 1980s by Guido van Rossum.
- **Philosophy:** Emphasizes readability, simplicity, and the idea that there should be one best way to do something. Refer to [Zen of Python](https://www.python.org/dev/peps/pep-0020/).
- **Versatility:** Python has a vast ecosystem, making it suitable for web, data science, AI, automation, and more.
- Quick video to understand : 
  ![image](https://img.youtube.com/vi/x7X9w_GIm1s/mqdefault.jpg)
  https://youtu.be/x7X9w_GIm1s?si=vYAXNmqsY-bp1EDx

## Installing Python
1. Visit the official [Python website](https://www.python.org/downloads/) to download the latest version.
2. Follow installation instructions for your specific operating system.
3. Verify the installation by typing `python --version` in your terminal.

## Your First Python Program
Python scripts typically end in a `.py` extension.
```python
print("Hello, World!")
```
There are multiple ways to run a Python script:

### Using the Python Interpreter Directly:
Run a script by using the `python` command followed by the `.py` file name.
```bash
python hello_world.py
```

### Through Shebang (`#!`) on Unix-like Systems:
You can make your Python script executable and invoke the interpreter in the script itself.
First, add the following line to the top of your `.py` file:
```bash
#!/usr/bin/env python3
```
Then, make your script executable:
```bash
chmod +x hello_world.py
```
Run the script:
```bash
./hello_world.py
```
**Exercise:** Write and execute a simple script that prints your name using both methods described above.

## Understanding How Python Works
Python is an interpreted language, which means it directly executes the code line-by-line. When executing, the Python interpreter translates each line into bytecode, which is a lower-level, platform-independent representation of the source code. Then, this bytecode is executed by the Python virtual machine (PVM).

Here's an illustration of the Python execution process:
![Python Execution Process](https://www.datasciencecentral.com/wp-content/uploads/2021/10/8784089862.jpeg)

This means that Python does not need to be compiled before it is run, unlike languages like C.

**Exercise:** Research another programming language and compare its execution process with Python's. How are they similar or different?


## General Python Concepts
- **Variables:** Unlike C, no need to declare variable type. Python is dynamically typed.
  ```python
  name = "Link"
  Life = 30
  ```
- **Syntax:** Indentation is crucial. It determines code blocks.
- **Control Structures:** Use loops and conditions to control the flow of your program.
  ```python
  if life > 0:
      print("Alive ❤️")
  else:
      print("Dead 💀")
  ```
**Exercise:** Write a program that takes an age input from the user and categorizes them into "Minor," "Adult," or "Senior" (age > 60).

## Python Data Structures
- **Lists:** Dynamic arrays. Access, append, insert, and remove elements.
  ```python
  fruits = ["apple", "banana", "cherry"]
  ```
  For more, refer to the [Python documentation on lists](https://docs.python.org/3/tutorial/introduction.html#lists).
  
- **Tuples:** Immutable sequences. Useful when data shouldn't change.
  ```python
  colors = ("red", "green", "blue")
  ```
  **Exercise:** Create a list of your favorite movies and then add another movie to this list. Create a tuple containing your top 3 vacation destinations.


## Existing Python Functions
Python comes with built-in functions to facilitate common operations.
- `print()`: Display content.
- `input()`: Get user input.
- `len()`: Determine the length of an item.
  
Explore more in the [Python documentation](https://docs.python.org/3/library/functions.html).



**Exercise:** Write a program that takes a sentence input from the user and counts how many words are in the sentence.

## Introduction to PIP
PIP is Python's package manager. It helps you install third-party libraries and dependencies.
![pip explainations](https://files.realpython.com/media/What-is-PIP_Watermarked.4944e95d83ad.jpg)
- To install a package:
  ```bash
  pip install package-name
  ```
- For example, to add colors to your terminal, you can use the [colorama](https://pypi.org/project/colorama/) package. Install it via:
  ```bash
  pip install colorama
  ```
**Exercise:** Install another popular Python library of your choice and display its version.

## Build a "Guess the Number" Game
Using Python's `random` module, you can generate random numbers and have the user guess them.
```python
import random

number = random.randint(1, 10)
guess = int(input("Guess a number between 1 and 10: "))

if guess == number:
    print("You guessed it!")
else:
    print(f"Wrong! The number was {number}.")
```
**Exercise:** Enhance the game. If the user's guess is wrong, provide a hint if their guess was too high or too low.

## Using Python to Fetch Data from an API
Python's `requests` module allows you to easily fetch data from APIs.
```python
import requests

response = requests.get("https://api.example.com/data")
data = response.json()
print(data)
```
Note: Ensure you've installed the `requests` package using PIP.
**Exercise:** Fetch data from another public API of your choice and display some relevant information in the terminal.

## Final Exercise: Cat Image Viewer

Combine what you've learned to fetch cat images from an API, store them in a list, and display them in the terminal using a PIP library.

Steps:
1. Fetch cat images from a cat image API.
2. Store the image URLs in a list.
3. Use a PIP library to display the images in the terminal.

Here's a hint to get you started:
```python
import requests

# Fetch cat images
response = requests.get("https://api.thecatapi.com/v1/images/search?limit=4")
data = response.json()

# Extract image URLs
image_urls = [img["url"] for img in data]

# Display images in the terminal (using a suitable PIP library)
# ...

```
You'll need to research a PIP library that allows displaying images in the terminal and integrate it into the code above.

---

End of course overview. Always consult the official [Python documentation](https://docs.python.org/3/) for a deeper understanding of any topic. Happy coding!
