# Python

## Concepts

*IDE Thoughts*

+ neovim (basic Config, Learn as you go) [Setup Neovim](https://mattermost.com/blog/how-to-install-and-set-up-neovim-for-code-editing/)


### Odds and Sods

#### Lists

Lists and ranges , you can create them at one time  
eg...  

```    
trees = [x**2 for x in range(0,31,3)]

```

this will create list without a for loop and you can action on the x (x**2)

Difference between  :

```
1) newpens = pens

2) newpens = pens[:]     # a slice

```

1. this tells python to associate the new variable  
2. now you take a slice out (the full list `[:]`) and newpens is its own independant list

thsws kajd alwjdlka