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
