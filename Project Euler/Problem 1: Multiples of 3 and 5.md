## Problem 1: Multiples of 3 and 5
If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.

Find the sum of all the multiples of 3 or 5 below the provided parameter value `number`.

```JavaScript
// My Solution
function multiplesOf3and5(number) {
  let arr = [];
  for (let i = 0; i < number; i++) {
    if ( i % 3 === 0 || i % 5 ===0) {
      arr.push(i)
    };
  };
  return arr.reduce((a, b) => a+b, 0)
};

multiplesOf3and5(1000);
```
