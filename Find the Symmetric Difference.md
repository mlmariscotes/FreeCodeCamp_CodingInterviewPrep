## Find the Symmetric Difference

The mathematical term symmetric difference `(△ or ⊕)` of two sets is the set of elements which are in either of the two sets but not in both. For example, for sets A = {1, 2, 3} and B = {2, 3, 4}, A △ B = {1, 4}.

Symmetric difference is a binary operation, which means it operates on only two elements. So to evaluate an expression involving symmetric differences among three elements (A △ B △ C), you must complete one operation at a time. Thus, for sets A and B above, and C = {2, 3}, A △ B △ C = (A △ B) △ C = {1, 4} △ {2, 3} = {1, 2, 3, 4}.

- Create a function that takes two or more arrays and returns an array of their symmetric difference. The returned array must contain only unique values (no duplicates).

---
#### `My Solution`
```JavaScript
// Finding symmetric difference
const diff = (arr1, arr2) => {
  const arrA = arr1.filter((elem) => !arr2.includes(elem));
  const arrB = arr2.filter((elem) => !arr1.includes(elem)); 
  return [...arrA, ...arrB].sort();
};

// Reducing to one array
function sym(...args) {
  if (args.length === 0 || args.length === 1) return args.flat(1).sort();
  while (args.length > 1) {
    const arrC = diff(args[0], args[1]);
    args = [arrC, ...args.slice(2)]; 
  };
  const x =  new Set([...args[0].sort()]);
  return [...x];
};

/*
===For Testing Code====
*/
// console.log(sym([1, 1, 2, 5], [2, 2, 3, 5], [3, 4, 5, 5]))
// console.log(sym([1, 2, 3, 3], [5, 2, 1, 4]))
// sym([1, 2, 3, 3], [5, 2, 1, 4])
// console.log(sym([1, 2, 3, 3], [5, 2, 1, 4]))
// diff([1, 2, 3], [5, 2, 1, 4]);
// console.log(sym([1, 2, 3], [5, 2, 1, 4]));
// console.log(sym([1, 2, 3]));


```
