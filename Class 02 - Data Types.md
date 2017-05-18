# Data Types 
Objectives: 
- Describe data types in JS
- Work with data stored in variables 
- Work with arrays 

**Review**:
Upstream is moving data from your remote, local fork into the master/origin. You set your origin and upstream - and that's how you identify where you push and pull from. 

Use variables to store data AND give data meaning. i.e. what is `6` in a given program? Number? Or a string of information? 

## Variables 
three ways to set variables
1. var => `var someVariable = 'hello'` (es4 - var can end up being either the below, the worse of both worlds)
2. let=> `let myFirstVariable = 'Hello World'` (can be reassigned) 
3. constant => `const mySecondVariable = 5` (permenant - cannot be changed - mostly what you want to use)

To invoke a variable, simply print it 
`console.log(myFirstVariable);` => Hello World 

**Checking Data Types**
Categories of data you can work with in your program. You'll be working with the values of data and operators to manipulate it. 
- What values constitute this data type?
- What operators can we perform with this data? 

## Numeric Data
Numeric Values are
- Integers
- Floats
- Coordinates 

Which can get arithmetic operators

**Arimetiic Operators**
All use a data object called `Math`! 
- `Math.abs()` will return an sbolute value 
- `Math.pow( 3, 2 )` will return exponent
- `Math.sqrt( 4 )`  will return squareroot 
- `Math.random ( )` will return a number between 0 and 1, unless you put two numbers. 
- `Math.round ( )` will round a number
- `Math.floor ( )` can randomize 

Neat way to do a random number generator:
```
// How might I get a random number between 0 and 10?
// method 2

const max = 10
const min = 1

const randomNumber = Math.floor (Math.random () * ( max - min + 1) + min)

console.log (randomNumber)
```
## Strings 

The value of any string data is any text from two quotes. Any quotes work, so long as your consistent in a given phrase. 

**Concatonation!** 
Will allow you to apply operators to strings. Order of operations still happen here! "Strings trump numbers" here. 

**Interpolation**
The backtick can be used to establish a template. You can use `${variableName}` inside of a string to call out something in JS inside the string itself, to make it easier to read:

```
let myName = 'Zakk'
console.log( `Hi! My name is - What? My name is ${myName}!` )
```
The $ sign indicates string interpolation, and comes from Ruby. 

**String Methods**
Methods are a function inside of an object. 
`console` + `.log` = passes the log method to console to print data

## Booleans 
Truthy and Falsy => just because a condition can evaluate as true/false does not necessarily mean its boolean values are the same. 
- There is a logical and `&&` - where both left and right side need to be true 
- Logical OR `||` only one side 
- Logical not `!true` or `!false`


---

**Tips** 
- You probably don't need to include `;` since the compiler can tell when it is or isn't necessary 
- If you try to reassign a `const` variable, it will fail to run (and will tell you the file, and the line, the error took place in) 
- variables using `let` takes more memory than `const` ?_?
- JS typically coerces things into strings because its more reliable




