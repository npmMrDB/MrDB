# ***MrDB***

## MrDB is a module made to save your variables in local db


# ***Instalation***
```
npm i mrdb
```

## **<span style="color:lime">Pros</span>**
#### Save your variables in a json using functions or even manually
#### MrDB is a DB module that has no dependents

## **<span style="color:red">Cons</span>**
#### Easily hackable
#### Everything must have bugs, even real life has!
<br>

# ***Usage***
## Set variable
```js
var db = require('mrdb')
db = new db('mylocaldb')

console.log(db.get("")) // expected output: {}
db.set("string", "I am a string!")
console.log(db.get("")) // expected output: {string: 'I am a string!'}
```

## Set a property into a object variable
```js
var db = require('mrdb')
db = new db('mylocaldb')

console.log(db.get("")) // expected output: {}
db.set("obj", {})
console.log(db.get("")) // expected output: {obj: {}}
db.set("obj.code", "MRDB-UBBO-THGX")
console.log(db.get("")) // expected output: {obj: {code: "MRDB-UBBO-THGX"}}
```

## Delete variable or property
```js

db.set("obj", {a:2})
console.log(db.get("")) // Expected output: { obj: { a: 2 } }
db.delete("obj.a")
console.log(db.get("")) // Expected output: { obj: {}}
db.delete("obj")
console.log(db.get("")) // Expected output: {}
```

## Push to array or Add number
#### Add and Remove are not avaliables functions anymore
### Why?
#### Now you can use MrDB#update() <`db.update`> to
#### update changes that has not been done by Set or Delete
#### to the json
## Example
```js
var db = require('mrdb')
db = new db('mylocaldb')

db.bestUser = "all of them" // makes a change that dont affect json
db.update(); // updates the change to json
db.get('') // Expected output: {betsUser: "all of them"}
```

<br>

--- 
<br>

# Being made with JS and ❤ by MrChrys