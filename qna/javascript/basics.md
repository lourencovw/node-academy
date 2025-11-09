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