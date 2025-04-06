# 23115031_compiler-design

# Sum of Cubes Compiler

This C++ project implements a mini-compiler that takes two positive integers as input and computes the **sum of cubes** of the numbers. It includes all typical compiler phases:

- **Lexical Analysis** (Lexer)
- **Syntax Analysis** (Parser)
- **Semantic Analysis**
- **Intermediate Representation (IR)**
- **Code Generation**
- **Execution**

## 📥 Input Format

The program expects **two space-separated integers** as input, for example:

```
2 3
```

## 🧮 Custom Instruction Design

We define a custom intermediate instruction to compute the sum of cubes as:

```
CUBEADD a, b -> result
```
Which expands into:
```
t1 = a * a * a
t2 = b * b * b
result = t1 + t2
```

## ▶️ How to Run
🧰 1. Installing MSYS2 (if not done already):
```
If you haven't installed it:

Download from: https://www.msys2.org
```

Follow the installation guide on the website.
⚙️ 2. Update the package database and core system packages
Run these commands in the MSYS2 terminal (use MSYS2 MINGW64 or UCRT64 depending on your need):
```bash
pacman -Syu
```
💡 3. Installing development tools (for C/C++ for example):
```bash
pacman -S make gcc flex bison
```
📝 4. Compiling and Running a C++ Program
Assume you have a file main.cpp. From the terminal:
```bash
g++ main.cpp lexer.cpp parser.cpp semantic.cpp ir.cpp codegen.cpp -o sum_of_cubes_compiler_final
```
```bash
./sum_of_cubes_compiler_final
```

📌 5. **Example Execution**:


Enter two integers: 2 3
Tokens: [2, 3]
Three-Address Code:
```
t1 = 2 * 2 * 2
t2 = 3 * 3 * 3
t3 = t1 + t2
```
Assembly Code:
```
LOAD R1, 2
MUL R1, R1, R1
MUL R1, R1, 2
LOAD R2, 3
MUL R2, R2, R2
MUL R2, R2, 3
ADD R3, R1, R2
```
Result: 35


## 📸 Output Screenshot

See `Screenshot 2025-04-06 190658.png` in the project folder.

## 🔗 GitHub link
Gi

