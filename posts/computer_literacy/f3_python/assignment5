---
title: "Assignment 5"
date: 2022-11-19T17:03:43+08:00
draft: false
---

# F3 CL Python Assignment 5: Dictionaries and While-Loops

## What are Dictionaries?

In real life, dictionaries store the definitions of words.  Each word in a language is assigned a definition.  We can then use the dictionaries to look up the definition using the word.

In Python, dictionaries store the *values* of *keys*.  Each *key* is assigned one *value*.  We can then use the dictionaries to look up the *value* of a *key*.

*(Real dictionaries allow words to have more than one definition, but Python only allows each key to store one value.)*

## Basics of Dictionaries

### Constructing Dictionaries

To construct a dictionary, we use curly brackets `{}`.

**Example 1:**

`a = { }`  
This creates an empty dictionary.

Key-value pairs are stored by separating keys and values with a semicolon `:`.  Commas are put between key-value pairs.

**Example 2:**

`b = {"apple": 1, "banana": "yellow"}`  
In this dictionary, there are two key-value pairs.  The key `"apple"` has the value `1`, and the key `"banana"` has the value `"yellow"`.

Strings, numbers, and tuples can be used as **keys** in dictionaries.  *(Tuples are similar to lists, but I won't discuss them here.  Here's a website that explains what tuples are: [https://www.w3schools.com/python/python_tuples.asp](https://www.w3schools.com/python/python_tuples.asp) )*  For the **values** of dictionaries, they can be of any type.  So yes, you can do stuff like this:

**Example 3:**

`c = {"apple": True, "banana": ["yellow", "sweet"], "lemon": {"another dictionary!": "yes this works:)"}, 69: 420}`

### Accessing and Changing Values of Keys

To access the values, we can put the key in square brackets `[]` after the dictionary.  To change the values, set their value with `=` .

**Example 4:**

`b = {"apple": 1, "banana": "yellow"}`  
`print(b["apple"])`  
`b["banana"] = "new value"`  
`print(b["banana"])`  
Output:  
`1`  
`new value`  

However, if the inputted key is not in the dictionary, an error will occur.

**(Incorrect) Example 5:**

`c = {"hello": "world"}`  
`print(c["apple"])`  
Output:  
`Traceback (most recent call last):`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`File "<string>", line 2, in <module>`  
`KeyError: 'apple'`  

To avoid this error, we can use `a.get()`.  It will return `None` if the key is not in the dictionary, and will not cause errors.  

**Example 6:**
`c = {"hello": "world"}`  
`print(c.get("apple"))`  
Output:  
`None`  
As you can see, no error is produced despite the fact that the key `"apple"` is not in dictionary `c`.

## Iterating over Dictionaries

### Method 1:  `a.keys()`

`a.keys()` will return a set of the keys of the dictionary.  We can then use a for-loop to iterate through the keys.

**Example 7:**

`a = {"one": 1, "two": 2, "three": 3}`  
`for i in a.keys():`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`print(k, a[k])`  

### Method 2:  Iterating directly over the dictionary

We can also use a for-loop to directly loop over the dictionary.

**Example 8:**

`a = {"one": 1, "two": 2, "three": 3}`  
`for i in a:`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`print(k, a[k])`  

### Method 3:  `a.items()`

`a.items()` will return a set of `(key, value)` tuples in a `dict_items` object.  *(It’s fine if you don’t understand the previous sentence.)*  But we can still use a for-loop to iterate through it, though slightly differently from previously.

**Example 9:**

`a = {"one": 1, "two": 2, "three": 3}`  
`for k, i in a.items():`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`print(k, i)`  

## Tasks in CL Notes
### Task 1
`chars = {}`   
`for c in "Python Programming is fun": # iterate over each character`   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[ c ] = 1`   
`print( chars.keys() )`   
Output:
`dict_keys(['P', 'y', 't', 'h', 'o', 'n', ' ', 'r', 'g', 'a', 'm', 'i', 's', 'f', 'u'])`  

**Solution:**
The output is a `dict_keys` object containing one of every character in the string `"Python Programming is fun"`, in order of first appearance.  

Notice how there are no duplicates in the `dict_keys` object.  This is because dictionaries cannot contain duplicate keys.

### Task 2
We need to modify the above code to count the number of occurrences of each character present in the string.   
**Expected output:**  
`{'P': 2, 'y': 1, 't': 1, 'h': 1, 'o': 2, 'n': 3, ' ': 3, 'r': 2, 'g': 2, 'a': 1, 'm': 2, 'i': 2, 's': 1, 'f': 1, 'u': 1}`  

When a character appears in the string, we need to add 1 to the corresponding key in the dictionary.  So, we might *(incorrectly)* do this:

**(Incorrect) Example 10:**
`chars = {}`  
`for c in "Python Programming is fun": # iterate over each character`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[c] += 1`
`print(chars)`
Output:
`Traceback (most recent call last)`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`File "c:\Users\nick\Documents\Visual_Studio_Code_Python\Misc\computerclubnotes.py", line 4, in <module>`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[c] += 1`
`KeyError: 'P'`

So we see that an error occurred.  But what went wrong?

Well, we see the error `KeyError: 'P'`.   `KeyError` means that the key (in this case `'P'` ) isn't in the dictionary.  We're trying to access a value that doesn't exist. 

To fix this, we need to check whether the key exists in the dictionary.  One way of doing so is using `in`.

**Solution:**
`chars = {}`
`for c in "Python Programming is fun": # iterate over each character`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`if  c  in  chars:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[c] += 1`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`else:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[c] = 1`
`print(chars)`
Output:
`{'P': 2, 'y': 1, 't': 1, 'h': 1, 'o': 2, 'n': 3, ' ': 3, 'r': 2, 'g': 2, 'a': 1, 'm': 2, 'i': 2, 's': 1, 'f': 1, 'u': 1}`

## What are While-Loops?
While-loops are loops that can be repeated indefinitely.  They execute a set of statements as long as a condition is true.

**Example 11:**
`n = 0`
`while n < 5:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`n += 1`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`print(n)`
Output:
`1`
`2`
`3`
`4`
`5`
Every time the code is looped, the condition `n < 5` is checked.  When n = 5, the condition `n < 5` is no longer `True`, so the while-loop ends.

## Tasks in CL Notes
### Task 3
Given the following code:
`from random import random # random() generates a number between 0 and 1`
`secret = int( random() * 100 ) + 1 # this becomes a number between 1 and 100` 
`guess = int( input( "Guess? (1 - 100) " ) )`
`while guess != secret:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`print("Wrong guess. Please try again.")`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`guess = int( input( "Guess? (1 - 100) " ) )`
`print("Bingo!")`
We need to modify it so that the program tells us whether the guess was too high or too low if it is incorrect.

To do that, we can use if-statements to compare the guess (`guess`) and the answer (`secret`).

**Solution:**
`from random import random`
`secret = int( random() * 100 ) + 1`
`guess = int( input( "Guess? (1 - 100) " ) )`
`while guess != secret:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`print("Wrong guess. Please try again.")`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`if  guess > secret:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`print("Your guess was too high.")`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`else:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`print("Your guess was too low.")`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`guess = int( input( "Guess? (1 - 100) " ) )`
`print("Bingo!")`

## Exercises in CL Notes
### Exercise 1
We need to write a program that asks a user to input a line of text, and output the line of text with duplicates of letters removed, so that only the first occurrence of each letter is retained.

Sample output 1: (user input is italicized) 
`Give me a sentence:` *Programming Python is fun!*
`Duplicates removed: Progamin ythsfu!` 

Sample output 2: (user input is italicized) 
`Give me a sentence:` *Never say never* 
`Duplicates removed: Nevr sayn`

We can reuse our code from Task 2 (see above).  Then, we use `input()` to ask the user for input, and we can print `"Duplicates removed:"` to get this code:

**(Incomplete) Example 12:**
`chars = {}`
`for c in input("Give me a sentence: "): # iterate over each character`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`if c in chars:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[c] += 1`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`else:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[c] = 1`
`print("Duplicates removed:", end=" ")`
`print(chars)`
Output (user input is italicized):
`Give me a sentence:` *apple*
`Duplicates removed: {'a': 1, 'p': 2, 'l': 1, 'e': 1}`

We then need to print out the keys of the dictionary `chars`.  We can simply loop over `chars.keys()` and print each key.

**Solution:**
`chars = {}`
`for c in input("Give me a sentence: "): # iterate over each character`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`if c in chars:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[c] += 1`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`else:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[c] = 1`
`print("Duplicates removed:", end=" ")`
`for i in chars.keys():`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`print(i, end="")`
Output (user input is italicized):
`Give me a sentence:` *apple*
`Duplicates removed: aple`

### Exercise 2
Our task is to write a program that keeps on generating random numbers between 1 and 100 (see Task 3), until one of them appears for the third time. Print the random numbers separated by space while they are generated.

Sample output 1: (note that the last number **9** appears for the third time)
41 27 77 68 39 23 46 56 26 6 34 75 61 25 14 98 86 37 48 48 94 69 1 90
11 85 70 63 42 96 73 62 99 6 **9** 64 92 7 29 11 96 27 **9** 34 92 30 51 89
39 91 68 18 85 2 79 **9**

Sample output 2: (this time it is three **80**'s) 
11 27 16 45 58 16 83 76 98 35 88 **80** 81 66 69 17 57 30 82 19 44 14 100 84 61 34 97 7 32 51 60 70 6 89 7 98 79 31 **80** 14 66 56 4 44 **80**

We again reuse the code from Task 2, modifying it to count the number of occurrences of items in a given list.  Let us store the random numbers in a list called `numbers`.  Adding in the random number generator part, we get:

 **(Incomplete) Example 13:**
`from random import random`
`numbers = [int( random() * 100 ) + 1]`
`chars = {}`
`for c in numbers:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`if c in chars:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[c] += 1`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`else:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[c] = 1`
`print(chars)`
Example output:
`{65: 1}`

Now that we have the number of occurrences of items, we need to check whether there is an item that occurs thrice.  We can simply check whether `3` is in `chars.values()` using `in`.  This will be the condition for the while-loop.

We need a while-loop to append random numbers to the list as long as no item has appeared thrice.  Here is what we get:

**(Incomplete) Example 14:**
`from random import random` 
`numbers = []` 
`chars = {}`  

`while not 3 in chars.values():`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`numbers.append(int( random() * 100 ) + 1)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars = {}` 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`for c in numbers:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`if c in chars:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[c] += 1`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`else:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[c] = 1`


 
`print(chars)`
Example output:
`{35: 1, 79: 2, 74: 1, 3: 3, 32: 1, 50: 1, 25: 2, 78: 1, 63: 1, 49: 2, 59: 1, 48: 1, 7: 1, 30: 1}`

Now, we need to print out the items inside the list `numbers`, separated by spaces.

**Solution:**
`from random import random`
`numbers = []`
`chars = {}`

`while not 3 in chars.values():`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`numbers.append(int( random() * 100 ) + 1)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars = {}`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`for c in numbers:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`if c in chars:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[c] += 1`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`else:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`chars[c] = 1`

`for i in numbers:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`print(i, end=" ")`

## Bonus: Better Ways?
**I know that after seeing this subtitle, 90% of everyone reading this article will click away.**  So for those of you left, let's look at some far more efficient ways to complete the tasks and exercises in the school CL notes!!!

### Task 2 (Efficient Version, Three Lines)
As a reminder, we need to count the number of occurrences of each character present in the string. 
**Example input:** Python Programming is fun
**Expected output:**  `{'P': 2, 'y': 1, 't': 1, 'h': 1, 'o': 2, 'n': 3, ' ': 3, 'r': 2, 'g': 2, 'a': 1, 'm': 2, 'i': 2, 's': 1, 'f': 1, 'u': 1}`  
We used seven lines in our previous solution using dictionaries.  However, we can actually use `count()` to count the occurrence of characters in a string.

**Example 15:**
`a = "Python Programming is fun"`
`print(a.count("P"))`
Output:
`2`

So we just have to loop over each character of the string and put a key-value pair in the dictionary.  Don't forget that duplicates cannot exist in dictionaries, so we don't have to worry about duplicate characters in the string.  So here's the solution, but with three lines only:

**Solution:**
`a = {}`
`for i in "Python Programming is fun": a[i] = "Python Programming is fun".count(i)`
`print(a)`
Output:
`{'P': 2, 'y': 1, 't': 1, 'h': 1, 'o': 2, 'n': 3, ' ': 3, 'r': 2, 'g': 2, 'a': 1, 'm': 2, 'i': 2, 's': 1, 'f': 1, 'u': 1}` 

Yes, it's *sometimes* possible to use for-loops without going to the next line - again, I won't discuss it here.  

### Exercise 1 (Efficient Version, One Line)
Originally, we used nine lines to remove duplicates in a string.

Output (user input is italicized):
`Give me a sentence:` *apple*
`Duplicates removed: aple`

For this one, I'll first give the solution and explain it afterwards.

**Solution:**
`print("Duplicates removed:", "".join(list(dict.fromkeys(input("Give me a sentence: ")))))`

Yes, that's it.  Just one line.

For convenience, I'll color the solution so it's easier to read.  Let's decipher this together, from the inside out.  

<nobr style="color:red">print("Duplicates removed:", </nobr><nobr style="color:orange">"".join(</nobr><nobr style="color:gold">list(</nobr><nobr style="color:limegreen">dict.fromkeys(</nobr><nobr style="color:blue">input("Give me a sentence: ")</nobr><nobr style="color:limegreen">)</nobr><nobr style="color:gold">)</nobr><nobr style="color:orange">)</nobr><nobr style="color:red">)</nobr>

The blue part simply asks for user input.  The green part, `dict.fromkeys()`, generates a dictionary with the keys as the characters of the inputted string.

**Example 16:**
`print(dict.fromkeys("banana"))`
Output:
`{'b': None, 'a': None, 'n': None}`

The yellow part, `list()`, converts the dictionary into a list.

**Example 17:**
`print(list(dict.fromkeys("banana")))`
Output: 
`['b', 'a', 'n']`

The orange part, `"".join()"`, joins the list together into a string.  It has the following syntax: `string_here.join(list_here)`.  It then connects the items inside the list in a new string, separating each item with the string provided.

**Example 18:**
`a = ["apple","banana", "watermelon", "grape"]`
`print("hello".join(a))`
Output:
`applehellobananahellowatermelonhellogrape`

**Example 19:**
`print("".join(list(dict.fromkeys("banana"))))`
Output:
`ban`

Finally, the red part prints everything out.

### Exercise 2 (Efficient Version, Four Lines)
Just now, we used thirteen lines to generate random numbers until one number appeared thrice.

Let's first use a *slightly* easier way to generate random integers.  Introducing `randint()`: to use it, we need to *import* it by running `from random import randint`.  The syntax is `randint(a, b)`, and it will generate a random number between `a` and `b` *(inclusive)*.  So, to generate a random number between 1 and 100, we can simply do `randint(1, 100)`!

Now, to improve on the original solution, we need a fundamentally different approach to this question.  We've been generating random numbers, then counting how many times every number occurred in the list.  But we don't have to do that!  

We actually only need to count how many times the final number appeared.  Think about it: if the one of previous numbers had occurred thrice, the program would've ended already.  So, if we're still generating random numbers, we know that no number has occurred thrice.

To count how many times a number has appeared in the list, we can again use `count()` (introduced earlier).  This time, we'll use it to count the occurrences of an item in a list.

**Example 20:**
`l = [1, 2, 3, 4, 5, 2, 2]`
`print(l.count(2))`
Output:
`3`

So we'll use it to check the occurrences of items in the list.  

**(Incomplete) Example 21:**
`from random import randint`
`l = [randint(1, 100)]`
`while l.count(l[-1]) < 3:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`l.append(randint(1, 100))`
`print(l)`
Example output:
`[56, 85, 56, 4, 37, 41, 27, 59, 55, 7, 94, 99, 88, 94, 40, 5, 81, 22, 18, 100, 27, 57, 38, 68, 81, 30, 42, 46, 68, 2, 89, 61, 55, 50, 73, 70, 61, 81]`

Finally, we need to print the random numbers properly.  We'll use `join` again (see Exercise 1 (Efficient Version) for an explanation on how to use it).  One thing though: `join` won't work on lists with `int` inside them, so we'll need to convert each `int` to `str`.

**Solution:**
`from random import randint`
`l = [str(randint(1, 100))]`
`while l.count(l[-1]) < 3:`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`l.append(str(randint(1, 100)))`
`print(" ".join(l))`
Example output:
`96 59 97 62 80 39 49 12 84 54 72 61 4 39 54 30 36 75 9 41 11 83 48 19 61 14 14 88 8 34 63 11 99 13 88 24 8 87 60 32 94 67 89 29 28 93 24 40 37 67 90 11`

## Further Information
If you've made it here, thank you for reading this guide.  Here are some further references, if you want to read more.

Dictionaries: [https://www.w3schools.com/python/python_dictionaries.asp](https://www.w3schools.com/python/python_dictionaries.asp)
While-loops: [https://www.w3schools.com/python/python_while_loops.asp](https://www.w3schools.com/python/python_while_loops.asp)
`count()`: [https://www.w3schools.com/python/ref_list_count.asp](https://www.w3schools.com/python/ref_list_count.asp)
`str.join()`: [https://www.w3schools.com/python/ref_string_join.asp](https://www.w3schools.com/python/ref_string_join.asp)
