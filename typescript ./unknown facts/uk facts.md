## 1. TypeScript doesn’t exist at runtime

After compilation, **all TypeScript types are removed**!  
They exist only during development to catch errors — in the final JavaScript output, there are **no types**.

Example:

`let age: number = 20;`

After compile:

`let age = 20;`

🧠 So, types are only for compile-time safety — browsers never see them.

---

## ⚡ 2. TypeScript supports _literal types_

You can make a variable accept only a specific set of values:

`let direction: "left" | "right" = "left"; direction = "right"; // ✅ OK direction = "up";    // ❌ Error`

So here, the variable can only be `"left"` or `"right"` — nothing else.

---

## ⚡ 3. `const` variables are automatically inferred as literal types

`const role = "admin"; // TypeScript infers the type as "admin", not just string!`

That means `role` can **never** be changed to another value.

---

## ⚡ 4. The `never` type means “impossible to return”

Used for functions that never return a value.

`function throwError(): never {   throw new Error("Something went wrong!"); }`

🧠 It tells TypeScript that this function either throws an error or runs forever.

---

## ⚡ 5. `unknown` is safer than `any`

- `any` disables type checking completely.
    
- `unknown` still **forces** you to check the type before using it.
    

Example:

`let data: unknown = "Rohit"; data.toUpperCase(); // ❌ Error  if (typeof data === "string") {   data.toUpperCase(); // ✅ Safe }`

---

## ⚡ 6. Arrays can be made read-only

You can prevent changes to an array by marking it as `readonly`.

`const nums: readonly number[] = [1, 2, 3]; nums.push(4); // ❌ Error – can’t modify a readonly array`

Useful when you want immutable data (data that can’t change).

---

## ⚡ 7. You can create your own custom types using `type` and `interface`

Example:

`type User = { name: string; age: number }; interface Product { id: number; name: string; }  let user: User = { name: "Rohit", age: 19 }; let item: Product = { id: 101, name: "Laptop" };`

🧠 These help structure data properly in larger projects.

---

## ⚡ 8. TypeScript allows _Union_ and _Intersection_ types

### 🌀 Union — means “either-or”

`let value: string | number; value = 10; value = "Rohit";`

### 💥 Intersection — means “combine”

`type A = { name: string }; type B = { age: number }; type C = A & B;  let person: C = { name: "Rohit", age: 19 };`

---

## ⚡ 9. You can use _type aliases_ for reusable types

It makes your code cleaner and easier to maintain.

`type Status = "success" | "error" | "loading"; let current: Status = "loading";`

---

## ⚡ 10. TypeScript catches type errors _before_ running

It does **static type checking**, meaning it finds mistakes even before the program runs —  
so your code becomes more reliable and bug-free 💪

---