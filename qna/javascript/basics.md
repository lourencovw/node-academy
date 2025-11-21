# 🟨 Javascript Basics - Interview Q&A

A collection of fundamental Javascript interview questions to help you master the core concepts behind the language.

---

## 1. What are the different data types in Javascript?

Javascript has **primitive** and **reference** types.

**Primitive types:**

- `string`
- `number`
- `boolean`
- `bigint`
- `symbol`
- `undefined`
- `null`

**Reference types:**
- `objects`
- `array`
- `function`
- `date`, `map`, `set`, etc.

Primitive values are immutable and stored directly in memory, while reference types are stored as memory references.

---
## ⚙️ 2. What is the difference between `var`, `let`, and `const`?

| Keyword | Scope | Reassignment | Redeclaration | Hoisting |
|----------|--------|---------------|---------------|-----------|
| `var` | Function | ✅ Yes | ✅ Yes | ✅ (initialized as `undefined`) |
| `let` | Block | ✅ Yes | ❌ No | ✅ (but not accessible before declaration) |
| `const` | Block | ❌ No | ❌ No | ✅ (but not accessible before declaration) |

Use `let` for variables that change and `const` for constants. Avoid `var` in modern code.

---
## 🔄 3. What is the difference between `==` and `===`?

- `==` (loose equality) compares values **after type coercion**.  
- `===` (strict equality) compares both **value and type**.

👉 Example:
```js
0 == '0'   // true
0 === '0'  // false
```
---
## 4. What is the difference between `null` and `undefined` ?

| Value | Meaning | Type |
|-------|---------|------|
| `undefined` | A variable has been declared but not assigned | `"undefined"` |
| `null` | Explicitly set to "no value" | `"object"` (a historical quirk)  |

---
## 5. What are truthy and falsy values

```js
const falsyValues = [false, 0, "", null, undefined, NAN]
```
Everything else is `truthy`.

---

## 6. What is hoisting?
Hoisting is JavaScript's default behavior of moving declaration to the top of their scope before execution.

Example:
```js
console.log(a); //undefined
var a = 5;
```
With `let` or `const`, variables are hoisted but not initialized (Temporal Dead Zone), so accessing them before declaration causes a **ReferenceError**.

