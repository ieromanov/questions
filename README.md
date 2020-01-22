# questions

### Что выведет `console.log`?
```js
function foo () {
    let a = b = 0;
    a++
    return a;
}
foo();
console.log(typeof a);
console.log(typeof b);
```

```js
let a = ['2', '2', '2', '2'].map(parseInt)
console.log(a);
```

```js
function foo (person) {
  if (persone == { name: 'any' }) {
    return 0;
  }
  return 10;
}

console.log(foo({ name: 'any' }))
```

```js
for (var i = 0; i < 10; i++) {
  setTimeout(() => console.log(i), 0)
}
for (let i = 0; i < 10; i++) {
  setTimeout(() => console.log(i), 0)
}
```

#### доп: Как сделать чтобы работало?
```js
let foo = {
  name: 'bar',
  sayName: () => {
    console.log(this.name)
  }
}

console.log(foo.sayName());
```

### Что выведет `console.log`
```js
var a = [2, undefiend, 1];
a.sort(() => 0)
сonsole.log(a);
```

#### В каком порядке выведутся `console.log`-и
```js
console.log(1);

setTimeout(() => console.log(2), 0)

new Promise((resolve, reject) => {
    console.log(3)
    setTimeout(() => console.log(4), 100);
    resolve(5)
  })
  .then((data) => {
    throw new Error(data)
  })
  .catch((err) => {
    console.log(err.message)
  })
  .then(() => {
    console.log(6)
    return 7
  })
  .catch((err) => {
    console.log(err)
  })
  .finally(() => {
    console.log(8)
  })
```

#### Будет ли ошибка? И что будет в консоли?
```js
funstion foo({ one, two }) {
    return {
        one: one,
        two: two
    }
}

console.log(foo(false))
```
