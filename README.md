# Python_Notes
Some notes fron "One million arab coders" lessons

## Summary of bash commands
In the preceding command line tutorial, you learned how to execute the following commands:

* ls, which lists the contents of a directory,
* cd, which changes your working directory,
* pwd, which prints your working (current) directory,
* open / start, which opens a file (on Mac or Windows, respectively),
* touch, which creates a new file with a specified extension or file type,
* mkdir, which makes (creates) a new directory,
* rm, which permanently removes a file,
* rmdir, which permanently removes an empty directory,
* rm -r, which permanently removes a directory and its contents (without confirmation), and
* rm -ri, which permanently removes a directory and its contents (with confirmation).

## Backus–Naur form
https://en.wikipedia.org/wiki/Backus%E2%80%93Naur_form

## Manipulating strings
* print a character multiple times
```python
print '-' * 6  #output ------
```
* find a substring
```python
s = 'any_string'
print s.find('z')   #output -1
print s.find('y')   #output  2
print s.find('ny')  #output  1
```
* string slicing
```python
sentence = "any_sentence"
starting_point = sentence.find('went');
print starting_point                     #output -1    
substring = sentence[starting_point-1:]  #output ce
print substring
```

```python
sentence = "A NOUN went on a walk. It can VERB really fast."
noun_starting = sentence.find('NOUN')
verb_starting = sentence.find('VERB')
substring1 = sentence[:noun_starting]
substring2 = sentence[noun_starting+4:verb_starting]
substring3 = sentence[verb_starting+4:]
print 'Substring1:'   #output Substring1:
print substring1      #output A 
print 'Substring2:'   #output Substring2:
print substring2      #output  went on a walk. It can 
print 'Substring3:'   #output Substring3:
print substring3      #output  really fast.
```

* string replacing
```python
str = "this is string example....wow!!! this is really string"
print str.replace("is", "was")       #output: thwas was string example....wow!!! thwas was really string
print str.replace("is", "was", 3)    #output: thwas was string example....wow!!! thwas is really string
```


## Methods  
```python
def say_hello(name):  
    greeting = "Hello " + name + "!"  
    return greeting  
 
print say_hello("Miriam")  
print say_hello("Andy") 
```
## if statement
```python
var1 = 100
if var1:
   print "1 - Got a true expression value"
   print var1
else:
   print "1 - Got a false expression value"
   print var1
"""
1 - Got a true expression value
100
"""
```
       
```python
var = 100
if var == 200:
   print "1 - Got a true expression value"
   print var
elif var == 150:
   print "2 - Got a true expression value"
   print var
elif var == 100:
   print "3 - Got a true expression value"
   print var
else:
   print "4 - Got a false expression value"
   print var
"""
3 - Got a true expression value
100
"""
```

## While loop 
```python
def print_numbers(a):
    i = 0
    while(i < a):
        i = i + 1
        print i

print_numbers(3)
#>>> 1
#>>> 2
#>>> 3
```

## For loop 
```python
from random import randint

def random_verb():
    x = randint(0,1)
    if(x == 0):
        return 'run'
    return 'kayak'

for i in range(5):
    print random_verb()
```

## Lists
```python
print "EXAMPLE 1: We can use for loops to go through a list of strings"
example_list_1 = ['a', 'b', 'c', 'd']
for thing in example_list_1:
    print thing
    

print "EXAMPLE 2: We can use for loops on nested lists too!"
example_list_2 = [['China', 'Beijing'],
                  ['USA'  , 'Washington D.C.'],
                  ['India', 'Delhi']]
for country_with_capital in example_list_2:
    country = country_with_capital[0]
    capital = country_with_capital[1]
    print capital + ' is the capital of ' + country
```
