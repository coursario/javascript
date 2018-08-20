# Basics - Array Functions - Reduce

## Description

The `reduce` function transforms given array into
another array, an object or a primitive value.

## Example

It is given the array `a` with:

```javascript
const a = [ 1, 2, 3 ];
```

Transformation into another array:

```javascript
const b = a.reduce((newArray, currentValue) => {
  newArray.push(currentValue);
  return newArray;
}, []);
// result: b === [ 1, 2, 3 ]
```

Transformation into an object:

```javascript
const b = a.reduce((newObject, currentValue) => {
  // key of object will automatically turned into a string:
  newObject[currentValue] = currentValue;
  return newArray;
}, []);
// result: b === { '1': 1, '2': 2, '3': 3 }
```

Transformation into a number (sum):

```javascript
const b = a.reduce((accumulatedSum, currentValue) => {
  accumulatedSum += currentValue;
  return accumulatedSum;
}, []);
// result: b === 6
```

