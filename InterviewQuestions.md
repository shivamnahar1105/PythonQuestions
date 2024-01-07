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


