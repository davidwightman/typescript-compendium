## Types and Interfaces

```
interface Person {
  name: string;
  last: string;
}

type Person = {
  name: string;
  lastName?: string; // optional property
}
```

- interface describe shape of object
- interfaces can be reopened and added on to
- use extends key word with types use & (intersection type)
