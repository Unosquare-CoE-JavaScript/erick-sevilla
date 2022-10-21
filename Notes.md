# Async JavaScript Deep Dive

## Section 2

### Synchronous VS Asynchronous

Syncronous code is the default we are using when we start coding on JavaScript, the reazon why it is default it´s because it is easy to undestand, let´s take the following code as example:
```
"use strict";

const test = function() {
    console.log("Start of code");

    alert("Notice Me!");

    console.log("End of code");
};

const test2 = function(){
    console.log("Now I get attention.");
};

test();
test2();

// ___OUTPOUT___
// Start of code
// ** The application displays an alert (Notice Me!)
// Notice Me!
// Now I get attention.
```

The syncronous code is also called blocking code, this is because if the user or any process takes to long to finish all the rest of the execution will be blocked until it finishes, so the program gets blocked

But what if we can react to what the user or any other entity/process does without waiting for it, that will improve the preformance of the execution and the user experience, thats why the asyncronous does.

if we set a **setTimeout(..)** function we can modify our outcome

```
"use strict";

const test = function() {
    setTimeout( {
        console.log("Start of code");

        alert("Notice Me!");

        console.log("End of code");
    }, 1000)
};

const test2 = function(){
    console.log("Now I get attention.");
};

test();
test2();

// ___OUTPOUT___
// Now I get attention.
// Start of code
// ** The application displays an alert (Notice Me!)
// Notice Me!
```

But this way we are still running our code syncronously inside the test function, but globaly speaking, the *setTimeout* uses a **Callback** what basicly does is executing a part of the code only when a confition or a process is complete, in this case is when 1000 miliseconds pases


### Advantages and Disadvantages:
#### Synchronos Code 
**Advantage**: Easy to write and to ureason about
**Disadvantage**: May create blocking code.
**Disadvantage**: Less performant
#### Asynchronos Code 
**Advantage**: Very Performant.
**Advantage**: Eliminates code blocking.
**Disadvantage**: It can be difficult to reason about
**Disadvantage**: Harder to write.

### Event Loop
The purpose of the Event Loop is to all the code is handle, The event loop makes possible to create asynchronous code

## Section 3
### Callbacks
### What is a JavaScript Promise
- An Object with Properties and Methods
- Represents the Eventual Completion (or Failure) of an Asynchronous Operation
- Provides a Resulting Value