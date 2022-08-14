## type narrowing

### The In operator

```
type Cat { meow: () => void}
type Dog { bark: () => void}

const talk = (creature: Cat | Dog) => {
  if ("meow" in creature) {

  creature.meow()
  } else {
    creature.bark()
  }
}


```

### the instanceof

- instanceof is from JavaScript

```
const printFullDate(date: Date | string) {
  if (date instanceof Date) {
    return date.toUTCString()
  } else {
    return new Date(string).toUTCString()
  }
}
```

### Type Predicates

- connects logic of function to narrowing of type

```
function isCat(animal: Cat | Dog): animal is Cat {
  return (animal as Cat).numLives !== undefined
}


```

### discriminated unions

- add discriminent like kind or type

```
interface Rooster {
  kind: "rooster"
}

interface Cow {
  kind: "cow"
}

type FarmAnimal = Pig | Rooster | Cow

function getFarmAnimalSound(animal: FarmAnimal) {
  if (animal.kind === "cow") {
    console.log('moo')
  }
}
```

### exhaustiveness checks with never

- make sure we have exhausted all possible options

```
const _exhaustiveCheck: never = animal; // will throw error
return _exhaustiveCheck;
```
