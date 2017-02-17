


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
