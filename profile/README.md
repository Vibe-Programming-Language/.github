<p align="center">
  <img src="https://raw.githubusercontent.com/Vibe-Programming-Language/Vibe/main/assets/banner.svg" alt="Vibe" width="600" onerror="this.style.display='none'">
</p>

<h1 align="center">Vibe Programming Language</h1>

<p align="center">
  <strong>A modern, expressive language that compiles to C++ — built for clarity, speed, and joy.</strong>
</p>

<p align="center">
  <a href="https://github.com/Vibe-Programming-Language/Vibe/releases"><img src="https://img.shields.io/github/v/release/Vibe-Programming-Language/Vibe?style=flat-square&color=blue" alt="Release"></a>
  <img src="https://img.shields.io/badge/language-C%2B%2B17-orange?style=flat-square" alt="C++17">
  <img src="https://img.shields.io/badge/platforms-Linux%20%7C%20macOS%20%7C%20Windows-green?style=flat-square" alt="Platforms">
  <a href="https://github.com/Vibe-Programming-Language/Vibe/blob/main/LICENSE"><img src="https://img.shields.io/github/license/Vibe-Programming-Language/Vibe?style=flat-square&color=purple" alt="License"></a>
  <a href="https://github.com/Vibe-Programming-Language/Vibe/stargazers"><img src="https://img.shields.io/github/stars/Vibe-Programming-Language/Vibe?style=flat-square" alt="Stars"></a>
</p>

---

## What is Vibe?

**Vibe** is a modern programming language designed to be expressive, readable, and powerful. It features clean syntax inspired by the best of Python, JavaScript, and Rust — while compiling down to **native C++ binaries** for production performance.

Whether you're prototyping in the interactive REPL or building production software, Vibe gets out of your way and lets you focus on what matters: writing great code.

```vibe
// A taste of Vibe
fn greet(name) {
  return "Hello, " + name + "!";
}

var people = ["Alice", "Bob", "Charlie"];
for person in people {
  print(greet(person));
}

// Functional programming
var squares = [1, 2, 3, 4, 5].map((x) => x ** 2);
print(squares);  // [1, 4, 9, 16, 25]

// Pattern matching
match status {
  200 => print("OK"),
  404 => print("Not Found"),
  _   => print("Unknown"),
}
```

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| 🧩 **Clean Syntax** | Expressive and readable — feels like pseudocode |
| 🏗️ **OOP** | Classes, inheritance, interfaces, access modifiers |
| 🎯 **Pattern Matching** | Powerful `match` expressions with wildcards |
| ⚡ **Lambdas & Closures** | First-class functions with arrow syntax |
| 📦 **Rich Standard Library** | 50+ builtins, modules for math, IO, OS, time, JSON |
| 🔧 **C++ Transpilation** | Compile to native binaries via `vibe build` |
| 💻 **Interactive REPL** | Color-coded, auto-semicolons, persistent state |
| 🛡️ **Error Handling** | `try`/`catch`/`finally` with `throw` |
| 📁 **Module System** | `import`/`export` for code organization |
| 🔢 **Enums** | Named constants with optional values |
| 🧪 **Dynamic Typing** | With optional type annotations |
| 🎨 **VS Code Extension** | Syntax highlighting and file icon theme |

## 🚀 Quick Install

### Download a Pre-built Binary

Head to the [**Releases**](https://github.com/Vibe-Programming-Language/Vibe/releases) page and download the latest binary for your platform:

| Platform | Download |
|----------|----------|
| 🐧 Linux (x86_64) | [`vibe-linux-x86_64.tar.gz`](https://github.com/Vibe-Programming-Language/Vibe/releases/latest) |
| 🪟 Windows (x86_64) | [`vibe-windows-x86_64.zip`](https://github.com/Vibe-Programming-Language/Vibe/releases/latest) |
| 📦 Source Code | [`Source code (zip)`](https://github.com/Vibe-Programming-Language/Vibe/releases/latest) |

### Build from Source

```bash
git clone https://github.com/Vibe-Programming-Language/Vibe.git
cd Vibe
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make -j$(nproc)
sudo make install   # optional
```

### Verify

```bash
vibe version
# Vibe 1.0.0
```

## 📖 Language Overview

### Variables & Types

```vibe
var name = "Vibe";       // mutable variable
let count = 42;          // mutable (alias for var)
const PI = 3.14159;      // immutable constant

// Types: int, float, str, bool, null, list, map, function
var items = [1, "two", true, null];
var config = {"host": "localhost", "port": 8080};
```

### Functions & Lambdas

```vibe
fn fibonacci(n) {
  if n <= 1 { return n; }
  return fibonacci(n - 1) + fibonacci(n - 2);
}

// Lambdas with arrow syntax
var double = (x) => x * 2;
var nums = [1, 2, 3].map((x) => x ** 2);  // [1, 4, 9]

// Closures
fn counter() {
  var n = 0;
  return () => { n = n + 1; return n; };
}
```

### Classes & Inheritance

```vibe
class Animal {
  var name = "";
  var sound = "";

  init(name, sound) {
    self.name = name;
    self.sound = sound;
  }

  fn speak() {
    print(self.name + " says " + self.sound);
  }
}

class Dog extends Animal {
  init(name) { super(name, "Woof!"); }
}

Dog("Rex").speak();  // Rex says Woof!
```

### Collections & Functional Programming

```vibe
var numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

// Chain functional operations
var result = numbers
  .filter((x) => x % 2 == 0)
  .map((x) => x ** 2);
// [4, 16, 36, 64, 100]

var sum = numbers.reduce((a, b) => a + b, 0);  // 55

// List methods: map, filter, reduce, find, some, every, flat, sort, reverse...
// String methods: upper, lower, trim, split, contains, replace, padStart...
```

### Error Handling

```vibe
try {
  var data = io.readFile("config.json");
} catch e {
  print("Error: " + e);
} finally {
  print("Cleanup done");
}
```

### Modules

```vibe
import math;
import io;
import os;
import time;

print(math.sqrt(16));      // 4
print(math.PI);            // 3.14159...
print(os.platform());     // "linux"

io.writeFile("out.txt", "Hello!");
```

## 📚 Standard Library

### Built-in Functions (always available)

`print` · `input` · `len` · `str` · `int` · `float` · `type` · `range` · `abs` · `min` · `max` · `sum` · `sorted` · `reversed` · `zip` · `enumerate` · `flatten` · `unique` · `map` · `reduce` · `join` · `keys` · `values` · `chr` · `ord` · `format` · `assert` · `clock` · `timestamp` · `random` · `hash` · `toJSON` · `exit`

### Modules

| Module | What's Inside |
|--------|---------------|
| **math** | `sqrt`, `pow`, `sin`, `cos`, `tan`, `log`, `floor`, `ceil`, `round`, `random`, `factorial`, `isPrime`, `gcd`, `lcm`, `PI`, `E` |
| **io** | `readFile`, `writeFile`, `appendFile`, `readLines`, `exists` |
| **os** | `exec`, `env`, `platform`, `cwd`, `sleep` |
| **time** | `now`, `millis`, `sleep`, `measure` |
| **json** | `stringify` |
| **string** | `ascii_letters`, `digits`, `repeat`, `format` |
| **collections** | `Stack`, `Queue` data structures |

## 🛠️ CLI Commands

```
vibe <file.vibe>      Run a source file
vibe run <file>       Run (explicit)
vibe build <file>     Transpile to C++ → compile to native binary
vibe check <file>     Syntax check without running
vibe repl             Start the interactive REPL
vibe version          Show version
vibe help             Show help
```

## 💻 Interactive REPL

```
$ vibe repl

  ╦  ╦╦╔╗ ╔═╗
  ╚╗╔╝║╠╩╗║╣
   ╚╝ ╩╚═╝╚═╝  v1.0.0

  Welcome to the Vibe REPL!
  Type .help for commands or start typing code.

vibe 1 ❯ let x = 42
vibe 2 ❯ x ** 2
1764
vibe 3 ❯ [1,2,3].map((n) => n * 10)
[10, 20, 30]
```

**REPL features:** color-coded output by type · auto-semicolons · multi-line with brace matching · `.help` / `.clear` / `.reset` / `.exit` commands · persistent state

## 🔧 Compile to Native

```bash
vibe build myapp.vibe
# Creates: myapp.cpp + myapp (native executable)
./myapp
```

Vibe transpiles your code into idiomatic C++ and compiles it with `g++`/`clang++` for maximum performance.

## 🧩 VS Code Extension

Get syntax highlighting and file icons for `.vibe` files in Visual Studio Code — available in the [vibe-vscode](https://github.com/Vibe-Programming-Language) extension.

## 📂 Repository Structure

| Repository | Description |
|------------|-------------|
| [**Vibe**](https://github.com/Vibe-Programming-Language/Vibe) | Core language — lexer, parser, runtime, codegen, CLI, REPL |

## 🤝 Contributing

We welcome contributions! Here's how:

1. **Fork** the [Vibe repo](https://github.com/Vibe-Programming-Language/Vibe)
2. Create a feature branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m "Add my feature"`
4. Push and open a **Pull Request**

## 📄 License

Vibe is open source under the [MIT License](https://github.com/Vibe-Programming-Language/Vibe/blob/main/LICENSE).

---

<p align="center">
  <strong>Ready to vibe?</strong> <a href="https://github.com/Vibe-Programming-Language/Vibe/releases">Download now →</a>
</p>
