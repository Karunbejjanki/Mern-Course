The greetDelayed function uses setTimeout() to print "Hello, Alice!" on the console. However, by the time setTimeout() was executed, the binding to the original object or variable was already lost, turning the output to "Hello, undefined!". An arrow function can be used inside setTimeout() to achieve the required effect: 

`setTimeout(() => { console.log(\Hello, ${this.name}!); }, 1000);`.

 Arrow functions themselves have no this, thereby retaining their context from the outer scope and correctly resolving the desired value.