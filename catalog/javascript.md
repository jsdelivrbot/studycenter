# What is the output of below code?

```
let firstName = Symbol("firstName");
console.log(firstName);
```

1.  `Symbol(firstName)`
2.  `firstName`
3.  syntax error

> > > >

# What is the output of below code?

```
var text = 'outside';
function logIt(){
  console.log(text);
  var text = 'inside';
};
logIt();
```

1.  `undefined`
2.  outside
3.  inside

> > > >

# What is the output of below code?

```
let firstName = new Symbol("firstName");
console.log(firstName);
```

1.  Uncaught TypeError: Symbol is not a constructor
2.  `Symbol(firstName)`
3.  `firstName`
4.  syntax error

> > > >

# What is the output of below code?

```
let map = Object.create(null);
let key1 = {};
let key2 = {};

map[key1] = "foo";

console.log(map[key2]);
```

1.  foo
2.  undefined
3.  null
4.  syntax error

``

<p>Object only accept a String or Number as key.</p>
<p>when you add an Object as key to an Object, it convert it into a String value. in this case "[object Object]". Now, even though key1 and key2 are different Objects, there String value is still "[object Object]", which same.
Hence, we will get "foo" as output.</p>
``

> > > >

# What is the log value in first iteration

```
const set = new Set(["1", "2", "3"]);

set.forEach((arg1, arg2, arg3) => {
   console.log(arg1, arg2);
});
```

1.  1 1
2.  1 0
3.  1 Set(3) {"1", "2", "3"}
4.  1 undefined

``

<p>
The strange difference between the set version of forEach() and the array version is that the first and second arguments to the callback function are the same. While this might look like a mistake, there’s a good reason for the behavior.
</p>
<p>
The other objects that have forEach() methods (arrays and maps) pass three arguments to their callback functions. The first two arguments for arrays and maps are the value and the key (the numeric index for arrays).
Sets do not have keys, however. The people behind the ECMAScript 6 standard could have made the callback function in the set version of forEach() accept two arguments, but that would have made it different from the other two. Instead, they found a way to keep the callback function the same and accept three arguments: each value in a set is considered to be both the key and the value. As such, the first and second argument are always the same in forEach() on sets to keep this functionality consistent with the other
forEach() methods on arrays and maps.
</p>
``

> > > >

# How to convert below set to array?

```
const set = new Set(["1", "2", "3"]);
```

1.  [...set] or Array.from(set.values())
2.  set.toArray()
3.  set.values()
4.  set.entries()

``

<p>
Any object which return iterator, including Set, can be converted into an Array using spread notation.
</p>
[...set] is the quickest way.
<p>
Array.from(set.values()) will also work.
</p>
set.values() and set.entries() returns iterator and not an Array.

``

> > > >

# Why we do not have built-in iterators in WeakSet and WeakMap?

1.  Managing weak references means there’s no way to know exactly how many values are in these collections, which also means there’s no way to iterate over them.
2.  Weak version of Set and Map are scale down version, Hence they don't have this advance feature.
3.  For better performance
4.  Statement is untrue.

> > > >

# Can object be spread in Array, like below

```
const arr = [1, 2];
const obj = {
  a: "a",
  b: "b"
};
const newArr = [...arr, ...obj];
```

1.  Yes, Only if it has a generator defined- otherwise it will give error: Uncaught TypeError: obj is not iterabl .
2.  Yes, all object can be spread in array.
3.  No, object can only be spread in another object.

> > > >