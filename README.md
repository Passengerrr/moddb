# moddb
> npm i moddb

Examples

```js
const MODLOFF = require("moddb")
const db = new MODLOFF({
    "dbName": "test", // Our DB file name.
    "dbFolder": "database", // Our DB folder name.
    "noBlankData": true,
    "readable": true,
    "language": "en" // You can write "tr" or "en".
})

db.set("x.y.z", "abc") // abc

db.get("x") // {y: {z: "abc"}}
db.all() // {x: {y: {z: "abc"}}}

db.push("a", "hello") //  ["hello"]
db.push("a", "world") //  ["hello", "world"]
db.unpush("a", "hello") // ["world"]

db.push("b", {test: "moddb"}) // [{test: "moddb"}]
db.push("b", {test2: "moddb2"}) // [{test: "moddb"}, {test2: "moddb2"}]
db.delByPriority("b", 1) // [{test2: "moddb"}]
db.setByPriority("b", {newtest:"hey this is edited"} 1) // [{newtest:"hey this is edited"}]

db.delete("x") // true
db.deleteAll() // true
```

