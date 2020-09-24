# Gizem Candemir
## UX/UI Designer & Frontend Developer

Hello world, I want to share my notes from tutorials with you!  
I will be collecting my notes and sharing my final versions for the challenges here. I hope it's useful to someone :)


### JavaScript30

The good old [#JavaScript30](https://javascript30.com/) challenge by Wes Bos.  You can see the list of all challenges [here](https://www.youtube.com/playlist?list=PLu8EoSxDXHP6CGK4YVJhL_VWetA865GOH). 

#### 01 - Drum Kit
My version: [http://js30-01-drum-kit.surge.sh/](http://js30-01-drum-kit.surge.sh/)  
(Click [here](https://github.com/gizemcandemir/JavaScript30/tree/master/01%20-%20JavaScript%20Drum%20Kit/index.html) to see it on GitHub)

#### 02 - CSS Clock
My version: [http://pastel-clock.surge.sh/](http://pastel-clock.surge.sh/)  
(Click [here](https://github.com/gizemcandemir/JavaScript30/tree/master/02%20-%20JS%20and%20CSS%20Clock/index.html) to see it on GitHub)

#### 03 - CSS Variables
My version (same as original): [http://js30-css-variables.surge.sh/](http://js30-css-variables.surge.sh/)  
(Click [here](https://github.com/gizemcandemir/JavaScript30/blob/master/03%20-%20CSS%20Variables/index.html) to see it on GitHub)

#### 04 - Array Cardio Day 1

(Click [here](https://github.com/gizemcandemir/JavaScript30/blob/master/04%20-%20Array%20Cardio%20Day%201/index.html) to see it on GitHub)

Notes:
```javascript
// Sorts the result from oldest to youngest
inventors.sort((a, b) => a.year > b.year)

// Gives the total sum of years inventors lived
const totalYears = inventors.reduce((total, inventor) => {
  return total + (inventor.passed - inventor.year);
}, 0);

// Sums up the instances of each item in the array
const data = ['car', 'car', 'truck', 'truck', 'bike', 'walk', 'car', 'van', 'bike', 'walk', 'car', 'van', 'car', 'truck' ];

const transportation = data.reduce((obj, item) => {
  if(!obj[item]) {
    obj[item] = 0;
  } 
    obj[item]++
    return obj;
}, {})
```

#### 05 - Flex Panel Gallery

(Click [here](https://github.com/gizemcandemir/JavaScript30/blob/master/05%20-%20Flex%20Panel%20Gallery/index.html) to see it on GitHub)

Notes:
```javascript
// Adds or removes the class 'open' from the DOM element where this function is triggered (by using 'this')
function toggleOpen() {
  this.classList.toggle('open');
}
```

#### 06 - Type Ahead

My version (same as original): [http://type-ahead.surge.sh/](http://type-ahead.surge.sh/)  
(Click [here](https://github.com/gizemcandemir/JavaScript30/blob/master/06%20-%20Type%20Ahead/index.html) to see it on GitHub)

Notes:
```javascript
//Using Regular Expressions
function findMatches(wordToMatch, cities) {
  return cities.filter(place => {
    const regex = new RegExp(wordToMatch, 'gi'); //gi means global, insensitive
    return place.city.match(regex) || place.state.match(regex)
  });
};
```

#### 07 - Array Cardio Day 2

(Click [here](https://github.com/gizemcandemir/JavaScript30/blob/master/07%20-%20Array%20Cardio%20Day%202/index-START.html) to see it on GitHub)

Notes:
```javascript
array.some(); //checks if at least one...
array.every(); //checks if every element...
array.find(); //returns what you are looking for
array.findIndex(); //returns index id

//common way to create new array after deleting one element with index
const newComments = [
  ...comments.slice(0, index),
  ...comments.slice(index + 1)
]
```

#### 08 - Fun with HTML5 Canvas

My version (same as original): [http://hue-paint.surge.sh/](http://hue-paint.surge.sh/)  
(Click [here](https://github.com/gizemcandemir/JavaScript30/blob/master/08%20-%20Fun%20with%20HTML5%20Canvas/index.html) to see it on GitHub)

#### 09 - 14 Must Know Dev Tools Tricks


```javascript
// Regular
console.log('hello');

// Interpolated
console.log('A string with %s is included', 'What we write here will be replacing "percent-symbol-s" in previous argument');

// Styled
console.log('using %c will let you style on next argument', 'background:red')

// Warning
console.warn('shows this in the warning style');

// Error
console.error('shows this in the error style');

// Info
console.info('shows this in the info style');

// Testing
const p = document.querySelector('p');
console.assert(p.classList.contains('ouch'), 'That is wrong!'); //will only console if that is wrong

// Clearing
console.clear();

// Viewing DOM Elements with all the available methods and calls
console.dir(p);

// Grouping together
dogs.forEach(dog => {
  console.groupCollapsed(`${dog.name}`);
  console.log(`This is ${dog.name}`);
  console.log(`${dog.name} is ${dog.age} years old`);
  console.log(`${dog.name} is ${dog.age * 7} dog years old`);
  console.groupEnd(`${dog.name}`);
});

// Counting
console.count(var);

// Timing
console.time('fetching data');
fetch('https://api.github.com/users/wesbos')
  .then(data => data.json())
  .then(data => {
    console.timeEnd('fetching data');
  });

// Shows result in table
console.table(dogs);
```

#### 10 - Hold Shift to Check Multiple Checkboxes

(Click [here](https://github.com/gizemcandemir/JavaScript30/blob/master/10%20-%20Hold%20Shift%20and%20Check%20Checkboxes/index.html) to see it on GitHub)

Notes:
```javascript
 document.querySelectorAll() // returns an array with specified elements
 
 // will play or pause the video depending on the video is already paused or not
 function togglePlay() {
  const method = video.paused ? 'play' : 'pause';
  video[method]();
}

// 
function handleRangeUpdate() {
  video[this.name] = this.value;
}
```

#### 12 - Key Sequence Detection

My version: [http://js30-konami-code.surge.sh/](http://js30-konami-code.surge.sh/)  
(Click [here](https://github.com/gizemcandemir/JavaScript30/blob/master/12%20-%20Key%20Sequence%20Detection/index.html) to see it on GitHub)

Notes:
```javascript
// The splice() method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.
// this one modifies the array to keep only secretCode length amount of elements from the end
pressed.splice(-secretCode.length - 1, pressed.length - secretCode.length); 

// The join() method creates and returns a new string by concatenating all of the elements in an array (or an array-like object), separated by commas or a specified separator string. If the array has only one item, then that item will be returned without using the separator.
if(pressed.join('').includes(secretCode)) {
  ...
}
```

#### 13 - Slide In on Scroll

My version: [http://js30-slide-in.surge.sh/](http://js30-slide-in.surge.sh/)  
(Click [here](https://github.com/gizemcandemir/JavaScript30/blob/master/13%20-%20Slide%20in%20on%20Scroll/index.html) to see it on GitHub)

Notes:
```javascript
// debounce means we will only run the specified function at most at the specified time
function debounce(func, wait = 20, immediate = true) {
  ...
}
```

#### 14 - Object and Arrays

Notes:
```markdown
// if you assign a value to a **reference** it is actually updating the original. 

let players = [a, b, c];
let team = players;
let team[2] = d
console.log(players); 
// output will be [a, b, d]

// if you **slice** the array and assign it to a variable. That new variable will be the copy of the original array. So when you update the **copy**, it won't update the original array.

const team2 = players.slice();

// or you can **concatenate** the original array to a new empty one.

const team3 = [].concat(players);

// or you can **spread** the old array into a new array with ES6.

const team4 = [...players];

// or you can create a new array with **Array.from()**

const team5 = Array.from(players);

// however if you reference a variable with an Object, and if you edit the reference you also update the original object. 
instead of referencing you need to create a copy for objects with **Object.assign** or as of 2018 you can also spread objects.

const cap2 = Object.assign({}, person, { number: 99 });
const cap2 = { ...person }

// when you use **Object.assign** it only copies the object one level deep. if you update the new object's deeper level variables the original will be updated too. to avoid it you can find the **cloneDeep** function online. Or you can use 'poorman's deepClone' by turning object to string with **JSON.stringify** and that string back to object with **JSON.parse()**  OR nowadays you can just use spread operator **{ ... object }** instead.
```

#### 15 - Local Storage and Event Delegation

My version: [http://js30-15-local-tapas.surge.sh/](http://js30-15-local-tapas.surge.sh/)  
(Click [here](https://github.com/gizemcandemir/JavaScript30/blob/master/15%20-%20LocalStorage/index.html) to see it on GitHub)

Notes:
```javascript
// you can add items to LocalStorage so your list will stay same when page is reloaded
localStorage.setItem('items', JSON.stringify(items));
```
