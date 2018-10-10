# Debugging
## Logging
There are various ways to log for debugging.
```js
console.log('%c Variables', 'color: orange')
console.log({ var_a, var_b, var_c })
console.table([var_a, var_b, var_c])
```

## Benchmarking - keep track of durations

```js
console.time('nameOfTimer')
.
.
.
console.timeEnd('nameOfTimer')
```

output `nameOfTimer: timeInMs`

## Stack Trace
```js
console.trace('message')
```
It'll give a stack trace for where it was called and what defined it.

<hr>

## Destructuring
```js
person = { name: 'John', surname: 'Oliver', country: 'UK', ... }

function fullName(person) {
  const { name, surname } = person

  return `${name} ${surname}`
}
```

## Template Literals
```js
const horse = {
    name: 'Topher 🐴',
    size: 'large',
    skills: ['jousting', 'racing'],
    age: 7
}

const { name, size, skills } = horse;
bio = `${name} is a ${size} horse skilled in ${skills.join(' & ')}`
console.log(bio);

// Advanced Tag Example

function horseAge(str, age) {

    const ageStr = age > 5 ? 'old' : 'young';
    return `${str[0]}${ageStr} at ${age} years`;
}

const bio2 = horseAge`This horse is ${horse.age}`;
console.log(bio2)
```

## Spread Syntax
```js
const pikachu = { name: 'Pikachu 🐹'  };
const stats = { hp: 40, attack: 60, defense: 45 }

const lvl0 = { ...pikachu, ...stats }
const lvl1 = { ...pikachu, hp: 45 }

// Arrays

let pokemon = ['Arbok', 'Raichu', 'Sandshrew'];

// Push
pokemon = [...pokemon, 'Bulbasaur', 'Metapod', 'Weedle']

// Shift
pokemon = ['Bulbasaur', ...pokemon, 'Metapod', 'Weedle', ]
```
