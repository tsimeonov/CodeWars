# Table of Content

| Language      | Difficulty    | Problem Name  |
| ------------- |:-------------:| -----:|
| JavaScript    | 8 kyu         | [Even or Odd](#problem1)|
| JavaScript    | 8 kyu         | [Add Length](#problem2)|
| JavaScript    | 8 kyu         | [Vowel remover](#problem3)||
| JavaScript    | 8 kyu         | [Quarter of the year](#problem4)||
| JavaScript    | 8 kyu         | [The 'if' function](#problem5)||
| JavaScript    | 8 kyu         | [Price of Mangoes](#problem6)||
| JavaScript    | 8 kyu         | [Powers of 2](#problem7)||

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
```

```javascript
function shortcut (string) {
   const noVowels = string.replace(/[aeiou]/gi, '')
   return noVowels
}

console.log(shortcut('how are you today?')); // Output: hw r y tdy?
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
  }
}
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

