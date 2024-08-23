# Understanding JavaScript Closures

Closures are functions that can access variables from their outer scope even after the outer function has finished executing.

## Example
```javascript
function outer() {
    let count = 0;
    return function inner() {
        count++;
        console.log(count);
    }
}

const counter = outer();
counter(); // 1
counter(); // 2
