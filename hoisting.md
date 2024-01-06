# Hoisting in JS 

### Hosting is a phenomena in js by which we can access the variables & functions even after we have initialized it or we have put some value in it. We can access it without any error.



1. Hoisting in js is a process in which all the variables, functions and definations are decalred before execution of the code.

2. variables are initialized to "undefined" when they are decalred and functions definations is stored as it is.

3. They are declared in the moemory location phase in the memory components f execution context, So we can use even after they are declared.

4. "Undefined means variables has been declared but value is not "Assigned", but "not defined" means varibale not fined.

5. When we "assign a variable" in "function declartion" we can not call this varibale as function "Before" declaration as it will behave as variable with "undefined" value.

6. Arrow function enact as a variable to get "undefined" during mmeory creation phase while function actually gets run 


Example 
```
a()

function a(){
    console.log("hiii")
}
function a(){
    console.log("bye")
}

Output will be : "bye" 
```


Explanation : 
During the hoisting phase, we look at the function, the compiler says, Oh, yeah, yeah, yep, I'm going to hoist this and I'm going to put this someplace in memory for us.And then it keeps going to the next line and says, Oh, here's function again.I'm going to put this in memory.

And because this even though this is the same thing.Because we're doing it one after another.
It's going to rewrite that place in memory to include console.log bye

So that in this case we've lost the ability to say hi with this function.

We can only say by.

This is the case.


## How funtion works in JS & variables Env 

1. The higher level of GEC(global execution window )on the stack,higher in preferance.

2. GEC is created as the functionis invovled and destroyed as its execution completed.

3. Same variable name but different scope of execution seperates the variable values.



Example 2 : 

```
var favFood = "grapes";

foodthoughts = function(){
    console.log("original food: " + favFood);

    var favFood = "sushi"

     console.log("new fave food: " + favFood);

};

foodthoughts()
```

so what would be the output ? 

explanation : 
```
var faveFood = undefined;
var foodthoughts = undefined;

var favFood = "grapes";

foodthoughts = function(){
    favFood = undefined 
    console.log("original food: " + favFood); // undefiend

    var favFood = "sushi"

     console.log("new fave food: " + favFood); //sushi

};
```


Example 3 :
FYR : https://replit.com/@aneagoie/hoisting-exe#index.js

```
function bigBrother() {
    function littleBrother() {
        return 'it is me!';
    }
    return littleBrother();

    function littleBrother() {
        return 'no me!';
    }
}

console.log(bigBrother()); 

Output will be : 'no me!' 
```



