# Table of Content

| No.      | Questions    |   
| ------------- |:-------------:| 
| 01    |[What are the possible ways to create objects in JS](#1-ways-to-create-objects)|
| 02    |[What is the difference between Call, Apply and Bind](#2-difference-between-call-apply-and-bind)||

---



### 1. Ways to create objects
  
<details>
  <summary>Object literals</summary>
  You can create an object using an object literal, which is a comma-separeted list of name-value pairs enclosed in curly brases {}.
  
```javascript
  const myObj = {
    name: 'John',
    age: 30,
    city: 'New York'
   };
```
</details>

<details>
  <summary>Object constructos</summary>
    You can use an object constructor function to create an object. The constructor function is called the 'new' keyword to create an new instance of the object.
  
```javascript
  function Person (name, age, city) {
    this.nake = name;
    this.age = age;
    this.city = city
   }
  
  const john = new Person('John', 30, 'New York')
```
</details>
  
<details>
  <summary>Object.create()</summary>
    You can use the 'Object.create()' method to create a new object that inherits from an existing object.
  
```javascript
  const person = {
    name: 'John',
    age: 30,
    city: 'New York'
   }
  
   const john = Object.create(person)
   john.name = 'John Doe'
```
</details>

<details>
  <summary>ES6 Classes </summary>
    You can create an object using a class declaration, which is a syntactical sugar over constructor functions.
  
```javascript
  class Person {
    constructor (name, age, city) {
      this.name = name;
      this.age = age;
      this.city = city;
    }
  }
  const john = new Person('John', 30, 'New Yourk')
```
</details>

### 2. Difference between call apply and bind
  
<details>
  <summary>Call</summary>
  The call() method invokes a function with a given this value and arguments provided one by one.
  
```javascript
  let employee1 = {firstName: 'John', lastName: 'Rodson'};
  let employee2 = {firstName: 'Jimmy', lastName: 'Baily'};
  
  function invite(greeting1, greeting2) {
    console.log(`${greeting1} ${this.firstNae} ${this.lastName}`)
  }
  
  invite.call(employee1, 'Hello', 'How are you'); // Hello John Rodson, How are you?
  invite.call(employee2, 'Hello', 'How are you'); // Hello jimmy Baily, How are you>
```
</details>

<details>
  <summary>Apply</summary>
  Invokes the function with a given this value and allows you to pass in arguments as an array.
  
```javascript
  let employee1 = {firstName: 'John', lastName: 'Rodson'};
  let employee2 = {firstName: 'Jimmy', lastName: 'Baily'};
  
  function invite(greeting1, greeting2) {
    console.log(`${greeting1} ${this.firstNae} ${this.lastName}`)
  }
  
  invite.apply(employee1, 'Hello', 'How are you'); // Hello John Rodson, How are you?
  invite.apply(employee2, 'Hello', 'How are you'); // Hello jimmy Baily, How are you?
```
</details>

<details>
  <summary>Bind</summary>
  Returns a new functon, allowing you to pass any number of arguments.
  
```javascript
  let employee1 = {firstName: 'John', lastName: 'Rodson'};
  let employee2 = {firstName: 'Jimmy', lastName: 'Baily'};
  
  function invite(greeting1, greeting2) {
    console.log(`${greeting1} ${this.firstNae} ${this.lastName}`)
  }
  
  let inviteEmployee1 = invite.bind(employee1)
  let inviteEmployee2 = invite.bind(employee2)
  invite.apply(employee1, 'Hello', 'How are you'); // Hello John Rodson, How are you?
  invite.apply(employee2, 'Hello', 'How are you'); // Hello jimmy Baily, How are you?
```
</details>

Call and Apply are pretty interchangeable. Both execute the current function immediately. You can remember by treating Call is for comma (separated list) and Apply is for Arry.
Whereas Bind creates a new function that will have **_this_** set tot the first parameter passed to bind().

