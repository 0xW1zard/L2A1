# How Generics Help Build Reusable and Type-Safe Code in TypeScript

## What are Generics?

Generics allow us to write one function or component that works with many data types while still keeping type safety.Instead of using any, Generics use a placeholder type (like T) that is decided when the function is used.

## Example:
```ts
//Without Generics (Bad)

function identity(value: any) {
  return value;
}

// No type safety
// Can cause errors

------------------------------------

//With Generics (Good)

function identity<T>(value: T): T {
  return value;
}

//Keeps the correct type
// Works with any data
// Safer and cleaner

```

## Conclusion

Generics help us write flexible, reusable, and type-safe code. They make sure our code works with any data without losing TypeScript safety.