# Object

#### Keys(yourobj) and Values(yourobj)
- To get the values and keys from object should use `Object.Keys(yourObject)` or `Object.values(yourObject)`
- To iterate the Object use `for-in` loop

```js
const object1 = {
  a: 'somestring',
  b: 42,
  c: false,
};
console.log(Object.keys(object1));
// Expected output: Array ["a", "b", "c"]
```

#### entries(yourobj)

- `Object.entries(yourObject)` return array of key and value 
- To iterate the `Object.entries` use `for-of` loop

```js
const arrayLike = { 0: "a", 1: "b"};
console.log(Object.entries(arrayLike));// [ ['0', 'a'], ['1', 'b'] ]
```
#### delete a key in object

- `delete` keyword can be used to delete a key in an object
-  returns true evertime, even the key not in the object

```js
const arrayLike = { 0: "a", 1: "b"};
console.log(delete arrayLike['0']); // true
console.log(arrayLike); // {1: 'b'}
```
#### Shallow Copy & Deep Copy (Clone)

- Shallow copy is referencing the value to a variable so any change in that variable may affect other variable
- Deep Copy is like creating a new object with same property and assigning to a variable

```js
const arrayLike = { 0: "a", 1: "b"};
const shallowCopy = arrayLike
arrayLike['1'] = 'c'
shallowCopy['0'] = 'b'
console.log(arrayLike); // {0: "b", 1: "c"}
```

##### Ways to create Deep Copy(Clone)

- Using JSON.stringify and JSON.parse
- Using spread operator
- Using assign method in Object

```js
const arrayLike = { 0: "a", 1: "b"};
const deepCopy1 = JSON.parse(JSON.stringify(arrayLike))
const deepCopy2 = {..arrayLike}
const deepCopy3 = Object.assign({}, arrayLike)
arrayLike['1'] = 'c'
deepCopy['0'] = 'b'
console.log(arrayLike); // {"0": "a","1": "c"}
console.log(deepCopy); // {"0": "b","1": "b"}
```


#### Converstion of map into Array 

```javascript
let obj = {}
console.log([...Object.keys(obj)])  // [key1, key2]
console.log([...Object.values(obj)])  // [value1, value2]
console.log([...Object.entries(obj)])  // [[key1, value1], [key2, value2]]
```

### Time Complexity

```js
Object.keys(yourobj) // O(N)
Object.values(yourobj) // O(N)
delete yourobj[key]  //O(1)
youobj[key] // O(1)
```