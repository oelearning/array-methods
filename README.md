# Array Methods

This repo is for document how works the array methods. 

all information is based on the book [JavaScript info](https://javascript.info/)

## Splice

The arr.splice method can **insert, remove and replace** elements

The syntax is:

```
arr.splice(start, deleteCount, [elem1, ..., elemN])
```

it modifies `arr` starting rom the index `start`, removes `deleteCount` elements and then inserts `èlem1, ..., elemN` at their place. Returns the array of removed elements.

Deletion example:

```
let arr = ["I", "study", "JavaScript"];

arr.splice(1, 1); // from index 1, remove 1 element

console.log(arr); // output ["I", "JavaScript"]
```

Deletion and replace example:

```
let arr = ["I", "study", "JavaScript", "right", "now"];

// remove 3 first elements and replace them with another
arr.splice(0, 3, "Let's", "dance");

console.log(arr) // output ["Let's", "dance", "right", "now"]
```

Here we can see that `splice` returns the array of removed elements:

```
let arr = ["I", "study", "JavaScript", "right", "now"];

// remove 2 first elements
let removed = arr.splice(0, 2);

console.log(removed); // "I", "study" <-- array of removed elements
```

Insert example:

```
let arr = ["I", "study", "JavaScript"];

// from index 2
// delete 0 elements
// then insert "complex" and "language"
arr.splice(2, 0, "complex", "language");

console.log(arr); // "I", "study", "complex", "language", "JavaScript"
```

> Note: here and in other array methods, negative indexes are allowed. They specify the position from the end of the array, like here:

```
let arr = [1, 2, 5];

// from index -1 (one step from the end)
// delete 0 elements
// then insert 3 and 4
arr.splice(-1, 0, 3, 4)

console.log(arr) // output [1, 2, 3, 4, 5]
```

## Slice

The syntax is:

```
arr.slice([start], [end])
```

It returns a new array copying to it all items from index `start` to `end` **(not including end)**. Both `start` and `end` can be negative, in that case position from array end is assumed.

For instance:

```
let arr = ["t", "e", "s", "t"];

alert(arr.slice(1, 3)); // e,s (copy from 1 to 2, because not includes the end)

alert(arr.slice(2)): // s,t (copy from 2 till the end)

alert(arr.slice(-2)); // s,t (copy from -2 till the end)
```


