# Table of Content

| Language      | Difficulty    | Problem Name  |
| ------------- |:-------------:| -----:|
| JavaScript    | 8 kyu         | [Even or Odd](#problem1)|
| JavaScript    | 8 kyu         | [Add Length](#problem2)|
| JavaScript    | 8 kyu         | [Vowel remover](#problem3)||
| JavaScript    | 8 kyu         | [Quarter of the year](#problem4)||

---

### 8 kyu Even or Odd<a name="problem1"></a>

Create a function that takes an integer as an argument and returns "Even" for even numbers or "Odd" for odd numbers.

```javascript
function evenOrOdd(number) {
  return (number % 2 === 0 ? 'Even' : 'Odd')
}

console.log(evenOrOdd(2)) // Output: Even
console.log(evenOrOdd(3)) // Output: Odd
```
---

### 8 kyu Add Length<a name="problem2"></a>

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

### 8 kyu Vowel Remover<a name="problem3"></a>

Create a function called shortcut to remove the lowercase vowels (a, e, i, o, u ) in a given string.

Examples

```javascript
"hello"     -->  "hll"
"codewars"  -->  "cdwrs"
"goodbye"   -->  "gdby"
"HELLO"     -->  "HELLO"
```

```javascript
function shortcut (string) {
   const noVowels = string.replace(/[aeiou]/gi, '')
   return noVowels
}

console.log(shortcut('how are you today?')); // Output: hw r y tdy?
```
---

### 8 kyu Quarter of the year<a name="problem4"></a>

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
