# Department of Computer Application, S.S.V.P.S. Science College, Dhule
## MCA-416 Lab on Python Programming

---

### 1. Introduction to Python Programming

#### a. Python Step-by-step Installation Process.
1. Open a web browser.
2. Go to www.python.org.
3. Click on Download Python.
4. Open the downloaded setup file.
5. Tick Add Python to PATH.
6. Click Install Now.
7. Wait for installation to finish.
8. Open Command Prompt.
9. Type `python --version` and press Enter. If the version appears, Python is installed successfully.

---

#### b. Implement a program based on strings. (slicing, casting, string function)

```python
# =============================================
# STRING OPERATIONS IN PYTHON
# =============================================

# Input from user
text = input("Enter a string: ")
print("\n============================")
print("ORIGINAL STRING:", text)
print("===============================")

# STRING SLICING
print("\n STRING SLICING:")
print("a) First 5 characters:", text [0:5])
print("b) Characters from index 2 to 8:", text [2:9])
print("c) Last 4 characters:", text [-4:])
print("d) Every 2nd character:", text[::2])
print("e) Reverse the string:", text[::-1])

# TYPE CASTING
print("\n TYPE CASTING (String to Number and Back):")
num str = "123"
print("String:", num str, "Type:", type (num_str))
num_int  int(num_str) # Convert string to integer
num_float = float(num_str) # Convert string to float
print("After int() Casting:", num int, "Type:", type (num_int))
print("After float() Casting:", num float, "Type:", type (num_float))
back_to_string = str(num_int)
print ("Back to String:", back to string, "Type:", type (back to string))

# STRING FUNCTIONS
print("\nSTRING FUNCTIONS:")

# Case conversion
print("a) Uppercase:", text.upper())
print("b) Lowercase:", text.lower())
print("c) Title Case:", text.title())
print("d) Swapcase (upper->lower, lower->upper):", text.swapcase())
print("e) Capitalize (first letter uppercase):", text.capitalize())

# Spacing
print("\n--- Whitespace and Formatting ---")
print("f) Strip (remove extra spaces):", text.strip())
print("g) Left Strip:", text.lstrip())
print("h) Right Strip:", text.rstrip())

# Searching and Replacing
print("\n--- Searching & Replacing ---")
print("i) Replace 'a' with '@':", text.replace('a', '@'))
print("j) Find index of 'o':", text.find('o'))
print("k) Index of first space:", text.find(' '))
print("1) Count of 'e':", text.count('e'))

# Checking content type
print("\n--- Checking String Type ---")
print("m) Is alphabetic?:", text.isalpha())
print("n) Is numeric?:", text.isdigit())
print("o) Is alphanumeric?:", text.isalnum())
print("p) Is upper?:", text.isupper())
print("q) Is lower?:", text.islower())
print("r) Is title case?:", text.istitle())
print("s) Is space?:", text.isspace())

# Alignment and formatting
print("\n--- Alignment and Formatting ---")
print("t) Center text (width 30):", text.center (30, '-'))
print("u) Left justify:", text.ljust(30,'*'))
print("v) Right justify:", text.rjust(30, '*'))

# Splitting and joining
print("\n--- Split and Join ---")
words = text.split() # Splits string into list by spaces
print("w) Split into words:", words)
joined = "-".join(words)
print("x) Join words with '-':", joined)

# Character check
print("\n--- Additional Info ---")
print("y) String length:", len (text))
if text:
    print("z) First character:", text [0])
    print("Last character:", text [-1])
else:
    print("String is empty!")

# Combining String and Number (Casting Example)
print("\nCOMBINING STRING AND NUMBER:")
age = 25
message "My age is + str(age) + years."
print (message)

#MULTILINE STRING
print("\n MULTILINE STRING EXAMPLE:")
multi_text = """Python is fun!
It is powerful, yet simple.
Great for beginners and professionals."""
print (multi_text)
print("\nAll string operations executed successfully!")
```

---

#### c. Implement a program based on Simple statements using Variables, Scope of variable, Built-in Data Types, Types of operator, etc.

```python
# =========================================================
# SIMPLE STATEMENTS, VARIABLES, DATA TYPES & OPERATORS
# =========================================================

# SIMPLE STATEMENTS & VARIABLES
# A simple statement performs a single action (like assignment or print)
name = "Madhura"
age = 22
city = "Dhule"
print("Name:", name)
print("Age:", age)
print("City:", city)

# BUILT-IN DATA TYPES
print("\n--- BUILT-IN DATA TYPES ---")

# Numeric types
integer_num = 10 # int
float_num = 15.75 # float
complex_num = 2+3j # complex

# Sequence types
string_val = "Python"
list_val = [1, 2, 3, 4]
tuple_val = ('a', 'b', 'c')

# Mapping type
dict_val = {"name": "Madhura", "age": 22}

# Set types
set val = {10,20,30}

# Boolean type
bool val = True

# Display data types
print("Integer:", integer_num, "Type:", type (integer_num))
print("Float:", float_num, "Type:", type (float_num))
print("Complex:", complex_num, "Type:", type (complex_num))
print("String:", string_val, "Type:", type (string_val))
print("List:", list_val, "Type:", type (list_val))
print("Tuple:", tuple_val, "Type:", type (tuple_val))
print("Dictionary:", dict_val, "Type:", type (dict_val))
print("Set:", set_val, "Type:", type (set_val))
print("Boolean:", bool_val, "Type:", type (bool_val))

# SCOPE OF VARIABLES
print("\n--- SCOPE OF VARIABLES ---")
global_var = "I am Global" # Global variable

def my function():
    local var = "I am Local" # Local variable
    print("Inside Function:")
    print("Local Variable:", local var)
    print("Accessing Global Variable inside function:", global_var)

my_function ()
print("Outside Function:")
print("Global Variable:", global_var)
# print (local_var) # Error: local_var not accessible outside the function

# TYPES OF OPERATORS
print("\n--- TYPES OF OPERATORS ---")
a = 10
b = 5

# Arithmetic Operators
print("Arithmetic Operators:")
print("Addition:", a + b)
print("Subtraction:", ab)
print("Multiplication:", a * b)
print("Division:", a / b)
print("Floor Division:", a // b)
print("Modulus:", a% b)
print ("Exponent:", a ** b)

# Comparison Operators
print("\nComparison Operators:")
print("a == b:", a == b)
print("a != b:", a != b)
print("a > b:", a > b)
print("a < b:", a < b)
print("a >= b:", a >= b)
print("a <= b:", a <= b)

# Logical Operators
print("\nLogical Operators:")
x = True
y = False
print("x and y:", x and y)
print("x or y:", x or y)
print("not x:", not x)

# Assignment Operators
print("\nAssignment Operators:")
num = 10
num += 5 # num = num+5
print("After +=:", num)
num = 3
print("After -=:", num)
num *= 2
print("After *= :", num)
num = 4
print("After /= :", num)

# Bitwise Operators
print("\nBitwise Operators:")
a = 5 # 0101
b = 3 # 0011
print("a & b (AND):", a & b)
print("a | b (OR):", a b)
print("a ^ b (XOR):", a^ b)
print("~a (NOT):", ~a)
print("a << 1 (Left Shift):", a << 1)
print("a >> 1 (Right Shift): ", a >> 1)

# Membership Operators
print("\nMembership Operators:")
name_list = ["Roshani", "Amit", "Sita"]
print("'Roshani' in list:", "Roshani" in name_list)
print("'Rekha' not in list:", "Rekha" not in name _list)

# Identity Operators
print("\nIdentity Operators:")
x = [1,2,3]
y = [1,2,3]
z = x
print("x is y:", x is y) # False different objects
print("x is z:", x is z) # True same object
print("x is not y:", x is not y)
print("\nProgram executed successfully!")
```

---

#### d. Implement a program based on decision and looping statements.

```python
# ====================================
# DECISION-MAKING AND LOOPING STATEMENTS IN PYTHON
# ====================================
print("=== Decision and Looping Statements Example ===")

#DECISION MAKING STATEMENTS
print("\n--- DECISION MAKING ---")

# Example 1: Simple if
num int(input("Enter a number: "))
if num > 0:
    print("Number is positive")

# Example 2: if-else
if num % 2 == 0:
    print("Number is Even")
else:
    print("Number is Odd")

# Example 3: if-elif-else ladder
marks int(input("\nEnter your marks: "))
if marks >= 75:
    print("Grade: Distinction")
elif marks >= 60:
    print("Grade: First Class")
elif marks >= 50:
    print("Grade: Second Class")
elif marks >= 35:
    print("Grade: Pass Class")
else:
    print("Grade: Fail")

# Example 4: Nested if
age int(input("\nEnter your age: "))
if age >= 18:
    if age >= 60:
        print("You are a Senior Citizen")
    else:
        print("You are an Adult")
else:
    print("You are a Minor")

#LOOPING STATEMENTS
print("\n--- LOOPING STATEMENTS ---")

# Example 1: for loop with range ()
print("\nUsing for loop (1 to 5):")
for i in range(1, 6):
    print(i, end=" ")

# Example 2: for loop with list
fruits = ["Apple", "Banana", "Cherry"]
print("\n\nList of Fruits:")
for fruit in fruits:
    print (fruit)

# Example 3: while loop
print("\nUsing while loop (count 1 to 5):")
count = 1
while count <= 5:
    print (count, end="")
    count += 1

# Example 4: break statement
print("\n\nBreak Example:")
for i in range (1, 10):
    if i == 5:
        print("Breaking loop at i=", i)
        break
    print ("i=", i)

# Example 5: continue statement
print("\nContinue Example (skip even numbers):")
for i in range (1, 10):
    if i % 2 == 0:
        continue
    print("Odd number:", i)

# Example 6: Nested loop
print("\nNested Loop Example:")
for i in range (1, 4):
    for j in range (1, 4):
        print(f"({i}, {j})", end=" ")
    print() # for new line

print("\nProgram executed successfully!")
```

---

#### e. Implement a program based on Tuples, Lists, Dictionaries and Sets etc.

```python
# Program: Demonstration of Tuples, Lists, Dictionaries and Sets

# Tuple Example (Immutable)
print("---- Tuple Example ----")
fruits = ("apple", "banana", "cherry", "apple")
print("Tuple:", fruits)
print("First fruit:", fruits [0])
print("Count of 'apple':", fruits.count("apple"))
print("Index of 'banana':", fruits.index("banana"))
print("Sliced Tuple:", fruits [1:3])
# Tuples are immutable, so we cannot modify them
# fruits [0] = "mango" # This will cause an error
print("Length of tuple:", len (fruits))
print()

# List Example (Mutable)
print("---- List Example ----")
numbers = [10,20,30,40,50]
print("Original List:", numbers)
numbers.append (60) # Add element
numbers.insert(2, 25) # Insert at position
numbers.remove(40) # Remove element
numbers.pop() # Remove last element
numbers.sort() # Sort the list
numbers.reverse() # Reverse the list
print("Modified List:", numbers)
print ("Length of List:", len (numbers))
print("First 3 elements (slicing):", numbers[:3])
print()

print("---- Dictionary Example ----")
student = {
    "name": "Riya",
    "age": 21,
    "course": "BCA",
    "marks": 89
}
print("Dictionary:", student)
print("Name:", student ["name"])
print("All Keys:", student.keys())
print("All Values:", student.values())
print("All Items:", student.items())

# Add / Update / Delete values
student ["grade"] = "A"
student ["marks"] = 92
del student ["age"]
print("Updated Dictionary:", student)

# Using get() safely
print("Get Course:", student.get("course"))
print()

print("---- Set Example ----")
colors = {"red", "blue", "green", "red"}
print("Set:", colors)
colors.add("yellow")
colors.remove ("blue") # Duplicate 'red' is removed automatically
print("Modified Set:", colors)

# Set Operations
set1 = {1,2,3,4}
set2 = {3,4,5,6}
print("Union:", setl.union (set2))
print("Intersection:", set1.intersection (set2))
print("Difference:", set1.difference (set2))
print("Symmetric Difference:", set1.symmetric_difference (set2))
```

---

### 2. Function and Organizing Programs

#### a. Implement a program based on Functions, Function with parameters.

```python
# Function without parameters
def greet():
    print("Hello Welcome to Python Programming")

# Calling the function
greet ()

# Function with parameters
def add numbers (a, b):
    result = a + b
    print("The sum of", a, "and", b, "is", result)

# Taking input from user
num1 int (input("Enter first number "))
num2 int(input("Enter second number "))
add numbers (num1, num2)

# Function with return statement
def multiply(x, y):
    product = x * y
    return product

# Taking input and using return value
n1 = int(input("Enter number 1 "))
n2 = int(input("Enter number 2"))
result = multiply (n1, n2)
print("The product is", result)

# Function with default parameter
def greet_user (name = "Guest"):
    print("Hello", name, "Welcome back")

# Taking name from user
user_name input("Enter your name ")
if user_name == "":
    greet_user()
else:
    greet_user (user_name)

# Function returning multiple values
def calculate (a, b):
    add = a + b
    sub = a - b
    mul = a * b
    return add, sub, mul

# Taking user input
num a = int(input("Enter first value "))
num b int (input("Enter second value "))
sum result, sub result, mul result = calculate (num a, num b)
print("Sum", sum_result)
print("Subtraction", sub_result)
print("Multiplication", mul result)
```

---

#### b. Implement a program based on Functions Inside of Functions.

```python
# Outer function
def main function():
    print("This is the main function")

    # Inner function 1
    def addition():
        num1 int(input("Enter first number for addition "))
        num2 int (input("Enter second number for addition "))
        result = num1 + num2
        print("Addition is", result)

    # Inner function 2
    def subtraction():
        num1 int(input("Enter first number for subtraction"))
        num2 int(input("Enter second number for subtraction "))
        result = num1 num2
        print("Subtraction is", result)

    # Inner function 3
    def multiplication():
        num1 int(input("Enter first number for multiplication "))
        num2 int(input("Enter second number for multiplication "))
        result = num1 * num2
        print("Multiplication is", result)

    # Calling inner functions
    addition()
    subtraction ()
    multiplication()

# Call the outer function
main function ()
```

---

#### c. Implement a program based on built-in functions.

```python
# Program based on Built-in Functions in Python

# Taking user input
num1 int (input("Enter first number "))
num2 int (input("Enter second number "))
num3 int(input("Enter third number "))

# Using built-in numeric functions
print("Maximum number is", max (num1, num2, num3))
print("Minimum number is", min(num1, num2, num3))
print("Sum of all numbers is", sum ( num1, num2, num3]))
print("Power of first number raised to second number is", pow (num1, num2))

# Using built-in string functions
name input("Enter your name ")
print("Length of your name is", len(name))
print("Uppercase:", name.upper())
print("Lowercase:", name.lower())
print("First letter capital:", name.capitalize())

# Using built-in type checking
print("Data type of num1 is", type (num1))
print("Data type of name is", type (name))

# Using list related built-in functions
numbers = [num1, num2, num3, 50, 25]
print("Original List:", numbers)
print("Sorted List:", sorted (numbers))
print("Length of List:", len (numbers))
print("Sum of List:", sum (numbers))
print("Maximum value in List:", max(numbers))
print("Minimum value in List:", min (numbers))

# Using mathematical built-in functions
import math
value float(input("Enter a number to find square root "))
print("Square root of", value, "is", math.sqrt(value))
print("Floor value of", value, "is", math.floor(value))
print("Ceiling value of", value, "is", math.ceil(value))
```

---

#### d. Implement a program using Anonymous Functions Lambda and Filter.

```python
# Program using Lambda and Filter with user input

# Take a list of numbers from the user
numbers = input("Enter numbers separated by space ")
numbers numbers.split # Split string into list
numbers list (map(int, numbers)) # Convert each element to integer
print("Original List:", numbers)

# Lambda for square of a number
square lambda x: x * x
num int(input("Enter a number to find square "))
print("Square of", num, "is", square (num))

# Using lambda to check even or odd
check = lambda n: "Even" if n % 2 == 0 else "Odd"
number int(input("Enter a number to check even or odd "))
print("The number is", check (number))

# Using filter() with lambda to find even numbers
even numbers = list(filter (lambda x: x % 2 == 0, numbers))
print("Even numbers are:", even_numbers)

# Using filter() with lambda to find numbers greater than a value
limit int(input("Show numbers greater than "))
greater_numbers = list(filter (lambda x: x > limit, numbers))
print("Numbers greater than", limit, "are:", greater_numbers)

# Using map() with lambda to find cube of all numbers
cubes list (map (lambda x: x * x * x, numbers))
print("Cube of all numbers:", cubes)
```

---

#### e. Implement a program using Maps, List Comprehension and Dictionaries.

```python
numbers = input("Enter numbers separated by space: ")
numbers numbers.split()
numbers = list (map (int, numbers)) # Convert all inputs to integers
print("Original Numbers:", numbers)

squares = list(map(lambda x: x * x, numbers))
print("Square of numbers:", squares)

even numbers = [x for x in numbers if x % 2 == 0]
print("Even Numbers:", even_numbers)

cubes = [x ** 3 for x in numbers]
print("Cube of numbers:", cubes)

# Using Dictionary
# Create a dictionary where key = number, value square
num_square_dict = {x: x * x for x in numbers}
print("Dictionary of Number: Square ->", num_square_dict)

# Create dictionary from user names
names input("Enter names separated by space: ").split()
name_length = {name: len (name) for name in names}
print("Dictionary of Name: Length ->", name_length)
```

---

#### f. Implement a program to demonstrate Class and Object.

```python
class Student:
    # Constructor
    def init (self, name, roll no, marks):
        self.name = name
        self.roll_no = roll_no
        self.marks = marks

    # Method to display student details
    def display_info(self):
        print("Student Name:", self.name)
        print("Roll Number:", self.roll_no)
        print("Marks:", self.marks)

    # Method to check grade
    def check grade (self):
        if self.marks >= 75:
            print("Grade: Distinction")
        elif self.marks >= 60:
            print("Grade: First Class")
        elif self.marks >= 40:
            print("Grade: Pass")
        else:
            print("Grade: Fail")

# -- Taking input from user
name input("Enter Student Name: ")
roll_no = input("Enter Roll Number: ")
marks = float(input("Enter Marks: "))

# --- Creating object of class
student1 = Student (name, roll_no, marks)

# Calling methods
student1.display_info ()
student1.check_grade ()
```

---

#### g. Implement a program to demonstrate Array.

```python
# Import array module
import array

# Create an empty array of integers
numbers = array.array('i', [])

# Take number of elements from user
n = int(input("Enter how many elements you want in array: "))

# Taking array elements from user
for i in range(n):
    num int(input("Enter element + str(i + 1) + ": "))
    numbers.append(num)

# Display the array
print("Array elements are:", numbers)

# Display each element using loop
print("Array elements one by one:")
for num in numbers:
    print (num)

# Perform some array operations
print("First element:", numbers[0])
print("Last element:", numbers[-1])

# Update an element
index = int(input("Enter index number to update: "))
new_value int(input("Enter new value: "))
numbers [index] = new value
print("Updated Array:", numbers)

# Remove an element
value int(input("Enter element to remove: "))
numbers.remove(value)
print("Array after removing element:", numbers)
```

---

#### h. Implement a program to create, import and use package and modules.

**Step 1: Create module `math_operations.py`**
```python
# math_operations.py
def add(a, b):
    return a + b

def multiply(a, b):
    return a b
```

**Step 2: Create module `string_operations.py`**
```python
# string_operations.py
def upper_case (text):
    return text.upper()

def lower_case (text):
    return text.lower()
```

**Step 3: Create `main_program.py`**
```python
# main_program.py
# Import modules from the package
from myPackage import math_operations, string_operations

# Use math module functions
a = int(input("Enter first number: "))
b = int (input("Enter second number: "))
print("Addition:", math_operations.add(a, b))
print("Multiplication:", math_operations.multiply(a, b))

# Use string module functions
text input ("Enter any text: ")
print("Uppercase:", string_operations.upper_case (text))
print("Lowercase:", string_operations.lower_case (text))
```

---

### 3. File And Directories

#### a. Implement a program based on Writing Text Files, Appending Text to a File, Reading Text Files.

```python
# Program to Write, Append and Read from a Text File

# --- Writing to a file
file open("student.txt", "w") # 'w' = write mode
file.write("Welcome to Python File Handling\n")
file.write("This is the first line of the file.\n")
file.close()
print("Data written to file successfully!")

# --- Appending to a file
file open("student.txt", "a") # 'a' = append mode
file.write("This line is added later using append mode.\n")
file.close()
print("Data appended successfully!")

# --- Reading from a file
file = open("student.txt", "r") # 'r' = read mode
print("\n--- Reading File Content ---")
content = file.read()
print (content)
file.close()
```

---

#### b. Implement a program based on paths and directories, file information, naming, moving, copying, and removing files.

```python
import os

# Step 1: Create a new folder
os.mkdir("MyFolder")
print("Folder created: MyFolder")

# Step 2: Create a file inside the folder
file_path = "MyFolder/sample.txt"
file open(file_path, "w")
file.write("Hello, this is a test file.")
file.close()
print("File created inside MyFolder.")

# Step 3: Rename the file
new_file_path = "MyFolder/renamed_sample.txt"
os.rename(file_path, new_file_path)
print("File renamed successfully.")

# Step 4: Move (simulate move using rename)
# First, create a new folder
os.mkdir("Backup")

# Now move the file by renaming its path
os.rename (new_file_path, "Backup/renamed_sample.txt")
print("File moved to Backup folder.")

# Step 5: Delete the file
os.remove("Backup/renamed_sample.txt")
print("File deleted successfully.")

# Step 6: Remove both folders
os.rmdir("MyFolder")
os.rmdir("Backup")
print("Folders removed successfully.")
```

---

#### c. Implement a program Based on Regular Expression and its functions.

```python
import re

# Take user input
text input("Enter any text: ")

#re.search() Find if pattern exists
if re.search(r"\d+", text):
    print("Text contains numbers.")
else:
    print("No numbers found in text.")

#re.findall() -> Find all occurrences
words re.findall(r" [A-Za-z]+", text)
print("All words found:", words)

# re.sub() Replace text
replaced_text = re.sub(r"\d", "*", text)
print("After replacing digits with :", replaced_text)

#re.split() -> Split string by space
split_text = re.split(r"\s+", text)
print("Split text into words:", split_text)

#re.match() -> Match from start
if re.match(r" [A-Z]", text):
    print("Text starts with a capital letter.")
else:
    print("Text does not start with a capital letter.")
```

---

### 4. Python GUI Programming

#### a. Implement a program creating Types of GUI Widgets, Resizing, and Configuring Options.

```python
from tkinter import *

# Create main window
root Tk()
root.title("GUI Widgets Example")
root.geometry("400x400") # Set window size (width x height)
root.resizable (True, True) # Allow resizing

# Configure background color
root.config(bg="lightblue")

# Label Widget
label = Label (root, text="Welcome to Python GUI", font=("Arial", 16), bg="lightblue", fg="darkblue")
label.pack (pady=10)

# --- Entry Widget (for text input)
entry_label = Label (root, text="Enter your name:", bg="lightblue")
entry_label.pack()
entry = Entry (root, width = 30)
entry.pack (pady=5)

# Button Widget
def show_message():
    name = entry.get()
    label_result.config(text="Hello, + name + !")

button = Button (root, text="Click Me", command=show_message, bg="green", fg="white")
button.pack (pady = 10)

# Label to display result
label_result = Label (root, text="", bg="lightblue", font=("Arial", 12))
label_result.pack(pady = 10)

# Checkbutton Widget
check_var = IntVar()
check = Checkbutton (root, text="I like Python", variable=check_var, bg="lightblue")
check.pack (pady=5)

# Radiobutton Widget
radio_var = StringVar()
radio_var.set("Beginner")
Label (root, text="Select Level:", bg="lightblue").pack()
Radiobutton (root, text="Beginner", variable=radio_var, value="Beginner", bg="lightblue").pack()
Radiobutton (root, text="Intermediate", variable=radio_var, value="Intermediate", bg="lightblue").pack()
Radiobutton (root, text="Advanced", variable=radio_var, value="Advanced", bg="lightblue").pack()

# Quit Button
quit_button = Button(root, text="Exit", command=root.destroy, bg="red", fg="white")
quit_button.pack(pady=10)

# Run the GUI
root.mainloop()
```

---

#### b. Implement a program Creating Layouts, Packing Order, Controlling Widget Appearances.

```python
from tkinter import *

# Create main window
root Tk()
root.title("Layout & Packing Example")
root.geometry("400x300")
root.config(bg="lightyellow")

# Top Frame
top_frame = Frame(root, bg="lightblue", relief=RIDGE, borderwidth = 3)
top_frame.pack(side = TOP, fill=X, pady=5)
Label (top_frame, text="Top Frame", bg="lightblue", font=("Arial", 14, "bold")).pack(pady=5)

# Left Frame
left_frame Frame(root, bg="lightgreen", relief=GROOVE, borderwidth = 3)
left_frame.pack(side=LEFT, fill=Y, padx=5)
Label (left frame, text="Left Menu", bg="lightgreen", font=("Arial", 12)).pack(pady=10)
Button (left frame, text="Option 1", bg="white").pack(pady = 5, padx=10)
Button (left frame, text="Option 2", bg="white").pack (pady = 5, padx = 10)

# Right Frame
right_frame Frame(root, bg="lightpink", relief=SUNKEN, borderwidth=3)
right_frame.pack(side=RIGHT, expand=True, fill=BOTH, padx = 5, pady=5)
Label (right frame, text="Main Content Area", bg="lightpink", font=("Arial", 12, "bold")).pack(pady=10)

# Add buttons with packing order
Button (right frame, text="Top", bg="skyblue").pack(side=TOP, pady=5)
Button (right_frame, text="Bottom", bg="orange").pack(side=BOTTOM, pady = 5)
Button (right_frame, text="Left", bg="lightgray").pack(side=LEFT, padx=5)
Button (right_frame, text="Right", bg="lightgray").pack(side=RIGHT, padx=5)

# Bottom Frame
bottom_frame = Frame(root, bg="lightgray", relief RAISED, borderwidth = 2)
bottom_frame.pack(side=BOTTOM, fill=X)
Label (bottom_frame, text="Status: Ready", bg="lightgray", font=("Arial", 10, "italic")).pack(pady=3)

# Run the window
root.mainloop()
```

---

### 5. Text Processing

#### a. Implement a program based on Text Processing, Searching for Files.

```python
# Part 1: Text Processing
file_name = input("Enter file name (example: sample.txt): ")
try:
    f = open(file_name, "r")
    text = f.read()
    f.close()

    # Count lines, words, and characters
    lines text.split("\n")
    words = text.split()
    chars = len (text)

    print("\n--- File Information ---")
    print("Total Lines:", len (lines))
    print("Total Words:", len(words))
    print("Total Characters:", chars)

    # Search for a word
    search_word input("\nEnter a word to search in the file: ")
    if search_word in text:
        print(f"'{search_word}' found in the file")
    else:
        print(f"'{search_word}' not found ")
except FileNotFoundError:
    print("File not found! Please check the file name.")

# Part 2: Simple File Searching
# Instead of using os, we take a list of file names from the user
print("\n--- Simple File Search ---")
files input("Enter some file names separated by commas: ")
file_list = files.split(",") # convert to list
file_list = [f.strip() for f in file list] # remove spaces

search_ext = input("Enter file extension to search (example: .txt): ")
print (f"\nFiles with extension 'search_ext}':")
found = False
for f in file list:
    if f.endswith(search ext):
        print("", f)
        found = True
if not found:
    print("No files found with that extension.")
```

---

#### b. Implement a program to demonstrate HTML Parsing.

```python
from bs4 import BeautifulSoup

# Sample HTML content
html doc = """
<html>
<title>Student Page</title>
<head>
</head>
<body>
<h1>Welcome Students</h1>
<p class="info">Python is easy to learn</p>
<p class="info">HTML parsing using BeautifulSoup</p>
<a href="https://www.python.org">Python Official Website</a>
</body>
</html>
"""

# Parse HTML
soup = BeautifulSoup (html_doc, 'html.parser')

# Get title
print("Title:", soup.title.string)

# Get all paragraph text
print("\nParagraphs:")
for p in soup.find_all('p'):
    print(p.text)

# Get link
link soup.find('a')
print("\nLink text:", link.text)
print("Link URL:", link.get('href'))
```

---

### 6. Accessing Databases

#### a. Implement a program based on using DBM Creating and Accessing Persistent Dictionaries.

```python
import dbm

# Create / open a DBM database
db = dbm.open("student_db", "c")

# Store data (key-value pairs)
db ["name"] = "Roshani"
db ["course"] = "Python"
db ["year"] = "2025"

# Close the database
db.close()

# Reopen the database to access data
db = dbm.open("student_db", "r")

# Read and display data
print("Name:", db("name").decode())
print("Course:", db ["course"].decode())
print("Year:", db ["year"].decode())

# Close database
db.close()
```

---

#### b. Implement a program based on using Relational Database Writing SQL Statements, Defining Tables, Setting Up a Database. ( Transactions and Committing the Results.)

```python
import mysql.connector

# Step 1: Connect to MySQL server (XAMPP)
conn mysql.connector.connect(
    host="localhost",
    user="root",
    password=""
)
cursor = conn.cursor()

# Step 2: Create database
cursor.execute("CREATE DATABASE IF NOT EXISTS college")
print("Database created")

# Step 3: Use database
cursor.execute("USE college")

# Step 4: Create table
cursor.execute("""
CREATE TABLE IF NOT EXISTS student (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    course VARCHAR(30)
)
""")
print("Table created")

# Step 5: Insert data (Transaction)
sql = "INSERT INTO student (id, name, course) VALUES (%s, %s, %s)"
values = (1, "Roshani", "Python")
cursor.execute(sql, values)

# Step 6: Commit transaction
conn.commit()
print("Data inserted and committed")

# Step 7: Fetch data
cursor.execute ("SELECT * FROM student")
result = cursor.fetchall()
print("\nStudent Table Data:")
for row in result:
    print (row)

# Step 8: Close connection
conn.close()
```