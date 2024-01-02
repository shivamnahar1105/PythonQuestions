# Python Basic Questions

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

### 4. where should we use Lambda function keyword in python ?
- They are usually used when we want a single result and not a resuable function.
- When a small function is needed for a short duration and defining a full function using def seems unnecessary, lambda functions provide a concise alternative.
- In Python, the lambda keyword is used to create anonymous functions, also known as lambda functions.
  Lambda functions are a concise way to create small, one-time-use functions without formally defining them using the def keyword.
