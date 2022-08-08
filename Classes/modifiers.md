## Modifiers

public - this method (or property) can be called anywhere, anytime

private - this method (or property) can only be called by other methods in this class (similar to # in regular JavaScript)

protected - this method (or property) can be called by other methods in this class, or by other methods in child classes

readonly - property cannot be changed

## Parameter property shorthand

```
class Player {
  constructor(public first: string, public last: string) {
    // don't have to initialize this.first = first !!!!!!
  }
}
```

## Interfaces

- classes can implement multiple interfaces

## abstract

- cannot create a new instance of class
- used to define methods that must be implemented by child class

```
abstract class Employee {
  constructor(public first: string) {}
  abstract getPay(): number; // does not exist here but required on all children, almost like interface
}

class FullTimeEmployee extends Employee {
  getPay() {
    return 4
  }
}

```
