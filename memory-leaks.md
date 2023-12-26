# Memory Leaks

1. memory leaks are pieces of memory that the applcation have used in the past, but is not needed any longer, but has not yet been returned back to us.


let array = [];
for (let i=5; i>1; i++){
    array.push(i-1)
}

1.Now, when I run this code, what's going to happen is we're going to run an infinite loop that keeps pushing to the array.I minus one over and over and over until well, we fill up our memory and there's nothing left for us to use.And well, we're going to crash the browser.

2.But what I did was I filled up our memory heap with more and more and more data.The garbage collection wasn't really working because, well, we had this array.We were using this array over and over until we crashed our program.

3.So memory leaks are pieces of memory that the application have used in the past, but is not needed any longer, but has not yet been returned back to us to the pool of free memory.

## Keep in mind that the execution of the loop also aided in the crash.


### Global variable 
var a = 1;
var b = 1;
var c = 1;

### Event listeners

var element = document.getElementById('button');
element.addEventListerners('click',onClick);

1. In our browser and let's say I select the button.And with this button, I'm going to add an event listener.That's going to listen on the click event and it's going to do some function that, well, I'll just. call it on click.

2. We don't really have it here, but it's going to have that.Now, this is one of the most common ways to leak memory, and that is you add these event listeners and you never remove them when you don't need them.So that you keep adding, keep adding, keep adding event listeners.
And because they're just there in the background, you forget about them.And next thing you know, you create a memory leak.

3. This happens a lot, especially if you go back and forth between single page applications where you're not removing the event listeners off the page.And as a user goes back and forth, back and forth, the memory keeps increasing more and more as more event listeners are added.


- memory is limited.That is when it comes to call stack and memory heap.

- Those are two places that JavaScript remembers or stores memory and we have limited use of them.

- So for us to write efficient code, we have to be conscious to not have a stack overflow or a memory leak and to manage that memory well.

