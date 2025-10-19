## 🔹 1. **Primitive Types**

These are the most basic data types:

|Type|Example|
|---|---|
|`number`|`let age: number = 25;`|
|`string`|`let name: string = "Alice";`|
|`boolean`|`let isOpen: boolean = true;`|
|`null`|`let empty: null = null;`|
|`undefined`|`let u: undefined = undefined;`|
|`bigint`|`let big: bigint = 9007199254740991n;`|
|`symbol`|`let sym: symbol = Symbol("id");`|

---

## 🔹 2. **Object Types**

These represent more complex structures.

### a. **Object**

`let person: { name: string; age: number } = {   name: "John",   age: 30 };`

### b. **Array**

`let numbers: number[] = [1, 2, 3]; let strings: Array<string> = ["a", "b"];`

### c. **Tuple**

A fixed-length array with specific types:

`let user: [string, number] = ["Alice", 25];`

---

## 🔹 3. **Enum**

A way to define named constants.

`enum Color {   Red,   Green,   Blue } let c: Color = Color.Green;`

---

## 🔹 4. **Any**

Can be any type. Avoid if possible (loses type safety).

`let data: any = 42; data = "hello"; data = true;`

---

## 🔹 5. **Unknown**

Like `any`, but safer — requires type checking before use.

`let value: unknown = "test"; if (typeof value === "string") {   console.log(value.toUpperCase()); }`

---

## 🔹 6. **Void**

Used for functions that return nothing.

`function logMessage(): void {   console.log("Hello"); }`

---

## 🔹 7. **Never**

Used for functions that never return (e.g., throw errors or infinite loops).

`function throwError(): never {   throw new Error("Something went wrong!"); }`




## 🔹 8. **Union Types**

Allow a variable to hold more than one type.

`let id: number | string; id = 10; id = "abc";`

---

## 🔹 9. **Literal Types**

Restrict a variable to a specific value.

`let direction: "up" | "down"; direction = "up"; // ✅ direction = "left"; // ❌ Error`

---

## 🔹 10. **Type Aliases & Interfaces**

### a. **Type Alias**

`type Point = {   x: number;   y: number; }; let pt: Point = { x: 10, y: 20 };`

### b. **Interface**

`interface Person {   name: string;   age: number; } let p: Person = { name: "Jane", age: 30 };`