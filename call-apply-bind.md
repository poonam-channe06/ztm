# call(), apply(), bind()

```let name ={
    firstName: "poonam",
    lastName: "channe",
    printfullName: function() {
        console.log(this.firstName + " " + this.lastName)
    }
}

name.printfullName();

Result : Poonam channe



let name2 = {
        firstName: "Prashant",
    lastName: "channe",
}

```



#### if we have to print name2 , so one method could be we just copy pasted the printfullName funtion inside name2 object , but thats not the good way to do it. 

So thats where the call method comes into picture 

## Function borrowing  - Call() Method


1. using call function we can do function borrowing 

2. we can borrow the functions from other objects and use it with the data of some other objects 


3. take the fucntion that needs to be called i.e.name.printFullname.call()
in above first arguemnt will be he referance , what we want needs to be pointing to 

```
name.printFullname.call(name2)

Result : Prashant channe 

```


## OR WE can do it in other ways 


```
let name ={
    firstName: "poonam",
    lastName: "channe",
    homeTown : "Mumbai"
}

let printfullName = function(hoemtwon){
      console.log(this.firstName + " " + this.lastName + hometown)
}

pritfullName.call(name, hometwon)

Result : Poonam channe Mumbai


let name2 = {
        firstName: "Prashant",
    lastName: "channe",
    homeTown : "Pune"
}


pritfullName.call(name2)

Result :  Prashant channe Pune 

```

## apply() Method : 


```
pritfullName.call(name2, ["Mumbai", "maharastra"])
```

Insted of call we use apply here , the only differeence is that we can pass these 2nd arguments in array list 


## bind() Method 


bind() looks exactly the same as call method , the onlt difference is instaed of directlt calling this method , bind() method printFullName with object and return the copy of that method 


```
let printMyName = printFullName.bind(name2, "Mumbai, "maharasgtra")
```

This is basiclly used to bind and keep a copy of that method and use it later, the only differnece between the bind and call is like it gives you the copy but which can be invoke later rather than directly  invoking it where ever we are wrting this line of code (pritfullName)



