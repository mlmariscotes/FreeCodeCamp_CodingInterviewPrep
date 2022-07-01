## Chunky Monkey
Write a function that splits an array (first argument) into groups the length of size (second argument) and returns them as a two-dimensional array.

---
```JavaScript
// My Solution
function chunkArrayInGroups(arr, size) {
  let group = [];
  let position = 0;
  
  while(position < arr.length) {
    group.push(arr.slice(position, position+=size));
  };
  
  return group;
};

chunkArrayInGroups(["a", "b", "c", "d"], 2);
chunkArrayInGroups([0, 1, 2, 3, 4, 5], 2)

```
