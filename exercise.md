**Step One: Simplifying Expressions**
Simplify the following big O expressions as much as possible:

O(n + 10) --> O(n)

O(100 * n) --> O(n)

O(25) --> O(1)

O(n^2 + n^3) --> O(n^3)

O(n + n + n + n) --> O(1)

O(1000 * log(n) + n) --> O()

O(1000 * n * log(n) + n) -->  O(nlog(n))

O(2^n + n^2) -> O(2^n)

O(5 + 3 + 1) --> O(1)

O(n + n^(1/2) + n^2 + n * log(n)^10) --> O(n^2)




**Step Two:** Calculating Time Complexity
Determine the time complexities for each of the following functions. If you’re not sure what these functions do, copy and paste them into the console and experiment with different inputs!

```js
function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}
```
**Runtime**: O(n)

```js
function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}
```

**Runtime**: O(n)

```js
function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}
```
**Runtime**: O(1)

```js
function onlyElementsAtEvenIndex(array) {
  let newArray = [];
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray.push(array[i]);
    }
  }
  return newArray;
}
```
**Runtime**: O(n)


```js
function subtotals(array) {
  let subtotalArray = [];
  for (let i = 0; i < array.length; i++) {
    let subtotal = 0;
    for (let j = 0; j <= i; j++) {
      subtotal += array[j];
    }
    subtotalArray.push(subtotal);
  }
  return subtotalArray;
}
```
**Runtime**: O(n^2)

```js
function vowelCount(str) {
  let vowelCount = {};
  const vowels = "aeiouAEIOU";

  for (let char of str) {
    if(vowels.includes(char)) {
      if(char in vowelCount) {
        vowelCount[char] += 1;
      } else {
        vowelCount[char] = 1;
      }
    }
  }

  return vowelCount;
}
```
**Runtime**: O(n)

**Part 3 - short answer**

Answer the following questions

True or false: n^2 + n is O(n^2). [TRUE]

True or false: n^2 * n is O(n^3).   [FALSE]

True or false: n^2 + n is O(n).     [FALSE]

What’s the time complexity of the .indexOf array method? O(n)

What’s the time complexity of the .includes array method? O(n)

What’s the time complexity of the .forEach array method? O(n)

What’s the time complexity of the .sort array method? O(nlog(n))

What’s the time complexity of the .unshift array method? O(n)

What’s the time complexity of the .push array method? O(1)

What’s the time complexity of the .splice array method? O(n)

What’s the time complexity of the .pop array method? O(1)

What’s the time complexity of the Object.keys() function? O(n)