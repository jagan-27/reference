#### Map 

* Map is like a object but compared to object, map is best for frequent removal or addtion of property
* `yourmap.set()` method is used to set a property to a map with key as first and value as second argument
* `yourmap.size()` method returns the size of the map
* `yourmap.delete(key)` method returns boolean on deletion on element in map
* `get` method takes key as argument and return the value of the key, if not return `undefined`
* `has` method used check the existence of key in the map, returns boolean



```javascript 
const map1 = new Map();
map1.set('a', 'alpha');
map1.set('b', 'beta');
map1.set('g', 'gamma');
map1.set('bar', 'foo');
console.log(map1.delete('bar')); // Expected result: true 
console.log(map1.size); // Expected output: 3 
console.log(map1.get('a')); // Expected output: "alpha"
console.log(map1.has('bar')); //false
```
#### Converstion of map into Array 

```javascript
let obj = new Map()
console.log([...obj.keys()])  // [key1, key2]
console.log([...obj.values()])  // [value1, value2]
console.log([...obj.entries()])  // [[key1, value1], [key2, value2]]
```