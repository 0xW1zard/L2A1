# How Pick and Omit Help Keep TypeScript Code DRY

## Introduction

We often work with large interfaces. But in many places, we do not need all the properties. If we write new interfaces again and again, our code becomes repetitive and breaks the **DRY** rule.

TypeScript provides two utility types called **Pick** and **Omit** to solve this problem.

---

## The Problem: Code Duplication

Let’s say we have a main interface:

```ts
interface User {
  id: number;
  name: string;
  email: string;
  password: string;
}

// Now, if we want a smaller version of User without the password, we need to rewrite this.


interface UserPreview {
  id: number;
  name: string;
  email: string;
}

// but if we use Pick it would be easy

--> type UserPreview = Pick<User, "id" | "name" | "email">;

//Omit is the opposite of Pick It removes properties we don’t need.

--> type SafeUser = Omit<User, "password">;
```

**Conclusion**

Pick and Omit help us create smaller versions of interfaces without rewriting code. They keep our TypeScript code clean, safe, and easy to manage.