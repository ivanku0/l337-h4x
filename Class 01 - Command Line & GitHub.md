# Class 01 - Lets learn about git & github 
- learning how to work in the terminal
- learn the basics of git and github 

## Goals
- navigating using the terminal
- manage a local repo in git 
- fork a repo
- clone a repo
- make a pull request on a repo 

Terminals predate GUI but serve as a text-based navigation system. "Character based
It is also easy to automate via bash scripting! -- More expert friendly than beginner friendly. 

- $ in the terminal is the prompt
- command
- input (Contains flags like -f )
- output (from running commands)

## Commands
- `pwd` (print working directory - absolute directory defines it from root to current folder)
- `ls` (lists all files in the current directory)
- `-a` will flag and list everything, including hidden files 
- `-l"`will flag and list attributes 
- you can include `ls` with a directory to list the files in a directory 
- `cd` changes the directory and cna takes a directory 
  - many commands have an assumed input. for example `cd` - with no input - takes you to root. 
 
**Command Shortcuts for Navigation** 
Add spaces after CD plus the below
- `./` curent directory 
- `../` up one directory 
- `../../` up two directories
- `/` goes to root 
- `~/` goes to home directory 

**file management commands**
- `mkdir` creates a directory but requires a filename 
- `rmdir` deletes a directory 
- `touch` creates a file
-- `touch` can take in more than one file in a single command. you can use this to create multiple files in a single command. 
- you can pass a `{01,02,03}` as a comma separated list and attach it toa file type like `.md` to create a series of enumerated files
- `rm` removes files. 
- `mv` will rename - is actually "move?"  - takes input, which takes the file you want to move, and where you want to move it to. assumes paths are relevant to current location. - 
- `cp` stands for copy - it takes two arguments: 1 - the path for the file you want to copy and 2 - the path you want to copy it to
  - Copying a directory requires you to pass `r` flag to it which stands for recursive. Any time you deal with a directory - pass `r` to make sure it happens since typical management of a directory has problems without `r`. Recursive will delete everything in that folder. 
- `f` stands for force - you can catonate `r` with `f` into `rf`  
- `trash` will acutally move things 

## Misc learnings
Fun Tip - you can edit your bash profile to alter the way your command line is expressed. We need to update it to support `> `

Spaces separate arguments! 

`clear` clears the terminal
`nano .bash_profile` will let you access your bash profile settings. 
`nano` is a text editor for the command line 
`open` will open a file. 
`open .` will open a directory 

# GitHub

Git is a version control system (precedes github by alot) 
GitHub is a Saas tool for working with git. Like mecurial, but GitHub is best 
## Git Overview
- allows you to track changes line by line 
- creating and working with a repostiroy 
- forking a repo (makes a copy on their server) 
- cloning a repo (move it to be local)

## What is VCS (Version Control)? 

Master -> Fork -> Local 
Pull Request is how you submit changes to the master app. Pull to get changes. 

`git fetch` finds any changes - `merge` will merge the code base. `git pull` merge and fetch but runs fetch merge -> so you can decide what you want to do with the pulled data. 

- repository - folder where git manages changes and history 
-  local version of the repo on your machine
- remote/origin shared version of the repo hosted on a server 
- fork - snapshot or copy of a repo 
- pull request - submitting changes from a fork to be merged  (into master)
- upstream - original repo of a forked repository. set if there are any changes different from the master, it will allow you to pull it back. 

## Git Commands 

- `git init` initiates a new repository out of your current relative path (current directory) 
- `git status` tells us the status of our repo
- `git add` + `path or files` you want to add 
- write `git add .` to add everything in a directory with the period
- or `git add -a` to add everything and everything
- or `git add /directory/` 

Adding files and Saving our files is - adding and commiting 
1. Adding with `git add`
2. Then, `git commit` with a message describing what we're saving with `git commit -m "some text descriptor"` (forgetting `-m` will take you into Vim)
4. You can use "rim raf" which is `rm -rf` to kill the repository you're in and remove it from version control

If stuck in Vim..use 
- `:q!` quit without save 
- `:wq` save and quit
- press `escape` to gtfo 
- 
You can also write
- `echo` and `>> [file name]` to write string into a file

---

# Notes from the reading 

## Intro to Programming and JS
- beautiful programming maintains the complexity of the program. that's where the art is - making a complicated program managable and understandable. 

- make sure ot understand example programs in the lessons. it will be difficult but keep at it. 
- a good proramming language helps the programmer by allowing them to talk about the ations that the computer has to perform on a higher level. it avoids unitneresting details, provides building blocks (functions or operators), and lets you efine your own building blocks 

## Chapter 01 - Data Values
- due to the way bits are stored in JS and our machines, arithmetic or any usage of values of 9 quadrillion (someting like tat) should be consiered rough approximations and not precise math
- same goes for any use of `infinity` or `-infinity` these are rough approximations are not very precise 
- To include a linebreak or tab in a string, you must include a backslash `\` operator to _escape_ the character. For example, use `n` after a backslash as `\n` to add a "newline" line break and add a `t` as `\t` to insert a tab character. You might write that as `This is the first line. \nAnd this is the second!`
- If you want to actually just have a backslash, write it twice like `\\` 
- You can combine (concatenate) strings by using the `+` operator 
- There is also `NaN` which is not a number 

### Unitary Operators
- Operators can be written as words, like the `typeof` operator, which tells you if a given paramter is a string or number, etc. Note this only takes one value and is consideredd a **unary operator**
 - You can use the negative `-` as a uniary operator to turn any value into negative 
 
``` 
var x = 10
console.log (-x)
// -10
```
- There are also **binary operators** which take two values 

### Boolean Operators
Just as any other language - boolean means on and off or yes or no. The values used to express this are true and false
- You can produce boolean by comparing numbers 
  - `console.log(3 > 2)` = true
  - `console.log(3 < 2)` = false
  - You can compare strings in this way, which will compare the value of each character as it is represented in **Unicode** 

-  Some possible operators are
   - `>=` greater than or equal to
   - `<=` less than or equal to
   - `==` equal to
   - `!=` not equal to

### Logical Operators 
Javascript supports three logia loperators `and`, `or`, and `not`. There is also the logical `&&` (and) operator. These are all used to "reason" about booleans. `&&` is a binary operator and result is true oNLY if both the values given to it are true. 

```
console.log(true && false)
// > false
console.log(true && true)
// > true 
```
The `||` operator denotes the logical "or". It produces true if either of hte values given to is true. _Not_ is also writen as an exclamation mark `!`. It is a unary operator that flips the value given to it -- `!True` produces false and `!False` produces true. 

**The PEMDAS of JS Operators**
1. `>`, `==`, etc.
2. `&&`
3. `||`

Remembering the above allows you to minimize the use of parenthesis. The last logical operator is _ternarny_ and takes three values. It is written with a question mark and a colon.

```
console.log (true ? 1 : 2);
// -> 1
console.log (false ? 1 : 2);
// -> 2
```
This is the conditional operator (or just ternary, since it's the only one of its kind in jS). The value on the left of the question mark picks which of the other two comes out *** When it is true, the middle value is chosen, and when it is false, the value on the right is chosen. 

## Undefined Values 
There are two special values written as **null** and **undefined**. Indicats the absence of a meaningful value. Sometimes, a function will produce **undefined** if needs to produce a value, but the value itself does not have much meaning.

There typically is no difference between undefined and null. It is useful to assume they are interchangable. 

## Automatic Type Conversion
JavaScript often converts values into things that make sense in order to make the function or script run correctly, like the below. It uses rules that aren't expected, which is known as _type coercion_. 
`console.log("5"-1)` > 4 
`console.log("5"+1)` > 51

If it tries to make a conversion that doesn't make sense, it will return a `NaN` 
`console.log("five"+2)` > NaN

If you see a `NaN` in an unexpected place, it is likely due an accidental type conversion. Generally, JS tries to convert one data type on one side of the operator the other. 

If `null` or `undefined` occurs on either sie of the operator, it will _only_ be true if both sides are either `null` or `undefined`. 

```
console.log(null == undefined);
// > true
console.log(null == 0);
// > false 
```
This is useful if you want to test whether a value has a real value instead of null or undefine, you can simply compare it to null with the == (or !=) operator. 
If you want to compare values to something precise like `false`: `0`, `NaN`, and the empty string `("")` count as `false`. Other values will be counted as `true`. 

For super precise comparison, you can also use `===` and `!==` which will test if two values are exactly the same 
`("") === false` > false

## Weird Logical Operator Behavior (Short Circuiting)

The `||` operator will convert either side of its binary values and return different things depending on what it's given. The `||` operator for example, will retur the value to its left whe nthat can be converted to true and will return the value on its right otherwise. This conversion works as you'd expect for Boolean and actually gives you a way to provide default values*** for certain functions. 
```
console.log(null || "user")
// > user
console.log("Karl" || "user")
// > Karl
```
If you give it an expression that might produce an empty value on the left, the value on the right will be used as a replacement in that case.  The `&&` operator works this same way but the other way around. It the value on the left converts to false, it returns that value, and otherwise it returns the value on its right. 

**Short Circuiting**
When using the above operators, if a boolean is already included in it, then the operator will not evaluate anything and simply accept the boolean value. For example 1 and X in the following snippets are ignored. 
```
True || 1 
> true
False && X
> False 
```
The conditional operator works the same way. The first expression is always evaluated, but the second or third value, whichever the one that is not picked, is not. 










 

