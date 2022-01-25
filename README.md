# What is This?
Allow users to input numbers/strings with commasRemove commas for string or numbers and check if the number/string contains commas

-Add commas
-Remove commas
-Check if string/num contains commas

# Installation

`npm i no-comma`

Usage
```js
const noComma = require('no-comma')

const isComma = noComma.isComma
const removeComma = noComma.removeComma
const addComma = noComma.addComma


const number = '5,000,000'
const noNumber = '5000000'


isComma(noNumber) // returns false
isComma(number) // returns true

removeComma(number) // returns 5000000
addComma(noNumber) // returns 5,000,000
```

Examples
```js
const noComma = require('no-comma')

const isComma = noComma.isComma
const removeComma = noComma.removeComma
const addComma = noComma.addComma


// req.body.salary = 4,000,000
// req.body.age = 12

const salaryNoComma = removeComma(req.body.salary) // returns 4000000

const salaryAdding = (salaryNoComma + age) // returns 4000012

console.log(addComma(salaryAdding)) // returns 4,000,012
```