# Tutorial 3: Python week 3. 


## Contents:
  - [1. If statements](#1. If statements)
  - [2. For loops](#2. For loops )
  - [3. Combing both](#3. Combing both)
  - [4. Lists](#4. Lists)
  - [5. Dictionaries](#5. Dictionaries)
  - [6. Combining EVERYTHING together](#6. Combining EVERYTHING together) 

 
## 1. If statements
*If statements* perform different computations or actions depending on whether a programmer-specified boolean condition evaluates to true or false. *If statements* are very important in branching processes and help segregate blocks of code based off of logic. 

Below is an example of an *if statement* in Python
```python
if 5 % 2 == 0:
  print "Five divided by two has no remainder"
else:
  print "Five divided by two has a remainder"
```
 **Task 1.1** 
 Fill in the **if statement to print out "Six divided by two has a remainder"
```python
if 6 %  = :
  print "Five divided by two has no remainder"
else:
  print "Five divided by two has a remainder"
```

 **Task 1.2** 
 Change the 'x == 5' statement so the *if statement* prints "I know how to read strings."
```python
x = "5"
if x == 5:
  print "I know how to read strings."
else:
  print "I may need to check what type x is. "
```

## 2. For loops 
A *for loop* is a control flow statement for specifying iteration, which allows code to be executed repeatedly. 

Below is an example of an *for loop* in Python
```python
for element in range(4):
  print(element)
```

**Task 2.1**
In this task, prin out all the values from 14 to 20.
```python
for element in range(?,?):
  print( ? )
```



## 3. Combing both
Both *if statements* and *for loops* are fundamental building blocks to programming. In combination they allow for logic to be repeatedbly be applied.

Below are two tasks to test your knowledge by combining the two. 

**Task 3.1** 
Using both a *for loop* and *if statement* print out all the odd numbers between zero and ten. 
```python
for element in range(?):
  if ? ? ? == ?:
    print 
```

**Task 3.2**
In the following, print start with a variable 'counter' set to 0 (counter = 0), use a for loop to add 3 to 'counter' stopping the loop if 'counter' exceeds 14, printing the result in each interation. Hint: 'break' will stop the loop. Also check the spelling!
```python
counter = 0 
for element in range(10):
  counter = ? + 3
  print( ? )
  if ? > ?:
    brake
```


## 4. Lists
Data types have already been explored in *Task 1.2*. Common data types include strings, floats and integers. Another important data type is the *list*. In Python, a *list* can initially be thought of as a vector. You can do analogous tasks to them, reference, multiply them, add them etc. 

Below is an example that prints '12', and '12, "test"', respectively. 
```python 
my_first_list = [12, "test", 42]
print(my_first_list[0])
print(my_first_list[0:1]
```
**Task 4.1**
By referencing 'my_second_list', print the third, fourth, fifth and sixth fibonacci numbers.
```python
my_second_list = [1, 1, 2, 3, 5, 8, 13, 21, 34] 
print( ? )
```

**Task 4.2**
Calculate the sum of the the list my_third_list. BE CAREFUL OF THE TYPES!
```python
my_third_list = [17, 25, 37, "42", 100]
print( ? )
```

## 5. Dictionaries
Like *lists*, *dictionaries* are another data type and another way to store data. However, instead of storing data as a single vector, they store data as key value. This data structure (analogous to JSON) is very common and used alot for APIs. More information on JSON data structures and it's usefulness can be found [here]()

Below is an example of a *dictionary*. Note how we use "second" as a key and '.keys()' to get all the keys.
```python
my_first_dictionary = {"first": 12, "second":20, "third":42}
print( my_first_dictionary['second'] ) 
print( my_first_dictionary.keys() )
# We can add to the dictionary be doing the following. 
my_first_dictionary['fourth'] = 3.14
```

**Task 5.1**
Create a dictionary with two strings and two integers.
```python
my_second_dicitonary = {" ": ?, ?}
print( my_second_dictionary['? '] )
print( my_second_dictionary   ?   )
```

**Task 5.2**
Print out the values for the dictionary in ascending order. Hint: if a dictionary is a 'key:value' store and '.keys()' accesses the keys in a dictionary, what function will access the values. Further how can you use the function 'sorted' to get the values in ascending order?
```python
my_third_dictionary = {"first": 10, "fifty": 50, "third": 30, "second": 20, "four": 40}
print( ?(my_third_dicitonary?) )
```
## 6. Combining EVERYTHING together
Now you have been through all of the most important data structures and logic it is time to bring them all together.

**Task 6.1** 
Iterate through all of the values and print out the values if they are of type 'string' or above 33. 
```python
my_fourth_dictionary = {"first": 10, "fifty": 50, "third": "30", "second": 20, "four": 40}
my_fourth_dictionary_values = my_fourth_dictionary
for i in ?: 
  if  isinstanceof(?,?) or ? > ?:
    print( ? ) 
```

**Task 6.2**
We have so far covered generic *for loops*, however, we are now going to look at special type called the *enumerate for loop*. This not only loops of values but also keeps an index as it it looping. A documentation of these loops can be found [here](http://book.pythontips.com/en/latest/enumerate.html). In the last task, your job is to initialise a dictionary called 'Austrlian_cities', and use the *enumerate for loop* to iterate through the keys (States) and save their capital cities as the values in a dictionary. Once created, print out this dictionary. 
```python
Australian_cities = {}
keys = ["WA", "Vic", "NSW", "SA" ]
values = ["Perth", "Melbourne", "Sydney", "Adelaide"]
for index, key in enumerate(keys):
  Australian_cities[ ? ] = values[ ? ]
 
print( ? )
```
