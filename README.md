# Table of Content

| No.      | Questions    |   
| ------------- |:-------------:| 
| 01    |[What are the possible ways to create objects in JS](#nr1)|
| 02    |[Add Length](#problem2)|
| 03    | [Vowel remover](#problem3)||

---

### Number #1 What are the possible ways to create objects in JS<a name="nr1"></a>

In JS, there are several ways to create objects: 

1. Object Literal Notation
<details>
  <summary>Explanation</summary>
  You can create an object using object literal notaion by definig its properties and values in curly braces
  <br>
  
```javascript
const person = {
  name: 'John',
  age: 30,
  gender: 'Male'
};
</details>
```

2. Constructor Functions
<details>
  <summary>Explanation</summary>
  You can create an object using constructor functions in JS. Constructor functions are used to create multiple instances of an object withe the same properties amd methods. To create an object using constructor functions, use the 'new' keyword to instantiate an object.
  <br>
  
```javascript
function Person (name, age, city) {
  this.name = name;
  this.age = age;
  this.city = city;
}

const person = new Person('John', 30, 'New York')
</details>
```

