# Table of Content

 Language      | Difficulty    | Problem Name  |
| ------------- |:-------------:| -----:|
| JavaScript    | 8 kyu         | [Even or Odd](#problem1)|
| JavaScript    | 8 kyu         | [Add Length](#problem2)|
| JavaScript    | 8 kyu         | [Vowel remover](#problem3)||
| JavaScript    | 8 kyu         | [Quarter of the year](#problem4)||
| JavaScript    | 8 kyu         | [The 'if' function](#problem5)||
| JavaScript    | 8 kyu         | [Price of Mangoes](#problem6)||
| JavaScript    | 8 kyu         | [Powers of 2](#problem7)||
| JavaScript    | 8 kyu         | [Collatz Conjecture (3n+1)](#problem8)||
| JavaScript    | 8 kyu         | [Cat years, Dog years](#problem9)||
| JavaScript    | 8 kyu         | [Count the number of cubes with paint](#problem10)||
| JavaScript    | 8 kyu         | [Get the main of an array](#problem11)||
| JavaScript    | 8 kyu         | [Abbreviate a Two Word Name](#problem12)||
| JavaScript    | 8 kyu         | [Is there a vowel in there?](#problem13)||
| JavaScript    | 8 kyu         | [Gravity Flip](#problem14)||
| JavaScript    | 8 kyu         | [Find nearest square number](#problem15)||
| JavaScript    | 8 kyu         | [Count of positives / sum of negatives](#problem16)||
| JavaScript    | 8 kyu         | [Contamination #1-String](#problem17)||

---

### Problem #1 Even or Odd<a name="problem1"></a>

Create a function that takes an integer as an argument and returns "Even" for even numbers or "Odd" for odd numbers.

```javascript
function evenOrOdd(number) {
  return (number % 2 === 0 ? 'Even' : 'Odd')
}
console.log(evenOrOdd(2)) // Output: Even
console.log(evenOrOdd(3)) // Output: Odd
```
---

### Problem #2 Add Length<a name="problem2"></a>

What if we need the length of the words separated by a space to be added at the end of that same word and have it returned as an array?

Example(Input --> Output)

```javascript
"apple ban" --> ["apple 5", "ban 3"]
"you will win" -->["you 3", "will 4", "win 3"]
```
Your task is to write a function that takes a String and returns an Array/list with the length of each word added to each element .

```javascript
function addLength(str) {
  return str.split(' ').map(word => `${word} ${word.length}`)
}
console.log(addLength('apple ban')) // Output: ["apple 5", "ban 3"]
console.log(addLength('you will win')) // Output: ["you 3", "will 4", "win 3"]
```
---

### Problem #3 Vowel Remover<a name="problem3"></a>

Create a function called shortcut to remove the lowercase vowels (a, e, i, o, u ) in a given string.

Examples

```javascript
"hello"     -->  "hll"
"codewars"  -->  "cdwrs"
"goodbye"   -->  "gdby"
"HELLO"     -->  "HELLO"

```javascript
function shortcut (string) {
   const noVowels = string.replace(/[aeiou]/gi, '')
   return noVowels
}
```
---

### Problem #4 Quarter of the year<a name="problem4"></a>

Given a month as an integer from 1 to 12, return to which quarter of the year it belongs as an integer number.

For example: month 2 (February), is part of the first quarter; month 6 (June), is part of the second quarter; and month 11 (November), is part of the fourth quarter.

```javascript
function quarterOf(month) {
            if (month === 1) {
                return 1
            } else if (month === 2) {
                return 1
            } else if (month === 3) {
                return 1
            } else if (month === 4) {
                return 2
            } else if (month === 5) {
                return 2
            } else if (month === 6) {
                return 2
            } else if (month === 7) {
                return 3
            } else if (month === 8) {
                return 3
            } else if (month === 9) {
                return 3
            } else if (month === 10) {
                return 4
            } else if (month === 11) {
                return 4
            } else if (month === 12) {
                return 4
            } else {
                console.log('Month not found');
            }
        }
        console.log(quarterOf(3)); // Output 1
        console.log(quarterOf(8)); // Output 3
        console.log(quarterOf(11)); // Output 4
```
---

### Problem #5 The 'if' function<a name="problem5"></a>

Create a function called *___if__* which takes 3 arguments: a value *__bool__* and 2 functions (which do not take any parameters): *__func1__* and *__func2__*

When *__bool__* is truthy, *__func1__* should be called, otherwise call the *__func2__*.

```javascript
function _if(bool, func1, func2) {
  if (bool) {
    return func1()
  } else {
    func2()
```

---

### Problem #6 Price of Mangoes<a name="problem6"></a>

There's a *__"3 for 2"__* (or *__"2+1"__* if you like) offer on mangoes. For a given quantity and price (per mango), calculate the total cost of the mangoes.

Examples:

```javascript
mango(2, 3) ==> 6    # 2 mangoes for $3 per unit = $6; no mango for free
mango(3, 3) ==> 6    # 2 mangoes for $3 per unit = $6; +1 mango for free
mango(5, 3) ==> 12   # 4 mangoes for $3 per unit = $12; +1 mango for free
mango(9, 5) ==> 30   # 6 mangoes for $5 per unit = $30; +3 mangoes for free
```

```javascript
function mango(quantity, price) {
  let normalQuantity = quantity - Math.floor(quantity / 3)
  return normalQuantity * price
}
console.log(mango(3, 3)); // 6 (1 mango for free)
console.log(mango(9, 5)); // 30 (3 mangos for free)
```

---

### Problem #7 Powers of 2<a name="problem7"></a>

Complete the function that takes a non-negative integer n as input, and returns a list of all the powers of 2 with the exponent ranging from 0 to n ( inclusive ).

Examples

```javascript
n = 0  ==> [1]        # [2^0]
n = 1  ==> [1, 2]     # [2^0, 2^1]
n = 2  ==> [1, 2, 4]  # [2^0, 2^1, 2^2]
```

```javascript
function powersOfTwo(n) {
 let arr = []
 for (let i = 0; i <= n; i++) {
 arr[i] = 2 ** i
}
 return arr
}
 console.log(powersOfTwo(0)); // Output [1]
 console.log(powersOfTwo(1)); // Output [1,2]
 console.log(powersOfTwo(4)); // Output [1, 2,4,8,16]
```

---

### Problem #8 Collatz Conjecture (3n+1)<a name="problem8"></a>

The Collatz conjecture (also known as 3n+1 conjecture) is a conjecture that applying the following algorithm to any number we will always eventually reach one:

#Task

Your task is to make a function hotpo that takes a positive n as input and returns the number of times you need to perform this algorithm to get n = 1.

#Examples

```javascript
hotpo(1) returns 0
(1 is already 1)
hotpo(5) returns 5
5 -> 16 -> 8 -> 4 -> 2 -> 1
hotpo(6) returns 8
6 -> 3 -> 10 -> 5 -> 16 -> 8 -> 4 -> 2 -> 1
hotpo(23) returns 15
23 -> 70 -> 35 -> 106 -> 53 -> 160 -> 80 -> 40 -> 20 -> 10 -> 5 -> 16 -> 8 -> 4 -> 2 -> 1
```

```javascript
function hotpo(n) {
 if (n <= 0) {
 throw new Error('Only positive numbers are allowed')
}
 let counter = 0;
 while (n > 1) {
  if (n % 2 === 0) {
   n = n / 2
  } else {
   n = (3 * n) + 1
  }
   counter += 1
  }
   return counter
 
console.log(hotpo(1)); // Output 0
console.log(hotpo(5)); // Output 5
console.log(hotpo(6)); // Output 8
```
---

### Problem #9 Cat years, Dog years<a name="problem9"></a>

Return their respective ages now as *__[humanYears,catYears,dogYears]__*

NOTES:
- humanYears >= 1
- humanYears are whole numbers only

__Cat Years__
- 15 cat years for first year
- +9 cat years for second year
- +4 cat years for each year after that

__Dog Years__
- 15 dog years for first year
- +9 dog years for second year
- +5 dog years for each year after that

```javascript
function humanYearsCatYearsDogYears(humanYears) {
  if (humanYears === 1) return [1, 15, 15]
  else if (humanYears === 2) return [2, 24, 24]
  else return [humanYears, 24 + (humanYears - 2) * 4, 24 + (humanYears - 2) * 5]
}
console.log(humanYearsCatYearsDogYears(1)) // Output [1,15,15]
console.log(humanYearsCatYearsDogYears(2)) // Output [2, 24,24]
console.log(humanYearsCatYearsDogYears(10)) // Output [10,56,64]
```
---

### Problem #10 Count the number of cubes with paint<a name="problem10"></a>

Upon arriving at an interview, you are presented with a solid blue cube. The cube is then dipped in red paint, coating the entire surface of the cube. The interviewer then proceeds to cut through the cube in all three dimensions a certain number of times.

Your function takes as parameter the number of times the cube has been cut. You must return the number of smaller cubes created by the cuts that have at least one red face.

```javascript
Examples:
countSquares(2) --> 26
countSquares(4) --> 98

```javascript
function countSquares(cuts) {
  if (cuts === 0) {
    return 1
  } else if (cuts === 1) {
      return 8
  } else {
      return (cuts + 1) ** 3 - (cuts - 1) ** 3
  }
 }
console.log(countSquares(2)) // Output 26
console.log(countSquares(4)) // Output 98
console.log(countSquares(5)) // Output 152
```

---

## Problem #11 Get the mean of an array<a name="problem11"></a>

It's the academic year's end, fateful moment of your school report. The averages must be calculated. All the students come to you and entreat you to calculate their average for them. Easy ! You just need to write a script.

Return the average of the given array rounded down to its nearest integer.

The array will never be empty.

```javascript
function getAverage(marks){
  const sum = marks.reduce((a, b) => a + b, 0)
  const avg = Math.floor((sum / marks.length))
  return avg
}
console.log(getAverage([2, 2, 2, 2])) // Output: 2
console.log(getAverage([1, 1, 1, 1, 1, 1, 1, 2])) // Output 1
```
---

### Problem #12 Abbreviate a Two Word Name<a name="problem12"></a>

Write a function to convert a name into initials. This kata strictly takes two words with one space in between them.

The output should be two capital letters with a dot separating them.

It should look like this:

```javascript
Sam Harris => S.H
patrick feeney => P.F
```

```javascript
function abbrevName(name){
  let fName = name.split(' ')[0].slice(0, 1).toUpperCase()
  let lName = name.split(' ')[1].slice(0, 1).toUpperCase()
  return `${fName}.${lName}`
  
  console.log(abbrevName('Sam Gariws')) // Output S.G
  console.log(abbrevName('evan Poe'))   // Output E.P
}

---

### Problem #13 Is there a vowel in there?<a name="problem13"></a>

Given an array of numbers, check if any of the numbers are the character codes for lower case vowels (a, e, i, o, u).

If they are, change the array value to a string of that vowel.

Return the resulting array.

Example 1

```javascript
function isVow(a) {
  let map = {
    97: 'a',
    101: 'e',
    105: 'i',
    111: 'o',
    117: 'u'
   }
   return a.map(num => map[num] ? map[num] : num)
}
  console.log(isVow([118, 117, 120, 121, 117, 98, 122, 97, 120, 106, 104, 116, 113, 114, 113, 120, 106]))
```

Example 2

```javascript
function isVow(a) {
  return a.map(x => /[aeiou]/.test(String.fromCharCode(x)) ? String.fromCharCode(x) : x)
}
console.log(isVow([118, 117, 120, 121, 117, 98, 122, 97, 120, 106, 104, 116, 113, 114, 113, 120, 106]))
```

---

### Problem #14 Gravity Flip<a name="problem14"></a>

Bob is bored during his physics lessons so he's built himself a toy box to help pass the time. The box is special because it has the ability to change gravity.

There are some columns of toy cubes in the box arranged in a line. The i-th column contains a_i cubes. At first, the gravity in the box is pulling the cubes downwards. When Bob switches the gravity, it begins to pull all the cubes to a certain side of the box, d, which can be either 'L' or 'R' (left or right). Below is an example of what a box of cubes might look like before and after switching gravity.

Examples (input -> output)

```javascript
'R', [3, 2, 1, 2]      ->  [1, 2, 2, 3]
'L', [1, 4, 5, 3, 5 ]  ->  [5, 5, 4, 3, 1]
```

```javascript
const flip=(d, a)=>{
  return d === 'R' ? a.sort((a,b) => a - b) : a.sort((a,b) => b - a)
}
```
---

### Problem #15 Find Nearest Square numer<a name="problem15"></a>

```javascript
function nearestSq(n){
  let root = Math.sqrt(n)
  let lowerRoot  = Math.floor(root)
  let lower = lowerRoot * lowerRoot
  let higher = (lowerRoot + 1) * (lowerRoot + 1)
  return (n - lower) <= (higher -n ) ? lower : higher
}
```

Example: 

```javascript
nearestSq(111);
```

1. Math.sqrt(111) returns 10.539230484541326.
2. Math.floor(10.539230484541326) returns 10.
3. lowerRoot * lowerRoot returns 100.
4. (lowerRoot + 1) * (lowerRoot + 1) returns 121.
5. (n - lower) <= (higher - n) returns true, so lower is returned, which is 100.

--- 

### Problem #16 Count of positives / sum of negatives<a name="problem16"></a>

Given an array of integers.

Return an array, where the first element is the count of positives numbers and the second element is sum of negative numbers. 0 is neither positive nor negative.

If the input is an empty array or is null, return an empty array.

Example
For input [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15], you should return [10, -65].

```javascript
function countPositivesSumNegatives(input) {
  let countPositives = 0;
  let sumNegatives = 0;
  if (input === null || input.length === 0) {
    return [];
  }
  for (let i = 0; i < input.length; i++) {
    if (input[i] > 0) {
      countPositives++;
    } else if (input[i] < 0) {
      sumNegatives += input[i];
    }
  }
  return [countPositives, sumNegatives];
}
```

Output

```javascript
countPositivesSumNegatives([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15]);
// returns [10, -65]
```

---

### Problem #17 Contamination #1-String"problem17"></a>

An AI has infected a text with a character!!

This text is now fully mutated to this character.

If the text or the character are empty, return an empty string.
There will never be a case when both are empty as nothing is going on!!

Note: The character is a string of length 1 or an empty string.

Example
```javascript
text before = "abc"
character   = "z"
text after  = "zzz"
```

```javascript
function contamination(text, char){
  if (!text || !char) {
    return ""
  }
  
  let result = ""
  for (let i = 0; i < text.length; i++) {
    result += char
  }
  
  return result
}
```

Output

```javascript
console.log(contamination("abc","z")) // Output: "zzz"
console.log(contamination("","z")) // Output: ""
console.log(contamination("abc","")) // Output: ""
```

---
