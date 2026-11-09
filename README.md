# TypeScript & OOP Assignment 1

**Student:** Sharif Uddin

## About

This project has my solutions for Assignment 1. It covers basic types, generics, interfaces, type narrowing, Promises, and classes in TypeScript.

## Files

- `solutions.ts` – all 8 coding solutions
- `type-vs-interface.md` – blog post 1
- `type-narrowing.md` – blog post 2

## Solutions

1. `multiplyValue` – optional parameter
2. `processInput` – union types and `typeof`
3. `formatCoordinate` – readonly tuple
4. `concatenateArrays` – generics and rest parameters
5. `Course`, `getPopularCourses` – interface and filter
6. `pluckValues` – generics with `keyof`
7. `Employee`, `Manager` – classes and access modifiers
8. `validateAgeAsync` – async function and Promise

## Blog Posts
 
1. [Type vs Interface in TypeScript](https://github.com/SharifuddinBD/NextLevelSoftwareDevelopmentwithAIEngineering_Assignment_1/blob/main/type-vs-interface.md)
   Explains the main differences between `type` and `interface`, such as declaration merging, flexibility, and extending. It also shows when to use each one.
2. [Access Modifiers in TypeScript](https://github.com/SharifuddinBD/NextLevelSoftwareDevelopmentwithAIEngineering_Assignment_1/blob/main/access-modifiers.md)
   Explains `public`, `private`, `protected`, and `readonly` with simple class examples. It shows how each one controls access to data.


## How to Run

```bash
npm install -g typescript
tsc solutions.ts
```