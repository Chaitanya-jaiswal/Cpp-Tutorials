# 📚 Computer Programming 1 – Variables & Streams

---

## 📝 Outline
- What is a **stream**?
- **Pre-defined** streams in C++
- **Output** stream (`cout`)
- **Input** stream (`cin`)
- Handling **errors** & stream state
- Reading **boolean** values

---

## 🌊 What Is a Stream?
A **stream** is a (theoretically infinite) sequence of characters used to **communicate** between your program and:
- **Devices** (keyboard, monitor)
- **Files** on disk  

Every stream ends with a special end‐of‐stream marker.

---

## 🚀 Pre-defined Streams
Include the I/O library:
```cpp
#include <iostream>
using namespace std;
```
| Stream  | Purpose                      |
| ------- | -----------------------------|
| `cin`   | Standard **input** (keyboard) |
| `cout`  | Standard **output** (screen)  |
| `cerr`  | Standard **error** (screen)   |

---

## 🖨️ Output Stream (`cout`)
Use the insertion operator `<<` to **write** data:
```cpp
cout << expression1 << expression2 << … << endl;
```
- **Computes** each expression
- **Converts** to characters
- **Sends** to the stream

> **Tip:** `endl` inserts `'
'` and **flushes** the buffer.

### Examples
```cpp
cout << "Hello, World!" << endl;
int year = 2024;
cout << "Year: " << year << endl;
```

---

## ⌨️ Input Stream (`cin`)
Use the extraction operator `>>` to **read** data into variables:
```cpp
cin >> var1 >> var2 >> …;
```
1. **Skips** leading whitespace  
2. **Parses** characters into the target type  
3. **Stores** in the variable  

### Reading Examples
```cpp
char c; float x; int n;
cin >> c >> x >> n;
cout << c << ", " << x << ", " << n << endl;
```

---

## ⚠️ Stream Error State
When a read **fails** (e.g., non-numeric input for an `int`), `cin` goes into an **error state**:
- **Subsequent reads** will also fail until you **clear** it.

### Managing Errors
```cpp
if (cin.fail()) {
  cin.clear();            // reset error state
  cin.ignore(numeric_limits<streamsize>::max(), '\n'); 
}
```
- `cin.clear()` → clear error flags  
- `cin.ignore()` → skip bad input  

---

## 🤔 Checking Stream Status
| Function         | Returns `true` if…                                 |
| ---------------- | -------------------------------------------------- |
| `cin.eof()`      | End-of-stream reached                              |
| `cin.fail()`     | Last operation **failed** or EOF                   |
| `cin.good()`     | No errors, not EOF                                 |

---

## 🔢 Reading Booleans
```cpp
bool b;
cin >> b;
```
- Accepts `0` → `false`, `1` → `true`  
- Any other digit → silently converted (`>1` → `true`)  
- Non-digit → yields `false` but **no error flag**  

> **Warning:** Always validate manually if strict input is needed!

---

## 🎯 Quick-Reference Cheat Sheet

```cpp
#include <iostream>
#include <limits>
using namespace std;

int main() {
  // Output
  cout << "Enter two ints: ";

  // Input with error handling
  int a, b;
  cin >> a >> b;
  if (cin.fail()) {
    cout << "Invalid input!\n";
    cin.clear();
    cin.ignore(numeric_limits<streamsize>::max(), '\n');
    return 1;
  }

  cout << "You entered: " << a << " and " << b << endl;

  // Reading a boolean
  bool flag;
  cout << "Enter 0 or 1: ";
  cin >> flag;
  cout << "Boolean read: " << flag << endl;

  return 0;
}
```

---

😊 _Happy coding!_
