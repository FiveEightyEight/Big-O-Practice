# Big-O

## Part 1

```javascript
const func1 = (n) => {
  for (let i = 0; i < n; i++) {
    console.log(n);
  }
}
```
- Time Complexity: O(n)
- Space Complexity: O(1)
---

```javascript
const func2 = (arr) => {
  for (let i = 0; i < arr.length; i++) {
    console.log(arr[i]);
  }
}
```
- Time Complexity: O(n)
- Space Complexity: O(1)
---
```javascript
const func3 = (arr) => {
  for (let v of arr) {
    console.log(v);
  }
}
```
- Time Complexity: O(n)
- Space Complexity: O(1)
---
```javascript
const func4 = (arr) => {
  for (let i = 0; i < 5; i++) {
    console.log(i);
  }
}
```
- Time Complexity: O(1)
- Space Complexity: O(1)
---
```javascript
const func5 = (arr) => {
  for (let i = 0; i < 5; i++) {
    console.log(i);
  }

  for (let i = 0; i < 100000; i++) {
    console.log(i);
  }
}
```
- Time Complexity: O(1)
- Space Complexity: O(1)
---
```javascript
const func6 = (arr) => {

  const sizeOne = arr.length + 1;
  arr[1] = sizeOne;

  for (let i = 0; i < arr.length; i++) {
    console.log(arr[i]);
  }

  for (let i = 0; i < arr.length; i++) {
    console.log(arr[i]);
  }

  for (let i = 0; i < arr.length; i++) {
    console.log(arr[i]);
  }

}
```
- Time Complexity: O(n)
- Space Complexity: O(1)
---
```javascript
const func7 = (arr) => {
  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < arr.length; j++) {
      console.log(i, j);
    }
  }
}
```
- Time Complexity: O(n^2)
- Space Complexity: O(1)
---
```javascript
const func8 = (arr) => {
  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < arr.length; j++) {
      for (let k = 0; k < arr.length; k++) {
        console.log(i, j, k);
      }
    }
  }
}
```
- Time Complexity: O(n^3)
- Space Complexity: O(1)
---
```javascript
const func9 = (arr) => {
  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < arr.length; j++) {
      console.log(i, j);
    }
  }

  for (let i = 0; i < arr.length; i++) {
    console.log(arr[i]);
  }

  for (let i = 0; i < arr.length; i++) {
    console.log(arr[i]);
  }
}
```
- Time Complexity: O(n^2)
- Space Complexity: O(1)
---
```javascript
const func10 = (arr) => {
  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < arr.length; j++) {
      console.log(i, j);
    }
  }

  for (let i = 0; i < arr.length; i++) {
    console.log(arr[i]);
  }

  for (let i = 0; i < 100; i++) {
    console.log(arr);
  }
}
```
- Time Complexity: O(n^2)
- Space Complexity: O(1)
---
## Part 2

### For every function state the best and worst case

```javascript
const func1 = (n) => {
  if (n === 3) return n;

  for (let i = 0; i < n; i++) {
    console.log(n);
  }
}
```
- Time Complexity: 
  - Best - O(1)
  - Worst - O(n)
- Space Complexity: O(1)
---

```javascript
const func2 = (n) => {
  if (n === 3) return n;

  for (let i = 0; i < n; i++) {
    console.log(n);
  }
}
```
- Time Complexity: 
  - Best - O(1)
  - Worst - O(n)
- Space Complexity: O(1)
---
```javascript
const func3 = (arr) => {
    if (arr.count < 3) {
      return;
    }

    if (arr[0] === 8675309) {
      return;
    }

    if (arr[0] + arr[1] === 24601) {
      arr.forEach(item => {
        arr.forEach(item => {
          console.log(item);
        });
      });
      return;
    }

    arr.forEach(item => {
      console.log(item);
    });
}
```
> In JavaScript: This would break. But assuming that by _.count_ we mean _.length_ then
- Time Complexity: 
  - Best - O(1)
  - Worst - O(n^2)
- Space Complexity: O(1)
---
```javascript
const func4 = (arr, target) => {

  if (arr.length % 2 === 1) {
    binarySearch(arr, target);
  }

  if (arr.length % 2 === 0) {
    linearSearch(arr, target);
  }
}
```
- Time Complexity: 
  - Best - O(log n)
  - Worst - O(n)
- Space Complexity: O(1)
---
```javascript 
const func5 = (arr) => {
    if (arr.length < 2) {
        return arr;
    }

    let mid = Math.floor(arr.length/2);
    let left = arr.slice(0, mid);
    let right = arr.slice(mid);

    return utilityFunc(func5(left),func5(right));
}

const utilityFunc = (left, right) => {
    let l = 0; 
    let r = 0;

    let result = [];

  while(l < left.length &&  r < right.length) {
    if (left[l] < right[r]) {
      result.push(left[l]);
      l++;
    }
    else {
      result.push(right[r]);
      r++;
    }
  }

  return result.concat(left.slice(l)).concat(right.slice(r));
}
```
- Time Complexity: 
  - Best - O(1)
  - Worst - O(n log n)
- Space Complexity: 
  - Best - O(1)
  - Worst - O(log n) | O(n)?
---
