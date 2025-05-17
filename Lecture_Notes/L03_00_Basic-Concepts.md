# 📘 Basic Concepts (L03_00)

---

## 📋 Outline  
- Overview of the fundamental building blocks of a programming language. citeturn0file2

---

## 🔤 What is a Programming Language? (Recall)  
- **Programming languages** share with natural languages:  
  - **Words**, **symbols**, and **grammatical rules**  
  - Allow us to express instructions in a precise form computers can process citeturn0file2

---

## 🧩 Language = Syntax + Semantics  
- **Syntax**: set of grammatical rules defining how code must be structured  
- **Semantics**: the meaning behind those structures and symbols citeturn0file2

---

## 🔡 Sequence of Words  
- A C++ “word” (token) may include:  
  - **Letters**: `a–z`, `A–Z`, underscore `_`  
  - **Digits**: `0–9`  
  - **Special characters**: `! ^ & * ( ) - + = { } | ~ [ ] ; : " < > ? , . /` citeturn0file2

---

## ↔️ Spaces  
- Whitespace characters separate tokens but are otherwise ignored:  
  - **Space** (` `)  
  - **Tab** (`	`)  
  - **Newline** (`
`) citeturn0file2

---

## 📝 Comments  
- Allow you to annotate code without affecting execution:  
  - **Single-line**: `// this is a comment`  
  - **Multi-line**:  
    ```cpp
    /* this comment
       spans many lines */
    ``` citeturn0file2

---

## 🆔 Identifiers  
- User-defined names for variables, functions, etc.  
- Must begin with a letter or underscore, followed by letters, digits, or underscores  
- Case-sensitive (`MyVar` ≠ `myvar`)  
- **Cannot** use reserved keywords citeturn0file2

---

## 🚩 Keywords  
- Reserved words with special meaning, e.g.:  
  `int`, `return`, `class`, `if`, `while`, `static`, …  
- Cannot be redefined by the programmer citeturn0file2

---

## 🔢 Literal Expressions  
- **Literals** (constant values) in C++ include:  
  - **Character**: `'a'`, `'
'`  
  - **String**: `"Hello, world!"`  
  - **Integer**: `42`, `0x2A`, `052`  
  - **Floating-point**: `3.14`, `6.022e23` citeturn0file2

---

### 🆔 Constant Characters  
- Single characters in single quotes: `'x'`  
- **Escape sequences** (start with `\`):  
  - `
` (newline), `	` (tab), `\` (backslash), `'`, `"`, … citeturn0file2

---

### 💬 Constant Strings  
- Sequences of characters in double quotes: `"Hello
"`  
- Can include spaces, symbols, and escape sequences citeturn0file2

---

### 🔍 Character-Literal Examples  
```cpp
cout << "1. \n means: " << "[
]" << endl;
cout << "9. \\ means: " << "[\]" << endl;
```  
- Demonstrates how each escape code is rendered citeturn0file2

---

## 🔢 Representation of Numbers  

1. **Integer literals**  
   - **Decimal** (default): `123`, `-7`  
   - **Octal** (prefix `0`): `075` (equal to 61 decimal)  
   - **Hexadecimal** (prefix `0x`): `0x7B` (equal to 123 decimal) citeturn0file2

2. **Floating-point literals**  
   - Fixed notation: `3.14`, `-0.001`  
   - Scientific notation: `6.022e23`, `1.0E-3` citeturn0file2

---

### 🧮 Numeric Examples  
```cpp
cout << "012 means: " << 012 << endl;       // prints 10 (octal)
cout << "-12.451e-3 means: " << -12.451e-3; // prints -0.012451
cout << 4/3 << endl;                       // integer division → 1
cout << 4.0/3.0 << endl;                   // floating-point → 1.33333
``` citeturn0file2

---

## 🔧 Operators  
- Symbols (and combinations) that perform operations:  
  - **Arithmetic**: `+ - * / %`  
  - **Logical**: `&& || !`  
  - **Comparison**: `== != < > <= >=`  
  - **Assignment**: `= += -= *= /=`  
  - **Bitwise**: `& | ^ ~ << >>` citeturn0file2

---

## ⚖️ Properties of Operators  
- **Position**:  
  - **Prefix**: before operand (`++i`)  
  - **Infix**: between operands (`a + b`)  
  - **Postfix**: after operand (`i++`)  
- **Precedence**: defines evaluation order (`*` before `+`)  
- **Associativity**: order for same-precedence (`left` or `right`) citeturn0file2

---

## 🚪 Separators  
- Punctuation that delimits code elements:  
  - Parentheses/Brackets: `(` `)` `{` `}` `[` `]`  
  - Comma (`,`), Semicolon (`;`), Colon (`:`)  
- Some symbols (like `,`) can also act as operators depending on context citeturn0file2

---

💡 **Tip:** Keep your code clean with consistent naming, indentation, and comments for readability and maintainability! 🚀  
