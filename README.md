# Table of Content

| Language      | Difficulty    | Problem Name  |
| ------------- |:-------------:| -----:|
| JavaScript    | 8 kyu         | [Even or Odd](#problem1)|
| JavaScript    | 8 kyu         | [Add Length](#problem2)|
| zebra stripes | are neat      |    $1 |

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
