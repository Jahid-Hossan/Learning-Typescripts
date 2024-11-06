# Basic Data Types in TypeScript

This README file provides an overview of the fundamental data types in TypeScript. Understanding these data types is essential for effectively using TypeScript’s type-checking capabilities, which help catch errors at compile time and make the code more readable and maintainable.

## Table of Contents

1. [Introduction to TypeScript Data Types](#introduction-to-typescript-data-types)
2. [Primitive Types](#primitive-types)
   - [String](#string)
   - [Number](#number)
   - [Boolean](#boolean)
   - [Null](#null)
   - [Undefined](#undefined)
   - [BigInt](#bigint)
   - [Symbol](#symbol)
3. [Special Types](#special-types)
   - [Any](#any)
   - [Unknown](#unknown)
   - [Void](#void)
   - [Never](#never)
4. [Complex Types](#complex-types)
   - [Array](#array)
   - [Tuple](#tuple)
5. [Conclusion](#conclusion)

---

## Introduction to TypeScript Data Types

TypeScript is a superset of JavaScript that adds static typing. With TypeScript, we can specify data types to variables, function parameters, and return values, which enhances code reliability and readability. Below is an overview of the most commonly used TypeScript data types.

---

## Primitive Types

### String

Represents textual data. Strings are wrapped in single, double, or backticks.

```typescript
let firstName: string = "Alice";
```

### Number

Represents both integer and floating-point numbers. Unlike JavaScript, TypeScript doesn't differentiate between different numeric types.

```typescript
let age: number = 30;
let score: number = 95.5;
```

### Boolean

Represents a true/false value.

```typescript
let isActive: boolean = true;
```

### Null

Represents the absence of any value.

```typescript
let emptyValue: null = null;
```

### Undefined

Represents a variable that has been declared but not yet assigned a value.

```typescript
let notAssigned: undefined;
```

### BigInt

Allows representation of integers beyond the safe limit for the `number` type. Created by appending `n` to the end of the integer.

```typescript
let largeNumber: bigint = 123456789012345678901234567890n;
```

### Symbol

Represents a unique identifier primarily used as object keys.

```typescript
let uniqueID: symbol = Symbol("id");
```

---

## Special Types

### Any

A flexible type that can hold any data type. This type is often discouraged as it removes type-checking.

```typescript
let randomValue: any = "Hello";
randomValue = 42;
```

### Unknown

A safer version of `any`. Before performing any operations on it, the value must be type-checked.

```typescript
let uncertainValue: unknown = "Hello";
if (typeof uncertainValue === "string") {
  console.log(uncertainValue.toUpperCase());
}
```

### Void

Typically used as the return type for functions that do not return a value.

```typescript
function logMessage(message: string): void {
  console.log(message);
}
```

### Never

Represents the type of values that never occur, often used for functions that throw errors or have infinite loops.

```typescript
function throwError(errorMsg: string): never {
  throw new Error(errorMsg);
}
```

---

## Complex Types

### Array

Represents a list of values of a single type. TypeScript supports both generic (`Array<type>`) and shorthand syntax (`type[]`).

```typescript
let scores: number[] = [85, 92, 78];
```

### Tuple

Represents an array with a fixed number of elements, where each element may have a different type.

```typescript
let person: [string, number] = ["Alice", 25];
```

---

## Conclusion

TypeScript's static typing system provides powerful tools to make code more predictable, maintainable, and safer. By utilizing basic data types effectively, developers can avoid many common errors that might otherwise go unnoticed in JavaScript.

---
