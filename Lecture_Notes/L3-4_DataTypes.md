# 📊 L3-4: Data Types

## 📝 Outline
- Variables and Constants
- Fundamental Data Types
  - Boolean
  - Integer
  - Real
  - Enum
  - Char

---

## 🅰️ Variables and Constants
### Definition & Declaration
- **Variable**: Named memory location whose value (r-value) can change during execution. Identified by an address (I-value).
  - **Syntax**: `type identifier;` (definition), `type identifier = expression;` (definition w/ init)
    ```cpp
    int x;           // define x
    int y = 3;       // define and initialize y to 3
    extern int z;    // declare z defined elsewhere
    ```
- **Constant**: Named value that cannot change, must be initialized at compile-time.
  - **Syntax**: `const type identifier = expression;`
    ```cpp
    const int KILO = 1024;
    // KILO = 1023; // error: cannot assign to const
    ```

> 💡 Always initialize variables to avoid undefined values!

---

## 🔢 Fundamental Data Types

### 1️⃣ Boolean (`bool`)
- Domain: `{false, true}` (`false` ↔ `0`, `true` ↔ any non-zero int).
- Operators: `!` (NOT), `&&` (AND), `||` (OR) with **lazy evaluation**.
  ```cpp
  bool a = true;
  bool b = false;
  bool c = (a && (b = true)); // b not set, c == false
  ```

### 2️⃣ Integer Types
- **Signed**: `short`, `int`, `long`, `long long` (at least 16, 16, 32, 64 bits respectively).
  - Range for N-bit two's complement: `[-2^(N-1), 2^(N-1)-1]`.
- **Unsigned**: `unsigned short`, `unsigned int`, etc.
  - Range: `[0, 2^N - 1]`.
- **Arithmetic operators**: `+`, `-`, `*`, `/` (integer division), `%` (remainder).
  ```cpp
  int a = 5 / 2;    // 2
  int b = 5 % 2;    // 1
  ```

#### 🔧 Bitwise operators (on unsigned ints)
| Operator | Meaning                    |
|----------|----------------------------|
| `x << n` | left shift by n bits       |
| `x >> n` | right shift by n bits      |
| `x & y`  | bitwise AND                |
| `x | y`  | bitwise OR                 |
| `x ^ y`  | bitwise XOR                |
| `~x`     | bitwise NOT (complement)   |

> 🛠️ Note: Shifting may drop bits or introduce zeros.

### 3️⃣ Real Types
- `float` (≈32-bit, ~7 decimal digits), `double` (≈64-bit, ~15 digits), `long double` (≥80-bit).
- Use `.` or scientific notation with `e/E`.
  ```cpp
  double x = 3.14;
  float  y = 2.5e-3f; // 0.0025
  ```

### 4️⃣ Enumeration (`enum`)
- User-defined set of named integer constants.
  ```cpp
  enum Day { MON, TUE, WED, THU, FRI, SAT, SUN };
  Day today = MON;
  ```
- Optionally assign values:
  ```cpp
  enum Color { RED = 10, GREEN = 15, BLUE = 20 };
  ```

### 5️⃣ Character (`char`)
- Single byte representing a character via encoding (e.g., ASCII).
- Printable: `'A'`, `'0'`, `'+'`, `' '`.
- Arithmetic on `char`: treated as small integers.
  ```cpp
  char c = 'A';        // ASCII 65
  int  code = c + 1;   // 66
  ```

---

## ⚙️ Operators & Expressions

### Assignment Operators
- Simple: `x = y`
- Compound: `x += y` (⇔ `x = x + y`), `x -= y`, `x *= y`, etc.

### Increment / Decrement
- `x++` (postfix: returns old value), `++x` (prefix: returns new value).
  ```cpp
  int x = 5;
  cout << x++ << endl; // prints 5, then x=6
  cout << ++x << endl; // x=7, prints 7
  ```

> ⚠️ Avoid side-effects in complex expressions: evaluation order is unspecified!

### Relational Operators
- `==`, `!=`, `<`, `<=`, `>`, `>=`.

### Mixed-Type Expressions
- **Implicit conversions**: smaller to larger type (promotion), real↔int (truncation).
- **Explicit casts**: `(type)value` or `type(value)`.
  ```cpp
  double r = 3/2;         // 1.0 (int division ➔ double)
  double r2 = 3.0/2;      // 1.5
  int    i = (int)3.9;    // 3
  ```

---

## 📏 The `sizeof` Operator
- returns size in bytes of a type or expression.
  ```cpp
  cout << sizeof(int) << endl;    // e.g., 4
  cout << sizeof x << endl;        // size of variable x
  ```

--- 

> 🎓 *Master these data types and operations to write efficient, correct C++ code!* 🚀
