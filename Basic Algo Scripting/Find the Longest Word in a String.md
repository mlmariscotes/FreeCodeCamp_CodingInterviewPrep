## Find the Longest Word in a String
Return the length of the longest word in the provided sentence.

Your response should be a number.

---
```JavaScript
// My Solution
function findLongestWordLength(str) {
  let arr = [];
  str.split(" ").map((elem) => {
    arr.push(elem.length);
  });

  return Math.max(...arr)
};

findLongestWordLength("The quick brown fox jumped over the lazy dog");
```
