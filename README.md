# 🚀 10 Basic Python Practice Projects (Level 2)

This collection builds on the fundamentals, introducing more complex data structures, logic, and real-world programming concepts. These examples demonstrate the ability to solve practical problems.

---
 
## 1. 🎲 Guess the Number Game
This program introduces the `random` module, `while` loops for repeated guessing, and more complex `if-elif-else` logic.

```python
import random

# Generate a random integer between 1 and 100
secret_number = random.randint(1, 100)
print("I'm thinking of a number between 1 and 100.")

# Infinite loop until the correct number is guessed
while True:
    try:
        guess = int(input("Take a guess: "))

        if guess < secret_number:
            print("Your guess is too low. Try again.")
        elif guess > secret_number:
            print("Your guess is too high. Try again.")
        else:
            # Correct guess ends the game
            print(f"Congratulations! You guessed the number: {secret_number}")
            break
    except ValueError:
        print("Invalid input. Please enter a whole number.")
```
## 2. ➗ Factorial Calculator
This program calculates the factorial of a number using loops.

```Python

#Take input from the user
num = int(input("Enter a non-negative number: "))
factorial = 1

#Handle negative numbers
if num < 0:
    print("Sorry, factorial does not exist for negative numbers.")
elif num == 0:
    # Base case: factorial of 0 is always 1
    print("The factorial of 0 is 1.")
else:
    # Multiply numbers from 1 to n
    for i in range(1, num + 1):
        factorial *= i
    print(f"The factorial of {num} is {factorial}")
```

## 3. ✅ Simple To-Do List (Dictionary-based)
This program demonstrates how to manage tasks with a dictionary.

```Python

# Dictionary to store tasks and their status
tasks = {}

while True:
    action = input("Choose an action (add, show, quit): ").lower()

    if action == "add":
        # Add new task
        task = input("Enter the task: ")
        tasks[task] = "Pending"
        print(f"Task '{task}' added.")

    elif action == "show":
        # Display all tasks
        if not tasks:
            print("Your to-do list is empty.")
        else:
            print("\n--- Your Tasks ---")
            for t, status in tasks.items():
                print(f"{t}: {status}")
            print("------------------\n")

    elif action == "quit":
        # Exit the program
        print("Exiting To-Do List. Goodbye!")
        break
    
    else:
        print("Invalid action. Please choose add, show, or quit.")
```

## 4. 📝 Word Counter
Counts the frequency of words in a sentence.

```Python

import string

# Input a sentence from the user
sentence = input("Enter a sentence: ").lower()

# Remove punctuation
translator = str.maketrans('', '', string.punctuation)
sentence = sentence.translate(translator)

words = sentence.split()

# Dictionary to store word counts
word_count = {}

# Count occurrences of each word
for word in words:
    word_count[word] = word_count.get(word, 0) + 1

print("\n--- Word Frequencies ---")
for w, count in word_count.items():
    print(f"'{w}': {count}")
print("------------------------\n")
```

## 6. 📂 Read & Write to a Text File
Demonstrates basic file I/O operations.

```Python

# Write to a file
with open("sample.txt", "w") as f:
    f.write("Hello, this is a test file.\n")
    f.write("Python file handling is simple!")

print("Data has been written to sample.txt.")

# Read from a file
print("\nReading content from sample.txt:")
with open("sample.txt", "r") as f:
    content = f.read()
    print(content)
```

## 7. 🔄 Palindrome Checker
Checks if a word is the same forwards and backwards.

```Python

# Take input from user
word = input("Enter a word to check if it's a palindrome: ")

# Clean the word (remove spaces and convert to lowercase)
cleaned_word = word.replace(" ", "").lower()

# Compare the cleaned word with its reversed version
if cleaned_word == cleaned_word[::-1]:
    print(f"Yes, '{word}' is a palindrome!")
else:
    print(f"No, '{word}' is not a palindrome.")
```

## 8. 🔐 Password Generator
Creates a random password of a given length.

```Python

import random
import string

# Input password length
length = int(input("Enter the desired password length: "))

# Define the character set
characters = string.ascii_letters + string.digits + string.punctuation

# Randomly pick characters and join them to form the password
password = "".join(random.choice(characters) for _ in range(length))

print("Generated password:", password)
```

## 9. ➕ Basic Calculator (with Functions)
A menu-driven calculator using functions for modularity.

```Python

# Function definitions
def add(x, y): return x + y
def subtract(x, y): return x - y
def multiply(x, y): return x * y
def divide(x, y):
    if y == 0:
        return "Error: Division by zero is not allowed."
    return x / y

print("Select operation:")
print("1. Add")
print("2. Subtract")
print("3. Multiply")
print("4. Divide")

choice = input("Enter choice(1/2/3/4): ")

a = float(input("Enter first number: "))
b = float(input("Enter second number: "))

if choice == '1':
    print(f"Result: {a} + {b} = {add(a, b)}")
elif choice == '2':
    print(f"Result: {a} - {b} = {subtract(a, b)}")
elif choice == '3':
    print(f"Result: {a} * {b} = {multiply(a, b)}")
elif choice == '4':
    print(f"Result: {a} / {b} = {divide(a, b)}")
else:
    print("Invalid choice")
```

## 10. ⚠️ Exception Handling Example
Shows how to handle potential errors gracefully.

```Python

try:
    # Take input and perform division
    numerator = int(input("Enter a numerator: "))
    denominator = int(input("Enter a denominator: "))
    
    result = numerator / denominator
    print("Result:", result)

except ValueError:
    # Handles non-numeric input
    print("Invalid input! Please enter numbers only.")

except ZeroDivisionError:
    # Handles division by zero
    print("Error! Cannot divide by zero.")

finally:
    # This block always runs, regardless of an error
    print("Program execution finished.")
```

# 📚 What You’ll Learn
Using loops, conditionals, and functions effectively.

Applying dictionaries, string methods, and file handling.

Implementing error handling with try...except.

Building logic-driven programs that solve real problems.

# 🤝 Contributing
Feel free to fork this repo, add more intermediate Python programs, and submit a pull request.

# ⭐ Support
If you found this helpful, please star ⭐ the repository to support more projects like this.
