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
 
input function will always return a string unless: int('*prompt*') * 7 etc to generate total, not string.
len() is a counting function, not an indexing 

##### *Variables*
- Start with a letter or underscore
- Avoid the following keywords

| False | None | True  |  |   |  | |  |
| ------------- | ------------- |------------- | ------------- |------------- | ------------- |------------- | ------------- |
| and | as | assert |break |class |continue |def |del |
| elif | else | except |global |is |or |try |break |
| finally | for | if |lambda |pass |while |import |nonlocal |
|raise |with |in | not | return | yeild|

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

## File Explanation
### *Slogan Randomizer*
This is a simple syntax, which when run through multiple instances, creates a randomized sentance on each iteration.

### *Dog Age Calculator*
Simple code to prompt and calculate the age of your dog in human years 
  
