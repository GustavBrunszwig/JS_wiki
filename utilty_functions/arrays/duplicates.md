
1. Remove duplicate elements from array:

```
const filterElements = (array) => {
  return Array.from(new Set(array));
};
```
---
2. Filter objects from array by their duplicate value:

```
const filterDuplicates = (array, key) => {
  const seen = new Set();

  const filteredArr = array.filter((el) => {
    const duplicate = seen.has(el[key]);
    seen.add(el[key]);
    return !duplicate;
  });

  return filteredArr;
};
```

* [CodeSandbox example](https://codesandbox.io/s/filter-duplicates-from-array-kxfddr?file=/src/filter.js)
* [Few more solutions](https://fullstackheroes.com/tutorials/javascript/5-ways-to-remove-duplicate-objects-from-array-based-on-property/)
