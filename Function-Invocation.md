## Function expression

var india = function(){
    console.log("Jai shree ram");
}

or 
var india = () =>{
    console.log("Jai shree ram");
}

## Function Declaration

function canada(){
    console.log("Merry christmas");
}

## Function call / execution
india()  -- This function gets defined at pasttime that is when compiler loos at the code and start hoisting and allocating memory 
canada() -- 

This function is defined at runtime.
when we actually run the function or call the function or to execute the function or invoke the funtion.



When a function is invoked, well, we create a new execution context on top of our global execution context.And we get a few things.We get the "this" keyword,

But unlike the global execution context that gave us a global object that equals to this.

Instead, with a function invocation, we get something called arguments, and that's another key word in JavaScript.
