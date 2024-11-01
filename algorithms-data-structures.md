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
