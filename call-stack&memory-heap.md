# CallStack & Memory Heap

we need a place to store and wriete info.
that is to store our variabke , our objectes our data of our apps, and a place to actually run and kepp track of whats happening line by line on our code ,
so we use call stack and memory heap for that.


1. we need the memory heap as a place to store and write info bcoz at the end of the day all programs just read and write operations.
2. that way we have to place to allocate memory use memory and release memory.
--
3. and with the stack we need aplace to keep a track of where we are in the code so what we can run the code in order.
4. Memory heap is the where memory allocation happens and the call stack is where h engine keeps a track of where your code is in its exceution.

## call stack + memory heap 

const bumber = 10; // allocate memory for number
const string = "poonam" // allocate memory for string
const info = {         // allocate memory for an object and its values 
    name: "poonam",
    "lastname: "channe"
}

