Functional is a library for functional programming in JavaScript. It defines the standard higher-order functions such as map, reduce (aka foldl), and select (aka filter). It also defines functions such as curry, rcurry, and partial for partial function application; and compose, guard, and until  for function-level  programming. And all these functions accept strings, such as 'x -> x+1', 'x+1', or '+1' as synonyms for the more verbose function(x) {return x+1}.

Functional lets you write code such as this:
```
  map('x+1', [1,2,3])
  select('x>2', [1,2,3,4])
  some('_.length < 3', 'are there any short words?'.split(' '))

  // double the items in a list
  map('_/2', [1,2,3])
  // find the odd numbers
  filter('%2', [1,2,3,4])
  // or the evens
  filter(not('%2'), [1,2,3,4])

  Array.prototype.sum = reduce.curry('+', 0).compose('this')
  [1,2,3].sum()
```

  * [Demo](http://osteele.com/sources/javascript/functional/)
  * [Download](http://github.com/osteele/functional-javascript)