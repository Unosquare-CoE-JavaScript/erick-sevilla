# You don´t know JavaScript Yet - Getting Started


## Chapter 1: WhatIsJavaScript?

### What’s With That Name? 
JavaScript was mainly purposed to be used by Java developers and have some statements similar to it but as Jeremy Jerith said on 2009: 
>"Java is to JavaScript as ham is to hamster".

at the end, the JavaScript name ended being just a marketing decision after the TC39 committee (The committee in charge of manage JS regulations) formalized the name by the ECMA standards as ECMAScript, so is correct to call JavaScript: JavaScript, JS, ECMAScript or ES2019. 
 
 
### The Web Rules Everything About (JS) 
JS is attached to the web specifications since it is implemented for web browsers (with some mismatch exceptions) but in general all the TC39 will have to simply choose to conform the specifications to the reality of the web. 
One of the solutions for those exceptions was the Appendix B that long story short it allowed to detail about any known mismatches between the oldest JS specifications and the reality of JS just on the web JS, the rest of the JS environment must follow the defined rules. 
 
 
### Not all (Web) JS... 
There are some functions and object methods JS-looking that obey the JS syntax but they are controlled by the environment running JS, those elements are responsible of the majority of the cross-platform inconsistency complaints but it is actually due to the difference between those environment behaviors, not how JS itself works. 
 
 
### It´s Not Always JS 
Even if the console/REPL (Read-Evaluate-Print-Loop) in the browser´s Developer tools feels like a JS environment, it is not. Developer tool's purpose is making the developers life easier but we can´t and shouldn't expect those tools to always adhere strictly to the way JS programs are handled, the developer console is not trying to pretend to be a JS compiler so we shouldn´t trust the developer console behavior as an exact to the letter JS semantics. Instead think of it like just a "JS-Friendly" environment. 
 
 
### Many Faces 
The paradigms on the programming language are oriented mostly like a guide and mold for the programmers to approach problems and solutions and how they structure their code. There are 3 typical paradigm-level categories: 
    - Procedural (top to down linear progression code following a line of procedures) 
    - Object Oriented (Collecting logic and data into units called classes) 
    - Functional Programming (organize the code into functions and adaptation to those functions into variables) 
In that matter, JS is most definitely a multi-paradigm language because it can approach problems and take decisions for the solutions line by line using procedural code, class-oriented or even functional programming. 
 
 
### Backwards & Forwards 
There are 2 types of realize/update compatibilities on the languages around the programming languages, those are Backwards and Forwards 
The Backwards compatibility refers that once something is released it won't become invalid in the future, that means that on the programs coded on the 90´s can and will work on the current engine 
The Forwards compatibility refers that including a new addition on the language on a program would not cause that program to break if it were in an older engine, that means that a program created on 2019 should work on a 2010 engine, it may not recognize some of the newest features of the language but the program won't break 
Despite many wishing or myths, JS IS NOT FORWARDS COMPATIBLE, so if we try to run a 90s JS program on today´s engine or environment it will work just fine but if we want to run a program wrote today on a 90s environment it won't work 
 
 
### Jumping the Gaps 
Since JS is not forwards-compatible, it means there will be always a gap between the new TC39 implementations and the oldest versions of the engine, that does not mean that the developers have to code with the old syntax on their projects, for that matter exists the "Transpilers" that are in charge of convert from that newer JS syntax version to an equivalent oldest syntax, this is because it is strongly recommended that the developers use the lasts version of JS so their code is clean an communicates its ideas most efficiently even if the engines that they are using are older, so we have to thank the transpilrs like Babel 
 
 
### Filling the Gaps 
Also, since JS is not forward-compatible, and if we are not talking about just a syntax gap we can fall into a function gap issue, or example if we want to use a ES2019 feature on a pre-ES2019 environment an error would occur, to solve this issue we can use the named "polyfill" patterns, that basically prevents the code to fail if it is implemented on an older engine by adding conditionals to circle back the code on oldest ways in case the new statements fails. 
 
 
### What´s in an Interpretations? 
JS is more compiled than interpreted language 
JS is "parsed" 
The compile process is formed  
Steps of the entire flow of a JS source program: 
- After it leaves the IDE it gets transpiled by Babel, Packed by Webpac and gets delivered to the JS engine 
- The JS engine parses the code to an AST (Abstract Syntax Tree) 
- Then the AST is converted to a kind of Byte code which gets refined by the JIT (Just in time) compiler 
- Finally, the JS Virtual Machine executes the program 
  
 
### Strictly Speaking 
At 2009 JS added the *strict mode*, the benefits of it still not by default sadly but it is a very useful mode to program on JS, I is bassicly a set of rules or best practices (A guide) to optimize and clean the code, with out those rules the program will still be able to execute but without the same performance and not exploiting the maximum power of JS, that´s why it still an optional setup.
```
// only whitespace and comments are allowed
// before the use-strict pragma
"use strict";
// the rest of the file runs in strict mode
```




## Chapter 2: Surveying JS

### Values
In JavaScript there are two main xtypes of values, the *Primitive* and *Objects*, the primitive types are the type of values set as a singule value that could be a number, string, boolean, etc.
```
let string = "My name is Kyle.";
```
On this example, the value "My name is Kyle." is a promotive sting literal usally used to represent words and sentences.

Object in othe hand is a set of diferent primitive values arrange on an element that could be an "Key Object" or an "Array" for example.
```
let names = ["Frank","Kyle","Peter","Susan"];
```
On this other example we can see the set of different strings into an Array that can provide all the strings that are into it arranged on a index structure.}

### Value Type Determination
For distinguishing values, the **typeofo** perator tells you itsbuilt-in type, if primitive, or"object"otherwise:
```
typeof42;// "number"
typeof"abc";// "string"
typeoftrue;// "boolean"
typeofundefined;// "undefined"
typeofnull;// "object" -- oops, bug!
typeof{"a":1};// "object"
typeof[1,2,3];// "object"
typeoffunctionhello(){};// "function"
```

### How We Organize in JS

#### Classes
#### Class Ingeritance
#### Modules
#### Classic Modules
#### ES Modules


## Chapter 3: Digging tothe Roots of JS
### Iterators
### Consuming Iterators
### Iterables
### Closure
### "this" Keyword
### Prototypes

## Chapter 4: The BiggerPicture
### Pillar 1: Scope and Closure
### Pillar 2: Prototypes
### Pillar 3: Types and Coercion