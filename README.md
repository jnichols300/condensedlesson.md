


## Document Object Model 

The [**D**ocument **O**bject **M**odel](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
is a programming interface for HTML.

An HTML *document* is available for us to manipulate as an object, and this object is structured like a tree:



## Accessing the document

`document`
  - `document.head`
  - `document.body`

Each web page loaded in the browser has its own document object. The Document interface serves as an entry point to the web page's content

### Element attributes

`document.body`
  - .children
  - .childNodes
  - .firstChild
  - .lastChild
  - .nextSibling
  - .parentElement
  - .parentNode

Methods are available on any element.

### Methods for selecting elements

- document.getElementById
- document.getElementsByTagName
- document.getElementsByClassName
- document.querySelector
- document.querySelectorAll

## Events

- https://developer.mozilla.org/en-US/docs/Web/API/Event

- .onclick
- .addEventListener
  - click
  - mouseover
- .preventDefault()

## Conditionals (35m /w ex)

// Have an example somewhere where one of the more unusual "falsey" values (e.g., empty string) triggers a conditional.

write and narrate through the following code

```javascript
var age = 24;
if(age < 18) {
  console.log("You're too young to enter this club! Get outta here")
}
else if(age > 18 && age < 21){
  console.log("Come on in! But no Drinking!!")
}
else{
  console.log("Come on in!")
}
```

Conditionals will always follow this pattern. There is a key word(if, else if, else). Followed by an expression that will evaluate to true or false in parentheses. Then followed by code to execute when condition is met.

Broken code example below:

```javascript
var age = 24;
if(age > 21){
  console.log("Come on in!")
}
else if(age > 75){
  console.log("Come on in, but I don't know if this is the place for you!")
}
else{
  console.log("get outta here youngin!")
}
```

# Syntax & Semantic Naming

## Syntax
Variable syntax
    camelCase
  - First letter of first word lowercase. First letter of remaining words uppercase.
  - No spaces or punctuation between words.


### While Loop
```javascript
var i = 0;
while(i < 10){
  console.log(i)
  // don't increment at first
}
```
### For Loop
```javascript
var step;
for (step = 0; step < 5; step++) {
  // Runs 5 times, with values of step 0 through 4.
  console.log('Walking east one step');
}
```

# JS Debugging

## Debugging Javascript

#### The Sources Panel

The Sources panel helps us visualize what's going on when we load JavaScript code. It provides a way for us to debug our code in an interactive way. Follow the steps below to explore the Sources panel:

```
cmd+alt+j
```

- If it is not already selected, select **Sources**.

Take a look:

![chrome](http://s6.postimg.org/5fwewzf0h/298740c0_175f_11e5_84a1_f8c88c3e607a.jpg)

Schema From [Chrome dev tools Website](https://developer.chrome.com/devtools/docs/javascript-debugging)

#### Debugging with breakpoints

A breakpoint is an instruction given to a program via a keyword to pause the execution of a script. The Chrome dev tools let you pause execution of a script and see what's going on.

#### Add and remove breakpoint

On the left side of the panel, click on a line number where you want to stop the execution of the code. The line number will be highlighted with a blue arrow to show the breakpoint.

**Multiple breakpoints**

You can add several breakpoints in the scripts, and everytime a breakpoint is set, the execution will stop. You can enable and disable the breakpoints using the checkboxes on the right sidebar.

It is possible to access a breakpoint by clicking on it in the source on the left.

A breakpoint can be removed by clicking on the blue arrow on the left.

#### Debugger keyword

Another way of setting breakpoints in the code is to use the `debugger` keyword. If the console is open and the interpreter is going through a line in the code that contains `debugger`, then the console will highlight this line and the console will be in the context of the `debugger`.

```javascript
debugger

setTimeout(function(){
  alert("Loaded");
}, 0);
```

The DevTools console drawer will allow you to experiment within the scope of where the debugger is currently paused. Hit the **Esc** key to bring the console into view. The Esc key also closes this drawer.

#### Execution control

This section of the lesson is taken from [Chrome dev tools](https://developer.chrome.com/devtools/docs/javascript-debugging#execution-control)

The execution control buttons are located at the top of the side panels and allow you to step through code. The buttons available are:

- **Continue**: continues code execution until we encounter another breakpoint.
- **Step over**: step through code line-by-line to get insights into how each line affects the variables being updated. Should your code call another function, the debugger won't jump into its code, instead stepping over so that the focus remains on the current function.
- **Step into**: like Step over, however clicking Step into at the function call will cause the debugger to move its execution to the first line in the functions definition.
- **Step out**: having stepped into a function, clicking this will cause the remainder of the function definition to be run and the debugger will move its execution to the parent function.
- **Toggle breakpoints**: toggles breakpoints on/off while leaving their enabled states intact.

There are also several related keyboard shortcuts available in the Sources panel:

| Execution | Shortcut |
|-----------|----------|
| Continue | `F8` or `Command + /` |
| Step over | `F10` or `Command+'` |
| Step into | `F11` or `Command+;`  |
| Step out | `Shift+F11` or `Shift+Command+;` |
| Next call frame | `Ctrl+.` |
| Previous call frame | `Ctrl+,` |

#### Interact with paused breakpoints

Once you have one or more breakpoints set, return to the browser window and interact with your page.

#### Pretty Print option

Most of the time, the JavaScript in a website will be minified, meaning that variable names are condensed and spaces and line breaks are removed. This can make the source code unreadable, and difficult to debug. You can re-format the code using the "Pretty Print" button of the bottom left side of the panel `{}`. This makes the code more easy to read and debug.



