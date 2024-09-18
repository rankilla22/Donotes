# Python

[Odds / Randoms](#odds_//_randoms)
[Lists](#lists) 

## Problems to Solve

* have a think

## Odds / Randoms

### *IDE Thoughts*

- *neovim (basic Config, Learn as you go) [Setup Neovim](https://mattermost.com/blog/how-to-install-and-set-up-neovim-for-code-editing/)*

# Python Concepts

## Print()

How to get print() not to add `\n`

use te following

```python
print(f"thing",end="")
print("thing",end="")
```

## Lists

Lists and ranges , you can create them at one time
eg...

```python
trees = [x**2 for x in range(0,31,3)]
```

this will create list without a for loop and you can action on the x (x\*\*2)

Difference between :

```python
1) newpens = pens

2) newpens = pens[:]     # a slice
```

1. this tells python to associate the new variable
2. now you take a slice out (the full list `[:]`) and newpens is its own independent list
3. <mark>NB Avoid this if lists are large saves memory and time</mark>

**Empty string checker:**

```python
listthing = []

if listthing:
```

This evaluates as a bolean ( True / False)

```python
countries = ["Brazil", "Japan", "Canada", "Australia", "South Africa"]


while countries:
    single = countries.pop();
    print(f"{single}")

print(f"\n{countries}")
```

Using a while clause to test if the string is empty, use this <u>when manipulating lists</u>

## Dictionaries

### Get()

Prints key value, and can set a default value if there is none

```python
my_dict = {
    "name": "Alice",
    "age": 30,
    "city": Cape Town,
    "is_student": True,
    "favorite_color": "blue"
}

print(get(my_dict['Town',"not available"])
```

this will return

```python
"Not Available"
```

### SET()

```python
key_value_pairs = [
    "name":"Alice",
    "age": 35,
    "city": "New York",
    "is_student": True,
    "favorite_color": "blue",
    "age": 25,
    "city": "London",
    "is_student": False,
    "age2": 35,   # Duplicate key 'age'
]


for v in set(key_value_pairs.values())
    print(v)
```

returns all the unique values eg:

```python
False
Alice
35
London
blue
25
```

## While

Use flags

```python
flag = True


while flag:
    doo foo:
```

## Functions

Styling Guide:     

* descriptive and in all lowercase and underscores

* a `'''comment'''` must be the first line after the `def`

* if you use defaults do not use spaces eg :
  
  `def func_name(para_0,para_1='default value')`

                              

                        

## Lists

```python
phrases = [
    "Hello, world!",
    "Keep it simple.",
    "Never give up.",
    "Learn every day.",
    "Coding is fun.",
    "Think outside the box.",
    "Dream big.",
    "Believe in yourself.",
    "Embrace challenges.",
    "Stay positive."
]
sent_models = []

def show_messages(lista):
    for phrase in lista:
        print(f"{phrase}")

def send_messages(lista,listb):
    lista2 = lista[:] # avoid doing this if lists are big saves memory and speed
    while lista2:
        message = lista2.pop()
        listb.append(message)
        print(message)

show_messages(phrases)

send_messages(phrases,sent_models)

print(phrases)
print(sent_models)
```

* Showing the difference of `For` and `while`

* `while` is used when manipulating lists 

### 

### Passing and arbitrary number of arguments

```py
def pizza_topping(size,*toppings): # this create a tuple
    #print the list of topping given above
    print(toppings)
```

<u>this must always be the last in the function definition</u>

* NB you will often see `*args` which collects arbitrary positional arguments like this

### Using Arbitrary Keyword arguments

```py
def build_profile(first,last,**user_info):
    #Build a dict containing everything we know about a user
    user_info['frist_name'] = first
    user_info['last_name'] = last
    return user_info

user_profile = build_profile('Albert','Einstien',local='germany',
                hair='spiky')

print(user_profile)
```

* NB you will often see the parameter name `**kwargs` used to collect non-specific keyword arguments

## Module

Styling Guide: descriptive and in all lowercase and underscores

```py
import pizza as p
from pizza import pizza_topping as ptop
from pizza import * #can call the functions directly
```

## Classes

Styling guide :

* capitalize `class Dog:`

a function that's part of a class is called a method
