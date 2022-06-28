## Problem 3: Largest prime factor
The prime factors of 13195 are 5, 7, 13 and 29.

What is the largest prime factor of the given `number?`

https://www.freecodecamp.org/learn/coding-interview-prep/project-euler/problem-3-largest-prime-factor

```JavaScript
function largestPrimeFactor(number) {
  // Getting the all the prime factor
  function primeFactors(n) {
    const factors = [];
    let divisor = 2;

    while (n >= 2) {
      if (n % divisor == 0) {
        factors.push(divisor);
        n = n / divisor;
      } else {
        divisor++;
      };
    };
    return factors;
  };

  return Math.max(...primeFactors(number))
};
```
