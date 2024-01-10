
# CONST VS. VAL


In Kotlin, **`const`** and **`val`** are used to declare values that cannot be changed, but they have different meanings and contexts.

# Const

* Used to declare values that are compile-time constants.
* It can only be used on top-level properties (outside of any function or class) or on companion object members.
* The value assigned to a constant must be a known compile-time value (it cannot be calculated at runtime).
```
const val PI = 3.14159
```

# Val

* Used to declare runtime immutable values (runtime constants).
* It can be used to declare properties in a class, function properties, and local variables.
* The value assigned to a **val** can be known (assigned) at runtime and does not need to be determined at compile-time.

```
val name = readLine()
```

## Utilização do `const val`

The main advantage of using `const val` is performance optimization. A constant declared in this way is replaced by its value at compile time, eliminating the need to access memory at runtime to retrieve the constant's value.

Another advantage is that constants declared like this are treated as literal values, meaning they can be used in expressions that require a known compile-time constant value. This includes, for example, array size definition, assigning values to annotations, and other situations where a constant value is required.