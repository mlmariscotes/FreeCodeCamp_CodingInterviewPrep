## Title Case a Sentence
Return the provided string with the first letter of each word capitalized. Make sure the rest of the word is in lower case.

For the purpose of this exercise, you should also capitalize connecting words like `the` and `of`.

---
```JavaScript
function titleCase(str) {
  let arr = [];
  str.toLowerCase().split(" ").forEach((elem) => {
    let word = elem.charAt(0).toUpperCase() + elem.slice(1);
    arr.push(word)
  });
  return arr.join(" ");
};

titleCase("I'm a little tea pot");
```
