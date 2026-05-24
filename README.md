<div align="center">

# Scientific Calculator

**A fully-featured scientific calculator built with pure HTML, CSS, and JavaScript — no dependencies, no build tools, just one file.**

![Version](https://img.shields.io/badge/version-2.0-00ffaa?style=for-the-badge&labelColor=0a0a0f)
![Language](https://img.shields.io/badge/HTML%2FJS-Single%20File-4ac8ff?style=for-the-badge&labelColor=0a0a0f)
![License](https://img.shields.io/badge/License-MIT-ffaa00?style=for-the-badge&labelColor=0a0a0f)

</div>

---

## Overview

A scientific calculator with a cyberpunk dark-mode interface, featuring four specialized modes — Basic, Scientific, Statistics, and Physical Constants. Built entirely in vanilla HTML/CSS/JavaScript with no external dependencies.

---

## Features

### Basic Mode
- Standard arithmetic operations
- Trigonometric functions: `sin`, `cos`, `tan`
- Logarithms: `log₁₀` and natural log `ln`
- Square root, powers, absolute value, factorial, percentage
- Mathematical constants: `π` and `e`
- Full parentheses support

### Scientific Mode
- Inverse trigonometry: `sin⁻¹`, `cos⁻¹`, `tan⁻¹`
- Hyperbolic functions: `sinh`, `cosh`, `tanh`
- `log₂`, cube root, `x²`, `x³`
- Reciprocal `1/x`, sign toggle `±`, scientific notation
- **DEG / RAD toggle** for angle mode
- **Calculation history** — last 20 results, clickable to reuse

### Statistics Mode
Enter a comma-separated list of numbers and compute:

| Function | Description |
|----------|-------------|
| Mean | Arithmetic average |
| Median | Middle value |
| Mode | Most frequent value |
| Std Dev | Population standard deviation |
| Variance | Population variance |
| Sum | Total |
| Min / Max | Bounds |
| Range | Max − Min |
| Count | Number of entries |
| Geometric Mean | nth root of product |
| Harmonic Mean | Reciprocal average |

### Constants Mode
One-click insertion of physical and mathematical constants:

| Constant | Symbol | Value |
|----------|--------|-------|
| Pi | π | 3.14159265358979... |
| Euler's Number | e | 2.71828182845904... |
| Golden Ratio | φ | 1.61803398874989... |
| Speed of Light | c | 299,792,458 m/s |
| Gravitational Constant | G | 6.674 × 10⁻¹¹ N·m²/kg² |
| Planck's Constant | h | 6.626 × 10⁻³⁴ J·s |
| Boltzmann Constant | k_B | 1.38 × 10⁻²³ J/K |
| Avogadro's Number | N_A | 6.022 × 10²³ mol⁻¹ |
| Ideal Gas Constant | R | 8.314 J/mol·K |
| Standard Gravity | g | 9.8 m/s² |
| Elementary Charge | q | 1.602 × 10⁻¹⁹ C |
| Electron Mass | mₑ | 9.109 × 10⁻³¹ kg |
| Proton Mass | mₚ | 1.673 × 10⁻²⁷ kg |
| Permittivity of Free Space | ε₀ | 8.85 × 10⁻¹² F/m |

---

## Getting Started

No installation required. Download `calculator.html` and open it in any modern browser.

```bash
# Clone the repository
git clone https://github.com/your-username/scientific-calculator.git

# Open directly
open calculator.html
```

Or serve locally:

```bash
# Python
python -m http.server 8080

# Node.js
npx serve .
```

---

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `0` – `9` | Number input |
| `+` `-` `*` `/` | Arithmetic operators |
| `.` | Decimal point |
| `^` | Exponentiation |
| `(` `)` | Parentheses |
| `Enter` or `=` | Evaluate expression |
| `Backspace` | Delete last character |
| `Escape` | Clear all |

---

## How It Works

User input is stored as a string expression. On evaluation, trig functions are wrapped in angle-aware helpers that respect the current DEG/RAD mode before passing to `Math`. The expression is then executed in a sandboxed `Function()` scope with only `Math` and the custom trig helpers exposed — no `eval` on the global scope.

The statistics engine is implemented from scratch in plain JavaScript, covering all eleven functions without any external library.

---

## Project Structure

```
scientific-calculator/
├── calculator.html    # Complete application — single self-contained file
└── README.md
```

---

## Roadmap

- [ ] Graph plotter for functions
- [ ] Matrix operations mode
- [ ] Unit converter
- [ ] PWA support for offline use
- [ ] Export calculation history

---

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add your feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## License

MIT License. See [LICENSE](LICENSE) for details.
