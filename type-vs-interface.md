# Type vs Interface in TypeScript: Which One Should You Use?

## Introduction

When I started learning TypeScript, I was confused about `type` and `interface`. Both describe the shape of data, and they look almost the same. But they are not identical. In this post, I explain the main differences in simple words.

## Body

**1. Declaration merging.** An `interface` can be declared more than once, and TypeScript merges the parts into one. A `type` cannot do this and gives an error.

```ts
interface User { name: string; }
interface User { age: number; }
// User has both name and age
```

**2. Flexibility.** A `type` alias can name unions, tuples, and primitives. An `interface` can only describe object shapes.

```ts
type Id = string | number;
type Point = [number, number];
```

**3. Extending.** Interfaces use `extends`, while types combine with the `&` operator. Both give a similar result.

```ts
interface Admin extends User { role: string; }
type Staff = User & { role: string };
```

**4. When to choose.** Use `interface` for objects, classes, and public APIs. Use `type` for unions, tuples, and complex combinations.

## Conclusion

Neither one is better in every case. A simple rule is: choose `interface` for objects and `type` for everything else. Most importantly, stay consistent in your project so your code is easy to read.
