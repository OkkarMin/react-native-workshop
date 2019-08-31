# Baby Steps into React Native

Learning new technology can be _daunting_. When I first started learning about React Native I dove right into it. Started off by reading documentations which was _time-consuming_.

In this workshop, we are going to learn about React Native's Core Components which will allow you to create an application at the end using _'Baby Steps'_ approach. Taking one step at a time towards our final application. All within 2 hours.

With this, I hope to _reduce friction_ at the start of your React Native learning journey.

---

## JavaScript refresher

Before we continue, let us take a look at bascic JavaScript required for our _Baby Steps_

### Variables

#### Declaration

Do use `const` and `let` for variables. Do not use `var`

```js
const count = 10

for (let i=0, i<count; i++) {
  console.log(`Hello ${count}`)
}
// 0, 1, 2, 3, ..., 9
```

#### String interpolation

Variables can be used in multiple combination with strings. Below are two most common way

Notice the use of `backtick` with `${...}`

```js
const name = 'Okkar'

console.log('Hello ' + name)
console.log(`Hello ${name}`)
// Hello Okkar
```

### Equality

When checking for equality in JavaScript, it is recommended to use three equals `===`

```js
const a = 1 // integer
const b = '1' // string
const c = 1 // integer

console.log(a == b) // true
console.log(a === b) // false
console.log(a === c) // true
```

### Data Structures

#### Array

```js
const anArray = ['o', 'k', 'k', 'a', 'r']

console.log(anArray[1]) // k
```

#### Object

```js
const object = {
  // key : value
  a: 1,
  b: 'Okkar'
}

console.log(object.b) // Okkar
```

#### Nested Object

```js
const nestedObject = {
  a: 1,
  b: 'Okkar',
  c: {
    d: 'Min',
    e: 25
  }
}
```

`c` is a key which contains the value of another object `{d: "Min", e: 25}`

### Functions

Two common way to declare functions, prefers arrow function over traditional function

```js
// traditional
function say(name) {
  console.log(`Hello ${name}`)
}

// arrow
const say = name => {
  console.log(`Hello ${name}`)
}

say('Okkar Min') // Hello Okkar Min
```

### Spreading

This is a little bit tricky, but you can do it!

```js
const numbers = [1, 2, 3]
const twice = [...numbers, ...numbers] // [1,2,3,1,2,3]

const letters = ['x', 'y', 'z']
const thrice = [...numbers, ...letters, ...numbers]
// [1,2,3,'x','y','z',1,2,3]
```

Spreading : takes an iterable and give out elements in iterable

### De-structuring

Another tricky fellow

```js
const user = {
  studentID: 'OMIN001',
  fullName: {
    firstName: 'Okkar',
    lastName: 'Min'
  }
}

// OMIN001
let studentID = user.studentID
console.log(studentID)

let { studentID } = user
console.log(studentID)

// Okkar Min
let firstName = user.fullName.firstName
let lastName = user.fullName.lastName
console.log(firstName + ' ' + lastName)

let { firstName, lastName } = user.fullName
console.log(`${firstName} ${lastName}`)
```
