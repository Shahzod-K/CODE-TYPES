# CODE TYPES

## 1. Synchronous 
## 2. Asynchronous
## 3. new Promise 
## 4. async/await
## 5. try/catch
## 6. fetch/request

## ***Synchronous***

>Synchronous means that code is executed sequentially from top to bottom. Each statement is completed before the next one begins.<br>
As its base JavaScript language is synchronous. Synchronous means the code runs in a particular sequence of instructions given in the program. Each instruction waits for the previous instruction to complete its execution.

```js
const p = document.querySelector("p");
p.innerHTML = 'My name is John';
alert('Text set!')
p.style.color = 'red'
```

## ***Asynchronous***

>Asynchronous programming is a technique that enables your program to start a potentially long-running task and still be able to be responsive to other events while that task runs, rather than having to wait until that task has finished. Once that task has finished, your program is presented with the result.
### ***creat Asynchronous code:***
```js
// 1. Callbacks:
setTimeout(()=>{},0)

// 2. Promise:
let promise = new Promise((resolve,reject)=>{
    // logic
})

// 3. async/await:
async function get(){
    await ...
}
```
>Asynchronous callbacks are functions passed to another function that starts executing code in the background. Typically, when the code in the background finishes, the async callback function is called as a way of notifying and passing on data to the callback function that the background task is finished.
```js
function get(callback){
    setTimeout(()=>{
        callback("Hello world!");
    },2000);
}

get(function(value){
    console.log(value);
});
```

>In JavaScript, a promise is a good way to handle asynchronous operations. It
is used to find out if the asynchronous operation is successfully completed or
not. 
### A promise may have one of three states:
- Pending
- Fulfilled (resolve)
- Rejected

>The Promise() constructor takes a function as an argument. The function also
accepts two functions resolve() and reject().<br>
If the promise returns successfully, the resolve() function is called. And, if an
error occurs, the reject() function is called.

```js
const p = document.querySelector("p");
setTimeout(()=>{
    p.innerHTML = "Hello John"
},5000) // 5000 is milliseconds that will complete task in given time
p.style.color = 'red'
```
