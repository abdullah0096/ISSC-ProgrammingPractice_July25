# `switch` Statement

The `switch` statement is a clean way to select one of many code blocks to execute based on the value of a variable. 
It is often preferable to lengthy `if-else` chains when checking a single variable against multiple constant values.

---

## Syntax of `switch`

```c
switch (expression) {
    case constant1:
        // Code to execute if expression == constant1
        break;
    case constant2:
        // Code to execute if expression == constant2
        break;
    // more cases...
    default:
        // Code when no case matches
        break;
}
````

* The **expression** must be an **integral type**: `int`, `char`, or `enum`.
* Each **case label** must be a **unique, compile-time constant integral value**.
* The **break** statement prevents fall-through to subsequent cases.
* The **default** case is optional but recommended for handling unmatched values.

---

## ✅ What Types Can You Use in `switch`?

### **Allowed:**

* `int`
* `char`
* `enum`
* `bool` (from `stdbool.h`, implemented as integer 0 or 1)

### **Not Allowed:**

* Floating-point types (`float`, `double`)
* Strings
* Structs or arrays
* Variables or expressions as case labels (only constants allowed)

---

## Can You Use a Boolean Condition in `switch`?

**No.** You **cannot** use a Boolean condition (like `x > 5`) as a `case` label:

```c
switch (x) {
    case (x > 5): // Invalid: case labels must be constant integers.
        // ...
}
```

* `switch` matches values exactly.
* Use `if-else` for ranges or complex conditions.

**Note:**
You *can* use a Boolean *variable* as the switch expression (e.g., `0` or `1`), but this is rare.

---

## Common Mistakes When Using `switch`

* **Forgetting `break`:** Causes *fall-through*, unintentionally executing subsequent cases.
* **Duplicate case values:** Each `case` label must be unique.
* **Non-constant or variable case labels:** Must be known at compile-time.
* **Missing `default` case:** Leaves some values unhandled.
* **Declaring variables inside `case` without `{}`:** Causes compilation errors.
* **Using expressions or ranges as case labels:** Not allowed.
* **Uncommented fall-through:** If intentional, always comment it.

---

## Tips for Writing Effective `switch` Statements

* Always use `break`, unless intentional fall-through (and clearly comment it).
* Use braces `{}` when declaring variables inside cases.
* Always include a `default` case for safety.
* Use `switch` for equality checks on integral types.
* Keep all case values unique and compile-time constants.

---

## 🧪 Example of a `switch` Statement

```c
int day = 4;

switch (day) {
    case 1: 
        printf("Monday\n"); 
        break;
    case 2: 
        printf("Tuesday\n"); 
        break;
    case 3: 
        printf("Wednesday\n"); 
        break;
    case 4: 
        printf("Thursday\n"); 
        break;
    case 5: 
        printf("Friday\n"); 
        break;
    case 6: 
        printf("Saturday\n"); 
        break;
    case 7: 
        printf("Sunday\n"); 
        break;
    default: 
        printf("Invalid day\n"); 
        break;
}
```

**Output:**

```
Thursday
```

---

## `switch` vs `if-else`

| Feature          | `switch`                              | `if-else`                 |
| ---------------- | ------------------------------------- | ------------------------- |
| Expression Types | Only `int`, `char`, `enum` (integral) | Any expression            |
| Case Types       | Unique constant values                | Conditions or expressions |
| Range Checks     | ❌ Not supported                       | ✅ Supported               |
| Fall-through     | ✅ Supported (use `break`)             | ❌ Not applicable          |
| Readability      | ✅ Clear for many discrete values      | ❌ Can become lengthy      |

---

## Conclusion

The `switch` statement is an easy and readable way to handle multiple discrete values of integral types. Remember its limitations and avoid common pitfalls like missing `break` or using invalid case labels.

For complex conditions or range checks, prefer `if-else`.

---

#### ✨ *Just Try !*