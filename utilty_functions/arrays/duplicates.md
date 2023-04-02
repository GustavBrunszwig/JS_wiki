
1. Remove duplicate elements from array:

```
const filterElements = (array) => {
  return Array.from(new Set(array));
};
```
---
2. Remove duplicate object from array by an object value (**id**):

```
const filterDuplicates = (array) => {
  const seen = new Set();

  const filteredArr = array.filter((el) => {
    const duplicate = seen.has(el.id);
    seen.add(el.id);
    return !duplicate;
  });

  return filteredArr;
};
```

* [CodeSandbox example](https://codesandbox.io/s/filter-duplicates-from-array-kxfddr?file=/src/filter.js)
* [Few more solutions](https://fullstackheroes.com/tutorials/javascript/5-ways-to-remove-duplicate-objects-from-array-based-on-property/)