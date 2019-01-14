### node-cache
---
https://github.com/ptarjan/node-cache

```
npm install memory-cache --save
```

```js
var cache = require('memory-cache');
cache.put('foo', 'bar');
console.log(cache.get('foo'));
cache.put('houdini', 'disappear', 100, function(key, value){
  console.log(key + ' did ' + value);
});
console.log('Houdini will now ' + cache.get('houdini'));
setTimeout(function(){
  console.log('Houdini is ' + cache.get('houdini'));
}, 200);
var newCache = new cache.Cache();
newCache.put('foo', 'newbaz');
setTimeout(function(){
  console.log('foo in old cache is ' + cache.get('foo'));
  console.log('foo in new cache is ' + newCache.get('foo'));
}, 200);
```

```
```


