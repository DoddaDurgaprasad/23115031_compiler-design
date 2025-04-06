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

1. **Compile the code using g++**:


```bash
g++ main.cpp lexer.cpp parser.cpp semantic.cpp ir.cpp codegen.cpp -o sum_of_cubes_compiler_final
```

2. **Run the compiler**:

```bash
./sum_of_cubes_compiler_final
```

3. **Example Execution**:

```
Enter two integers: 2 3
Tokens: [2, 3]
Three-Address Code:
t1 = 2 * 2 * 2
t2 = 3 * 3 * 3
t3 = t1 + t2
Assembly Code:
LOAD R1, 2
MUL R1, R1, R1
MUL R1, R1, 2
LOAD R2, 3
MUL R2, R2, R2
MUL R2, R2, 3
ADD R3, R1, R2
Result: 35
```

## 📸 Output Screenshot

See `Screenshot 2025-04-06 190658.png` in the project folder.

## 🔗 GitHub (mock)

[GitHub Repository]()

