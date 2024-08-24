# Python

[Odds / Randoms](#odds_//_randoms)
[Lists](#lists)

## Concepts

## Odds / Randoms
*IDE Thoughts*

- *neovim (basic Config, Learn as you go) [Setup Neovim](https://mattermost.com/blog/how-to-install-and-set-up-neovim-for-code-editing/)*

How to get print() not to add `\n`

use te following
```
print(f"thing",end="")
print("thing",end="")

```

## Lists

Lists and ranges , you can create them at one time  
eg...

```
trees = [x**2 for x in range(0,31,3)]

```

this will create list without a for loop and you can action on the x (x\*\*2)

Difference between :

```
1) newpens = pens

2) newpens = pens[:]     # a slice

```

1.  this tells python to associate the new variable
2.  now you take a slice out (the full list `[:]`) and newpens is its own independent list

**Empty string checker:**

```
listthing = []

if listthing:

```

This evaluates as a bolean ( True / False)