# Access Modifiers in TypeScript: Controlling Who Can Use Your Data

## Introduction

In object-oriented programming, we often want to protect the data inside a class. TypeScript gives us access modifiers for this job. They decide which parts of a class can be used from outside. In this post, I explain `public`, `private`, `protected`, and `readonly` in simple words.

## Body

**1. `public`.** This is the default. Anyone can read or change a public member from anywhere.

```ts
class Account {
  public owner: string;
  private balance = 0;
  protected type = "saving";
  readonly id: number;

  constructor(owner: string, id: number) {
    this.owner = owner;
    this.id = id;
  }
}
```

**2. `private`.** A private member can only be used inside its own class. Outside code gets a compile error.

```ts
const acc = new Account("Sharif", 1);
acc.balance = 500; // Error: 'balance' is private
```

**3. `protected`.** This is like private, but child classes can also use it.

```ts
class Premium extends Account {
  show() { return this.type; } // Allowed
}
```

**4. `readonly`.** A readonly property can be set once, in the constructor, and cannot change later.

```ts
acc.id = 2; // Error: 'id' is read-only
```

## Conclusion

Access modifiers make our classes safer and easier to maintain. Use `public` for open features, `private` for hidden data, `protected` for family classes, and `readonly` for values that must never change. Remember that these checks happen at compile time, not at runtime.
