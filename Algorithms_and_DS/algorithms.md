# Algorithms and data structures

Find Nemo

```javascript
const nemo = ['Nemo'];

function findNemo(array) {
   for (let i = 0; i < array.length; i++) {
      if (array[i] === 'Nemo') {
         console.log('We found Nemo!');
      }
   }
}

findNemo(nemo);
```

###How to check performance

```javascript
const nemo = ['Nemo'];

function findNemo(array) {
   // first timer for a performance
   let t0 = performance.now();
   for (let i = 0; i < array.length; i++) {
      if (array[i] === 'Nemo') {
         console.log('We found Nemo!');
      }
   }
   // second timer for a performance
   let t1 = performance.now();
   // result
   console.log('Call to find Nemo took ' + (t1 - t0) + ' milliseconds');
}

findNemo(nemo);
```

Array becomes bigger!

```javascript
const large = new Array(10000).fill('nemo');

function findNemo(array) {
   let t0 = performance.now();
   for (let i = 0; i < array.length; i++) {
      if (array[i] === 'nemo') {
         console.log('We found Nemo!');
      }
   }
   let t1 = performance.now();
   console.log('Call to find Nemo took ' + (t1 - t0) + ' milliseconds');
}

findNemo(large);
```

### O(n)

This is an example of Big O notatin O(n) --> Linear Time.
It takes linear time to find the Nemo. Proportionally
Big O depends on inputs (n) number of fish.

```javascript
const everyone = [
   'dory',
   'bruce',
   'marlin',
   'nemo',
   'gill',
   'bloat',
   'nigel',
   'squirt',
   'darla',
   'hank',
];

// Other ways doing loops

//ES5 fn

function boxCompressing(array) {
   array.forEach(function (el) {
      console.log(el);
   });
}

//ES6 arrow fn
const boxCompressing = (array) => array.forEach((el) => console.log(el));

boxCompressing(everyone);
```

---

### O(n)

O(1) - constant amount of time.
It's in green area like O(n), it's really scalable.

-  Linear time
-  Constant time

#### Exercise

**What is the Big O of the below function? (Hint, you may want to go line by line)**

```javascript
const myInput = [10, 20, 30, 40];

function funChallenge(input) {
   let a = 10; // О(1)
   a = 50 + 3; // О(1)

   for (let i = 0; i < input.length; i++) {
      // О(n)
      anotherFunction(); // О(n)
      let stranger = true; //O(n)
      a++; //O(n)
   }
   return a; //О(1)
}

//BIG O(3 + 4n)
```

#### Exercise

```javascript
// What is the Big O of the below function? (Hint, you may want to go line by line)
function anotherFunChallenge(input) {
   let a = 5; // O(1)
   let b = 10; // O(1)
   let c = 50; // O(1)
   for (let i = 0; i < input; i++) {
      // O(n)
      let x = i + 1; // O(n)
      let y = i + 2; // O(n)
      let z = i + 3; // O(n)
   }
   for (let j = 0; j < input; j++) {
      // O(n)
      let p = j * 2; // O(n)
      let q = j * 2; // O(n)
   }
   let whoAmI = "I don't know"; // O(1)
}
// Big O = 4 + 7n = O(n)
```

### Rule Book

-  Rule 1: Worst Case
   When we calculate Big O we always calculate worst Case
   Best case when our 'Nemo' will be in the start of array, the worst case: when 'Nemo' will be in the end of array
-  Rule 2: Remove constants
-  Rule 3: Different terms for inputs
-  Rule 4: Drop non dominants

To rule 3

```javascript
function compressBoxesTwice(boxes, boxes 2) {
   boxes.forEach(function(box){
      console.log(box);
   })

   boxes2.forEach(function(box) {
      console.log(box);
   })
}
```

Here **up** we have 2 different arrays, and **down** we have two loops under one array

O(a + b) // when arrays follow one after another we must + (up)

O(a _ b) // when arrays nested one in another we use _ (down)

#### Exercise

```javascript
// Log all pairs of array
const nums = [1, 2, 3, 4, 5];

function logPairs(array) {
   for (let i = 0; i < array.length; i++) {
      for (let k = 0; k < array.length; k++) {
         console.log(array[i], array[k]);
      }
   }
}

logPairs(nums);
```

Example of O(n ^ 2);

The same decision in ES5

```javascript
function logPairs(array) {
   array.forEach(function (firstBox) {
      array.forEach(function (secondBox) {
         console.log(firstBox, secondBox);
      });
   });
}

logPairs(nums);
```

O(n2) - quadratic time (2 is under n)

### O(n!)

Factorial - you are adding a loop for every element
