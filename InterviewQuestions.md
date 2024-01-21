# Python Basic Questions

[Python_Interview_Questions](https://colab.research.google.com/drive/18crmbaBn4AFYd8RUefb-LynmbU69uqlX)

### 1. 
- Value of True = 1 
- Value of False = 0 
- Value of None is Empty (not even Zero)

### 2. 
- print('' is '') # ---> returns true as string, int, float addrresses to the same memory if the value is same.
- print([] is []) # ---> returns False as list, tuple, dict creates different memories in the backend.
### 3. Difference between return & yield.
- Total keyword in python is 33
- Return sends a specified value back to its caller whereas Yield can produce a sequence of values.
  We should use yield when we want to iterate over a sequence, but don't want to store the entire sequence in memory. Yield are used in Python generators.
- Return gives a single value and yield usually gives a generator object on which we can iterate.

### 4. What is use of self in a class ?
- In Python, self is a conventional name for the first parameter of a method within a class.
  It represents the instance of the object itself. When you define a method within a class, the method should take self as its first parameter,
  and this parameter refers to the instance of the class.

### 5. where should we use Lambda function keyword in python ?
- They are usually used when we want a single result and not a resuable function.
- When a small function is needed for a short duration and defining a full function using def seems unnecessary, lambda functions provide a concise alternative.
- In Python, the lambda keyword is used to create anonymous functions, also known as lambda functions.
  Lambda functions are a concise way to create small, one-time-use functions without formally defining them using the def keyword.

### 6. try, else, except, finally
- a =5, b=0
- try:
  - q = a/b
  - print(q)
- except ZeroDivisionError:
  - print("Can't divide by error")
- else:
  - print("Else runs only if try block executes")
- finally:
  - print("Finally block always runs")

### 7. map function & sep function of print.

#### - Seprator in python
- The sep parameter in the print function is used to specify the separator between multiple arguments provided to the print function.
   When you print multiple values using print, they are separated by a space by default. However, you can use the sep parameter to change the separator.
   
  - a = 1
  - b = 2
  - c = 3
  - print(a, b, c, sep=", ")
 
#### - Map function 
- The map function in Python is used to apply a specified function to each item in an iterable (like a list) and returns a new iterable with the results.
- Example:
 ###### Define a function to square a number
def square(x):
    return x ** 2

###### Create a list of numbers
numbers = [1, 2, 3, 4, 5]

###### Use map to square each number in the list
squared_numbers = map(square, numbers)

###### Convert the result to a list (as map returns an iterable)
result_list = list(squared_numbers)

##### Print the squared numbers
print(result_list)


 ### 8. - Strings in python are immutable. So if we do slicing of a string new variable will be created for the same.

 ### 9. Data Structures in Python :
 - String
 - List
 - Tuple
 - Dictionary
 - Sets

 List Comprehension: We cannot use continue in list comprehension.

### 10. 
#### Sort vs Sorting 
- **Sort** is a method applied directly to a list, sorting it in place,
  while **Sorted** is a built-in function that creates a new sorted list from any iterable.
  Use sort if you want to modify the original list, and use sorted if you want to keep the original list unchanged and create a new sorted list.
 - Sort
    numbers = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5]
    numbers.sort()  # This sorts the list in-place
    print(numbers)  # [1, 1, 2, 3, 3, 4, 5, 5, 5, 6, 9]

- Sorting
    numbers = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5]
    sorted_numbers = sorted(numbers)  # This creates a new sorted list
    print(sorted_numbers)  # [1, 1, 2, 3, 3, 4, 5, 5, 5, 6, 9]
  

#### Remove vs Pop vs Discard  

- Both modifies the list in place.
- Use **Remove** if you want to remove a specific value from the list. It removes the first iterable.
- Use **pop** if you want to remove and optionally retrieve an element based on its index.

-- **Remove**
  .remove(x)
  This operation removes element x from the set.
  If element  does not exist, it raises a KeyError.
  The .remove(x) operation returns None.

-- **discard**
  This operation also removes element x from the set.
  If element  does not exist, it does not raise a KeyError.
  The .discard(x) operation returns None.

-- **pop**
  The .pop() method works differently for sets and lists.
  
  - **For sets:**
    The .pop() method removes and returns an arbitrary element from the set.
  - **For lists:**
    The .pop() method by default removes and returns the last element from the list if an index is not specified.
    If you provide an index as an argument (e.g., .pop(index)), it removes and returns the element at that specific index.

#### defaultdict

- The defaultdict tool is a container in the collections class of Python.
  It's similar to the usual dictionary (dict) container, but the only difference is that a defaultdict will have a default value
  if that key has not been set yet. If you didn't use a defaultdict you'd have to check to see if that key exists, and if it doesn't, set it to what you want.

#### Enumerate

- enumerate is a built-in function in Python that allows you to iterate over a sequence (such as a list, tuple, or string) along with its index.
It returns tuples containing the index and the corresponding item.

```
fruits = ['apple', 'banana', 'cherry']

for index, fruit in enumerate(fruits):
    print(f"Index {index}: {fruit}")
```

---- Output:
```
Index 0: apple
Index 1: banana
Index 2: cherry
```

### Namedtuple
- A named tuple is a subclass of a tuple in Python. It is similar to a regular tuple, but it has named fields accessible using dot notation in addition to the usual indexing.    Named tuples provide a way to define simple classes for storing data in a more readable and self-documenting way than traditional tuples or lists.

```
from collections import namedtuple

# Define a named tuple 'Point' with fields 'x' and 'y'
Point = namedtuple('Point', ['x', 'y'])

# Create an instance of the named tuple
p = Point(x=1, y=2)

# Access fields using dot notation
print(p.x)  # Output: 1
print(p.y)  # Output: 2

# Access fields using indexing
print(p[0])  # Output: 1
print(p[1])  # Output: 2

```

```
from collections import namedtuple

# Define a named tuple 'Color' with fields 'red', 'green', and 'blue'
Color = namedtuple('Color', ['red', 'green', 'blue'])

# Create an instance of the named tuple
color = Color(red=255, green=0, blue=127)

# Access fields using dot notation
print(color.red)    # Output: 255
print(color.green)  # Output: 0
print(color.blue)   # Output: 127
```
### zip function
- In Python, the zip function is used to combine two or more iterables (e.g., lists, tuples) element-wise, creating an iterator of tuples.
  Each tuple contains elements from the input iterables at the same position. The resulting iterator stops when the shortest input iterable is exhausted.

  ```
  >>> print zip([1,2,3,4,5,6],'Hacker')
  [(1, 'H'), (2, 'a'), (3, 'c'), (4, 'k'), (5, 'e'), (6, 'r')]
  >>> 
  >>> print zip([1,2,3,4,5,6],[0,9,8,7,6,5,4,3,2,1])
  [(1, 0), (2, 9), (3, 8), (4, 7), (5, 6), (6, 5)]
  >>> 
  >>> A = [1,2,3]
  >>> B = [6,5,4]
  >>> C = [7,8,9]
  >>> X = [A] + [B] + [C]
  >>> 
  >>> print zip(*X)
  [(1, 6, 7), (2, 5, 8), (3, 4, 9)]
  ```


  
