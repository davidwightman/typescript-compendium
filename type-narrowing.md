## type narrowing

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
