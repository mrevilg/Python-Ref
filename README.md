# Python Coding Language
Python code base for individual and ongoing projects

## Basic Concepts
| Operator Precedence | Explanations |
| ------------- | ------------- |
| **  | To the power of  |
| -X  | Negative number  |
| * / %  | Multiply, Divide, Modulus or Remainder |
| + -  | Add, Minus  |
| *Boolean* | ------------- |
| not  | First  |
| and | Next  |
| or  | Last  |

 "#" for a comment line
 
 "\n" is a string, needs '' or ""
 
input function will always return a string unless: int('*prompt*') * 7 etc to generate total, not string.

len() is a counting function, not an indexing 

## Style Best Practices
### PEP 8 Recommendations
#### Indentation - 4 spaces, not 4 tabs
#### Line Length - 79 Char, 72 Char for Comments
#### Blank Lines - to indicate blocks of code visually

##

#### *Variables*
- Start with a letter or underscore
- Avoid the following keywords

| False | None | True  |  |   |  | |  |
| ------------- | ------------- |------------- | ------------- |------------- | ------------- |------------- | ------------- |
| and | as | assert |break |class |continue |def |del |
| elif | else | except |global |is |or |try |break |
| finally | for | if |lambda |pass |while |import |nonlocal |
|raise |with |in | not | return | yield|

### *Methods/Functions*
#### *String Methods*
- len or str (variablename), etc...
- len(), str(),

#### *'dot' Methods*
- variablename.lower(), variablename.upper() etc...
- .lower(), .upper(),
- .title() ...Cap first letter of each word in string


#### *'whitespacing' Methods*
- print("\tPython") tabspace then string
- print("\nPython") carriage Rtn then string
- variablename.rstrip() temp trim on right of var
- variablename.lstrip() temp trim on left of var
- variablename.strip() temp trim on left/right of var
- variablename = variablename.strip() perm trim on left/right of var

When using the result of an int (as a standalone variable) within the result of a string (concatenation of int+str) you must set how the int is to be used int/str e.g. :
  ```python
    age = 23
    print "Happy " + str(age) + "rd Birthday!"
  ```
##
#### *List Methods and Modifications*
Python lists are 'indexed' - they start at 0, using [-1] returns last item
  ```python
  bicycles = ['trek', 'cannondale', 'redline', 'specialized']
  print bicycles
  ```
- variable name[x] = new_content This will replace the index 'x' with the new value
- .append('newvalue') ...adds new value to end of list, or can be used to 'overflow'
- .insert(index, 'value') ... adds the new value at the noted index
- del variablename[x] = removal of that index's value
new_variablename = variablename.pop(x)... takes last index value and adds to new variable, or use 'x' index, Pop REMOVES values
- variablename.remove('actualvalue')... will search and remove noted value, first instance. Need loop for multiple.
- variable.sort()... permanently sorts the list, can do str or int, must define to concatenate mixed
- variable.sort(reverse=True)... perm reverse
- sorted(variablename)... temp sorting of list variable, can accept reverse=True argument
- variablename.reverse()... reverses the list as-is, perm.

#### *Lists and Loops*
 ```python
    variables = ['var_1', 'var_2', 'var_3',]
    for variable in variables:
        print(variable)
  ```
- Colon and subsequent line indentation associate that indented line *with the loop*
 ```python
    for value in range (1,5):
        print(value)
 ```
- range (x,y)... gives the tone stpes between each number
- variablename = list(range(x,y))... creates a list of numbers within the x/y range
- variablename = list(range(x,y,z))... x is start of range, y is end of range, z is step
```python
    squares = []
    for value in range (1,11):
        squares.append(value**2)
        
    print(squares)
 ```
 [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
 
 - If we use the now squares variable, min/max/sum are 1/100/385 respectivley 
 ```python
    squares = [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
    print(min(squares))
    print(max(squares))
    print(sum(squares))
 ```
*List comprehensions* are an embedded syntax in the list itself eg:
 ```python
    squares = [value**2 for value in range(1,11)]
    print(squares)
 ```
Slicing a list variablename = [1,2,3,4,5] print(variablename[x:y])... would print those index values in that range
- If you used [x,null], then it would return all index values from 'x' onward.
- If you used [-x:null], then it would return all values from the end of the list, per the number given.

Looping through a Slice, 
```python
    words = ['murray', 'john', 'paul', 'ringo', 'george']
    for word in words[:3]:
        print(word.title())    
 ```
 - As it is [:3]... will STOP the list after the FIRST 3 values
 - if it were [:-3]... would STOP the list 3 indexes from the END
 - if it were [3:]... it would START the list 3 values in from the START of the list
 - if it were [-3:]... it would START the list from 3 values FROM THE END of the list
 - [*index value at the START of list* : *index value for the STOP of list*] 
 
 An additional colon i.e. [::] would be Start/Stop/STEP. Steps are counted form one index to the next, not the index themselves.
 ```python
    words = ['murray', 'john', 'paul', 'ringo', 'george', 'alan', 'robert', 'diana']
    for word in words[::3]:
        print(word.title())    
 ```        
Immutable lists are called *Tuples*. This means that once defined, it cannot be changed. Tuples are defined with (BRACKETS & COMMAS!!!), but called with Sqr brackets [] like with a list using the desired indiex number. Tuples can be redefined later in code.
```python
    dimensions = (200, 50)
    print(dimensions[0])
    print(dimensions[1])

    print("\nOriginal Dimensions : ")
    for dimension in dimensions:
        print(dimension)

    dimensions = (400, 100)
    print("\nModified Dimensions : ")
    for dimension in dimensions:
        print(dimension)    
 ```
##
### IF Statements

In short,  if *conditional_test*:
                   *do something*
 ```python
     cars = ['audi', 'bmw', 'jeep', 'jaguar']

     for car in cars:
         if car == 'bmw':
             print (car.upper())
         else:
             print (car.title())
 ```
- If you include 'or' and 'and' as keywords you can concatenate variable names ()or/and().
#### IF Else (chain & blocks) Statements
 ```python
      age = 17
      if age >= 18:
          print("You are old enough to vote!")
          print("Have you registered to vote yet?")
      else:
          print("Sorry, you are to young to vote!")
          print("Be sure to register to vote when you turn 18!")
 ```
- elif = if/elif/else will break out at first true statement. For mutiple True requierments use multiple IF
```python
      age = 12
        if age < 4:
            print ("Your admisson cost is $0!")
        elif age < 18:
            print("Your admission cost is $5!")
        else:
            print("Your admission costs $10!")

        age = 65

        if age < 4:
            price = 0
        elif age < 18:
            price = 5
        elif age < 65:
            price = 10
        else:
            price = 5

        print ("Your admission is $" + str(price) + "!")
 ```
 
##
## File Explanation
### *Slogan Randomizer*
This is a simple syntax, which when run through multiple instances, creates a randomized sentance on each iteration.

### *Dog Age Calculator*
Simple code to prompt and calculate the age of your dog in human years 
  
