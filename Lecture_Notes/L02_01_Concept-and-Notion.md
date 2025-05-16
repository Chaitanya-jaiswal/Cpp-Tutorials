# Computer Programming 1: Concepts and Notions

*Source: L02_01_Concept-and-Notion.pdf citeturn0file1*

---

## Outline

1. Basic concepts on coding/programming  
2. Programming paradigms  
3. Introduction to C++

---

## 1. Programming vs. Coding

### 1.1 Definitions

- **Coding**  
  Writing lines of code in a programming language to create software.

- **Programming**  
  A multi-phase activity that includes:
  - Planning  
  - Design (algorithm & data structures)  
  - Implementation (coding)  
  - Testing  
  - Deployment  
  - Maintenance  

> To write code effectively you start with a mental schema, draft pseudocode, then implement. citeturn0file1

### 1.2 The Process

1. **Understand the problem & context**  
2. **Design the solution** (algorithm)  
3. **Implement the solution** (code)  
4. **Verify & validate** (testing)  
5. **Deliver** (deployment)  
6. **Maintain & evolve** (updates)  

*Note: Code reuse exists—writing from scratch is not always necessary.*

---

## 2. Coding ≠ Programming

| **Coding**                                   | **Programming**                                                                          |
|----------------------------------------------|------------------------------------------------------------------------------------------|
| Converts instructions to a machine-readable form. | Includes coding **and** requirement analysis, design, testing, debugging, maintenance. |
| Requires syntax and semantics knowledge.     | Requires problem-solving, algorithmic thinking, system-level design.                     |
| Like writing a single chapter.               | Like writing an entire book.                                                             |

---

## 3. What Is a Programming Language?

- A set of **syntax** (grammar) and **semantics** (meaning) rules.  
- Enables you to:
  1. Specify an algorithm to the computer.  
  2. Communicate instructions for execution.  

---

## 4. Why So Many Languages?

- Historical evolution of needs and technology.  
- Different objectives, domains, paradigms, and performance trade-offs. citeturn0file1

---

## 5. Language Classification Criteria

1. **Domain**:  
   - General-purpose vs. domain-specific  
2. **Paradigm**:  
   - Imperative vs. declarative  
3. **Abstraction level**:  
   - High-level vs. low-level vs. machine code  
4. **Execution**:  
   - Compiled vs. interpreted vs. JIT  
5. **Typing**:  
   - Strong vs. weak; static vs. dynamic  

---

## 6. Programming Paradigms

1. **Procedural** (e.g., C, Pascal)  
   - Sequence of instructions modifying program state.  
2. **Object-Oriented** (e.g., C++, Java)  
   - Objects encapsulate data & behavior; supports inheritance, polymorphism.  
3. **Logic/Declarative** (e.g., Prolog, Haskell)  
   - Programs as sets of facts & rules; queries drive computation.  
4. **Functional** (e.g., Lisp, ML)  
   - Computation via pure functions, recursion, immutable data.  
5. **Scripting** (e.g., Python, JavaScript)  
   - Interpreted, dynamic, rapid development.  
6. **Command Language** (e.g., Bash, PowerShell)  
   - Shell scripts automate OS tasks.  
7. **Event-Driven** (e.g., JavaScript GUIs)  
   - Reacts to user or system events via callbacks.  
8. **Markup-Language** (e.g., HTML, XML)  
   - Describes document structure, not logic.  
9. **Assembly**  
   - Low-level, hardware-specific; one step above machine code.  
10. **Mathematical/Data-Science** (e.g., R, MATLAB)  
    - Optimized for numeric & statistical operations.  
11. **Natural-Language** (emerging)  
    - Uses human-readable sentences and AI/NLP for code synthesis.   citeturn0file1

> Most modern languages are **multi-paradigm**, but each has its core strengths.

---

## 7. Why C++ for This Course?

- **General-purpose**, multi-paradigm (procedural, OOP, functional).  
- **Standardized** by ISO (C++98 → C++20).  
- Teaches low-level concepts:
  - Memory management & pointers  
  - Compiler architecture & optimization  
- Builds foundations for learning other languages.  
- Widely used in systems, games, browsers, embedded, finance, etc. citeturn0file1

---

## 8. C++ Compilation & Execution Flow

1. **Write** source file: `test.cc`  
2. **Compile** to object:  
   ```bash
   g++ -c test.cc        # → test.o
   ```  
3. **Link** with libraries:  
   ```bash
   g++ test.o -o test    # → executable “test”
   ```  
4. **Run**:  
   ```bash
   ./test
   ```

---

## 9. Basic C++ Program Templates

### 9.1 Skeleton
```cpp
#include <iostream>
using namespace std;

int main() {
    return 0;
}
```

### 9.2 “Hello, World!”
```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, world!
";
    return 0;
}
```

Compile and run:
```bash
g++ hello.cc -o hello
./hello
```
