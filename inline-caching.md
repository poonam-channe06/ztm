# inline caching

function findUser(){
    return `found ${user.firstName} ${user.lastName}`
}

const userData {
    firstName: "Poonam",
    lastName: "Channe"

}

found Poonam Channe 

Now inline caching does something really interesting.

 Due to inline caching done by the compiler code that executes the same method repeatedly, that is,

let's say the find user method or function was being called multiple times.

Well, the compiler can optimize this so that whenever it's looking for the user data, which has first

name and last name, it can use something called inline caching.

Where instead of looking up this object every time, finding the key that is first name and last name,

and then the values it will cache or inline cache.

So that find user just becomes this piece of text.

So if we call find user over and over and over, we would just replace that with found Johnson Jr.

Because at the end of the day, that's all that the function is doing.


 The other one that is really important for optimizing compiler code is something called hidden classes.


