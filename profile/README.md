<p align="center">
  <img src="https://raw.githubusercontent.com/Vibe-Programming-Language/Vibe/main/assets/banner.svg" alt="Vibe" width="600">
</p>

<h1 align="center">Vibe Programming Language</h1>

<p align="center">
  <strong>A modern, expressive language that compiles to C++ — built for clarity, speed, and joy.</strong>
</p>

<p align="center">
  <a href="https://github.com/Vibe-Programming-Language/Vibe/releases"><img src="https://img.shields.io/github/v/release/Vibe-Programming-Language/Vibe?style=flat-square&color=black" alt="Release"></a>
  <a href="https://vibe-lang-docs.vercel.app"><img src="https://img.shields.io/badge/docs-live-black?style=flat-square" alt="Docs"></a>
  <img src="https://img.shields.io/badge/language-C%2B%2B17-black?style=flat-square" alt="C++17">
  <img src="https://img.shields.io/badge/platforms-Linux%20%7C%20macOS%20%7C%20Windows-black?style=flat-square" alt="Platforms">
  <a href="https://github.com/Vibe-Programming-Language/Vibe/blob/main/LICENSE"><img src="https://img.shields.io/github/license/Vibe-Programming-Language/Vibe?style=flat-square&color=black" alt="License"></a>
  <a href="https://github.com/Vibe-Programming-Language/Vibe/stargazers"><img src="https://img.shields.io/github/stars/Vibe-Programming-Language/Vibe?style=flat-square&color=black" alt="Stars"></a>
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

## Key Features

| Feature | Description |
|---------|-------------|
| **Clean Syntax** | Expressive and readable — feels like pseudocode |
| **OOP** | Classes, inheritance, interfaces, access modifiers |
| **Pattern Matching** | Powerful `match` expressions with wildcards |
| **Lambdas & Closures** | First-class functions with arrow syntax |
| **Rich Standard Library** | 50+ builtins, modules for math, IO, OS, time, JSON |
| **C++ Transpilation** | Compile to native binaries via `vibe build` |
| **Interactive REPL** | Color-coded, auto-semicolons, persistent state |
| **Error Handling** | `try`/`catch`/`finally` with `throw` |
| **Module System** | `import`/`export` for code organization |
| **Enums** | Named constants with optional values |
| **VS Code Extension** | Syntax highlighting, IntelliSense, snippets, diagnostics |

## Quick Install

```bash
git clone https://github.com/Vibe-Programming-Language/Vibe.git
cd Vibe
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make -j$(nproc)
sudo make install   # optional
```

Or download a pre-built binary from [**Releases**](https://github.com/Vibe-Programming-Language/Vibe/releases).

## 📖 Documentation

Full documentation is available at **[vibe-lang-docs.vercel.app](https://vibe-lang-docs.vercel.app)** — covering installation, language tour, standard library reference, examples, and more.

## 📂 Ecosystem

| Repository | Description |
|------------|-------------|
| [**Vibe**](https://github.com/Vibe-Programming-Language/Vibe) | Core language — lexer, parser, runtime, codegen, CLI, REPL |
| [**Vibe-Docs**](https://github.com/Vibe-Programming-Language/Vibe-Docs) | Documentation site — [vibe-lang-docs.vercel.app](https://vibe-lang-docs.vercel.app) |
| [**Vibe-Language-Extension**](https://github.com/Vibe-Programming-Language/Vibe-Language-Extension) | VS Code extension — syntax highlighting, IntelliSense, snippets |

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
  <strong>Ready to vibe?</strong> <a href="https://vibe-lang-docs.vercel.app">Read the docs</a> · <a href="https://github.com/Vibe-Programming-Language/Vibe/releases">Download now →</a>
</p>
