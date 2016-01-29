## You don't (may not) need Lodash/Underscore 

Lodash and Underscore are great modern JavaScript utility libraries, and they are widely used by Front-end developers. However, when you are targeting modern browsers, you may find out that there are many methods which are already supported natively thanks to ECMAScript5 [ES5] and ESCMAScript2015 [ES6]. If you want your project to require fewer dependencies, and you know your target browser clearly, then you may not need Lodash/Underscore.

You are welcome to contribute with more items provided below.

## Quick links

1. [_.each](#_each)
1. [_.map](#_map)
1. [_.every](#_every)
1. [_.some](#_every)
1. [_.reduce](#_reduce)
1. [_.reduceRight](#_reduceright)
1. [_.filter](#_filter)
1. [_.find](#_find)
1. [_.findIndex](#_find)
1. [_.indexOf](#_indexof)
1. [_.lastIndexOf](#_lastindexof)
1. [_.includes/_.contains](#_.includes/_.contains)
1. [_.keys](#_keys)
1. [_.size](#_size)
1. [_.isNaN](#_isnan)
1. [_.reverse](#_reverse)
1. [_.join](#_join)
1. [_.toUpper](#_toupper)
1. [_.toLower](#_tolower)
1. [_.trim](#_trim)

## _.each

Iterates over a list of elements, yielding each in turn to an iteratee function.

  ```js
  // Underscore/Lodash
  _.each([1, 2, 3], function(value, index) {
    console.log(value);
  });
  // output: 1 2 3

  // Native
  [1, 2, 3].forEach(function(value, index) {
    console.log(value);
  });
  // output: 1 2 3
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 1.5 ✔ |  9 ✔  |  ✔  |  ✔  |   

**[⬆ back to top](#quick-links)**

## _.map

Translate all items in an array or object to new array of items.

  ```js
  // Underscore/Lodash
  var array1 = [1, 2, 3];
  var array2 = _.map(array1, function(value, index) {
    return value*2;
  });
  console.log(array2);
  // output: [2, 4, 6]

  // Native
  var array1 = [1, 2, 3];
  var array2 = array1.map(function(value, index) {
    return value*2;
  });
  console.log(array2);
  // output: [2, 4, 6]
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 1.5 ✔ |  9 ✔  |  ✔  |  ✔  |  

**[⬆ back to top](#quick-links)**

## _.every

Tests whether all elements in the array pass the test implemented by the provided function.

  ```js
  // Underscore/Lodash
  function isLargerThanTen(element, index, array) {
    return element >=10;
  }
  var array = [10, 20, 30];
  var result = _.every(array, isLargerThanTen);
  console.log(result);
  // output: true

  // Native
  function isLargerThanTen(element, index, array) {
    return element >=10;
  }

  var array = [10, 20, 30];
  var result = array.every(isLargerThanTen);
  console.log(result);
  // output: true
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 1.5 ✔ |  9 ✔  |  ✔  |  ✔  |  

**[⬆ back to top](#quick-links)**

## _.some

Tests whether some element in the array passes the test implemented by the provided function.
 
  ```js
  // Underscore/Lodash
  function isLargerThanTen(element, index, array) {
    return element >=10;
  }
  var array = [10, 9, 8];
  var result = _.some(array, isLargerThanTen);
  console.log(result);
  // output: true

  // Native
  function isLargerThanTen(element, index, array) {
    return element >=10;
  }

  var array = [10, 9, 8];
  var result = array.some(isLargerThanTen);
  console.log(result);
  // output: true
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 1.5 ✔ |  9 ✔  |  ✔  |  ✔  |  

**[⬆ back to top](#quick-links)**

## _.reduce

Applies a function against an accumulator and each value of the array (from left-to-right) to reduce it to a single value.

  ```js
  // Underscore/Lodash
  var array = [0, 1, 2, 3, 4];
  var result = _.reduce(array, function (previousValue, currentValue, currentIndex, array) {
    return previousValue + currentValue;
  });
  console.log(result);
  // output: 10

  // Native
  var array = [0, 1, 2, 3, 4];
  var result = array.reduce(function (previousValue, currentValue, currentIndex, array) {
    return previousValue + currentValue;
  });
  console.log(result);
  // output: 10
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 3.0 ✔ |  9 ✔  |  10.5  |  4.0  |  

**[⬆ back to top](#quick-links)**

## _.reduceRight

This method is like _.reduce except that it iterates over elements of collection from right to left.

  ```js
  // Underscore/Lodash
  var array = [0, 1, 2, 3, 4];
  var result = _.reduceRight(array, function (previousValue, currentValue, currentIndex, array) {
    return previousValue - currentValue;
  });
  console.log(result);
  // output: -2

  // Native
  var array = [0, 1, 2, 3, 4];
  var result = array.reduceRight(function (previousValue, currentValue, currentIndex, array) {
    return previousValue - currentValue;
  });
  console.log(result);
  // output: -2
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 3.0 ✔ |  9 ✔  |  10.5  |  4.0  |  

**[⬆ back to top](#quick-links)**

## _.filter

Creates a new array with all elements that pass the test implemented by the provided function.

  ```js
  // Underscore/Lodash
  function isBigEnough(value) {
    return value >= 10;
  } 
  var array = [12, 5, 8, 130, 44];
  var filtered = _.filter(array, isBigEnough);
  console.log(filtered);
  // output: [12, 130, 44]

  // Native
  function isBigEnough(value) {
    return value >= 10;
  } 
  var array = [12, 5, 8, 130, 44];
  var filtered = array.filter(isBigEnough);
  console.log(filtered);
  // output: [12, 130, 44]
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 1.5 ✔ |  9 ✔  |  ✔  |  ✔  |  

**[⬆ back to top](#quick-links)**

## _.find

Returns a value in the array, if an element in the array satisfies the provided testing function. Otherwise undefined is returned.

  ```js
  // Underscore/Lodash
  var users = [
    { 'user': 'barney',  'age': 36, 'active': true },
    { 'user': 'fred',    'age': 40, 'active': false },
    { 'user': 'pebbles', 'age': 1,  'active': true }
  ];

  _.find(users, function(o) { return o.age < 40; });
  // output: object for 'barney'

  // Native
  var users = [
    { 'user': 'barney',  'age': 36, 'active': true },
    { 'user': 'fred',    'age': 40, 'active': false },
    { 'user': 'pebbles', 'age': 1,  'active': true }
  ];

  users.find(function(o) { return o.age < 40; });
  // output: object for 'barney'
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  45.0  | 25.0 ✔ |  Not supported  |  Not supported |  7.1  |  

**[⬆ back to top](#quick-links)**

## _.findIndex

Returns an index in the array, if an element in the array satisfies the provided testing function. Otherwise -1 is returned.

  ```js
  // Underscore/Lodash
  var users = [
    { 'user': 'barney',  'age': 36, 'active': true },
    { 'user': 'fred',    'age': 40, 'active': false },
    { 'user': 'pebbles', 'age': 1,  'active': true }
  ];

  var index =  _.findIndex(users, function(o) { return o.age >= 40; });
  console.log(index);
  // output: 1

  // Native
  var users = [
    { 'user': 'barney',  'age': 36, 'active': true },
    { 'user': 'fred',    'age': 40, 'active': false },
    { 'user': 'pebbles', 'age': 1,  'active': true }
  ];

  var index =  users.findIndex(function(o) { return o.age >= 40; });
  console.log(index);
  // output: 1
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  45.0  | 25.0 ✔ |  Not supported  |  Not supported |  7.1  |  

**[⬆ back to top](#quick-links)**

## _.indexOf

Returns the first index at which a given element can be found in the array, or -1 if it is not present.

  ```js
  // Underscore/Lodash
  var array = [2, 9, 9];
  var result = _.indexOf(array, 2);    
  console.log(result); 
  // output: 0

  // Native
  var array = [2, 9, 9];
  var result = array.indexOf(2);    
  console.log(result); 
  // output: 0
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  | 1.5 ✔ |  9 ✔  |  ✔  |  ✔  |  

**[⬆ back to top](#quick-links)**

## _.lastIndexOf

Returns the index of the last occurrence of value in the array, or -1 if value is not present.

  ```js
  // Underscore/Lodash
  var array = [2, 9, 9, 4, 3, 6];
  var result = _.lastIndexOf(array, 9);    
  console.log(result); 
  // output: 2

  // Native
  var array = [2, 9, 9, 4, 3, 6];
  var result = array.lastIndexOf(2);    
  console.log(result); 
  // output: 0
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  |  ✔ |  9 ✔  |  ✔  |  ✔  |  

**[⬆ back to top](#quick-links)**

## _.includes/_.contains

Checks if value is in collection. 

  ```js
  var array = [1, 2, 3];
  // Underscore/Lodash - also called with _.contains
  _.includes(array, 1);
  // → true

  // Native
  var array = [1, 2, 3];
  array.includes(1);
  // → true
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  47✔  | 43 ✔ |  Not supported  |  34 |  9  |  

**[⬆ back to top](#quick-links)**

## _.keys

Retrieve all the names of the object's own enumerable properties.

  ```js
  // Underscore/Lodash 
  var result = _.keys({one: 1, two: 2, three: 3});
  console.log(result);
  // output: ["one", "two", "three"]

  // Native
  var result2 = Object.keys({one: 1, two: 2, three: 3});
  console.log(result2); 
  // output: ["one", "two", "three"]
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  5✔  | 4.0 ✔ |  9  |  12 |  5  |  

**[⬆ back to top](#quick-links)**

## _.size

Return the number of values in the collection.

  ```js
  // Underscore/Lodash
  var result = _.size({one: 1, two: 2, three: 3});
  console.log(result);
  // output: 3

  // Native
  var result2 = Object.keys({one: 1, two: 2, three: 3}).length;
  console.log(result2); 
  // output: 3
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  5✔  | 4.0 ✔ |  9  |  12 |  5  |  

**[⬆ back to top](#quick-links)**

## _.isNaN

Checks if value is NaN. 

  ```js
  // Underscore/Lodash
  console.log(_.isNaN(NaN));
  // output: true

  // Native
  console.log(isNaN(NaN));
  // output: true
  ```

Voice from the Lodash author:

>Lodash's `_.isNaN` is equiv to ES6 `Number.isNaN` which is different than the global `isNaN`.  
>--- [jdalton](https://github.com/cht8687/You-Dont-Need-Lodash-Underscore/commit/b8559a603dccaaa2449b5a68a2d8325cf1fb29cd#)

### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  |  ✔ |  ✔ |  ✔ |  ✔  |  

**[⬆ back to top](#quick-links)**

## _.reverse
:heavy_exclamation_mark:`Lodash only`
Reverses array so that the first element becomes the last, the second element becomes the second to last, and so on. 

  ```js
  // Lodash
  var array = [1, 2, 3];
  console.log(_.reverse(array));
  // output: [3, 2, 1]

  // Native
  var array = [1, 2, 3];
  console.log(array.reverse());
  // output: [3, 2, 1]
  ```

Voice from the Lodash author:

>Lodash's `_.reverse` just calls `Array#reverse` and enables composition like `_.map(arrays, _.reverse).`
It's exposed on _ because previously, like `Underscore`, it was only exposed in the chaining syntax.
>--- [jdalton](https://github.com/cht8687/You-Dont-Need-Lodash-Underscore/commit/22c4bcf2be48dd415d2b073759805562e520b615#)  

### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  1.0✔  |  1.0✔ |  5.5✔ |  ✔ |  ✔  |  

**[⬆ back to top](#quick-links)**

## _.join
:heavy_exclamation_mark:`Lodash only`
Joins a list of elements in an array with a given separator.

  ```js
  // Lodash
  var result = _.join(['one', 'two', 'three'], '--');
  console.log(result);
  // output: 'one--two--three'

  // Native
  var result = ['one', 'two', 'three'].join('--');
  console.log(result)
  // output: 'one--two--three'
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  1.0✔  |  1.0✔ |  5.5✔  |  ✔ |  ✔  |  

**[⬆ back to top](#quick-links)**

## _.toUpper
:heavy_exclamation_mark:`Lodash only`
Uppercase a given string.

  ```js
  // Lodash
  var result = _.toUpper('foobar');
  console.log(result);
  // output: 'FOOBAR'

  // Native
  var result = 'foobar'.toUpperCase();
  console.log(result);
  // output: 'FOOBAR'
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  |  ✔ |  ✔  |  ✔ |  ✔  |  

**[⬆ back to top](#quick-links)**

## _.toLower
:heavy_exclamation_mark:`Lodash only`
Lowercase a given string.

  ```js
  // Lodash
  var result = _.toLower('FOOBAR');
  console.log(result);
  // output: 'foobar'

  // Native
  var result = 'FOOBAR'.toLowerCase();
  console.log(result);
  // output: 'foobar'
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  ✔  |  ✔ |  ✔  |  ✔ |  ✔  |  

**[⬆ back to top](#quick-links)**

## _.trim
:heavy_exclamation_mark:`Lodash only`
Removes leading and trailing whitespace characters from string.

  ```js
  // Lodash
  var result = _.trim(' abc ');
  console.log(result);
  // output: 'abc'

  // Native
  var result = ' abc '.trim();
  console.log(result);
  // output: 'abc'
  ```
### Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
  5.0✔  |  3.5✔ |  9.0✔  |  10.5✔ |  5.0✔  |  

**[⬆ back to top](#quick-links)**

## Reference

* [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference) 

* [Underscore.js](http://underscorejs.org) 

* [Lodash.js](https://lodash.com/docs) 

## Inspired by: 

* [You-Dont-Need-jQuery](https://github.com/oneuijs/You-Dont-Need-jQuery)
* [Rui's blog](http://ktei.github.io/2016/01/07/some-general-js-tips-1.html)

# License

MIT
