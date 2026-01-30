# ASCII Art Generator with Pure Conditional Logic

A Python project that recreates ASCII art using **only for loops and if-else statements** - demonstrating algorithmic thinking and conditional programming without file I/O during execution.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [How It Works](#how-it-works)
- [Technical Details](#technical-details)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This project takes a unique approach to ASCII art generation by converting a text-based image into pure conditional logic. Instead of reading from a file during execution, the program uses nested loops with position-based if-else statements to determine each character's placement.

**Challenge**: Print a 41-line ASCII art image (120 characters per line) using only:
- `for` loops
- `if-else` statements
- No file reading inside loops

## ✨ Features

- **Pure Conditional Logic**: Zero file I/O during pattern generation
- **Educational**: Perfect for learning nested loops and conditional statements
- **Automated Generation**: Includes a generator script that analyzes source files
- **Complex Patterns**: Handles 8 different ASCII characters forming intricate designs
- **Performance Optimized**: Efficient conditional chains for fast rendering

## 🚀 Installation

### Prerequisites

- Python 3.x installed on your system

### Clone the Repository

```bash
git clone https://github.com/yourusername/ascii-art-conditional-logic.git
cd ascii-art-conditional-logic
```

### No Additional Dependencies Required!

This project uses only Python standard library.

## 💻 Usage

### Run the Pattern Generator

```bash
python vk.py
```

This will output the ASCII art pattern to your console.

## 📁 Project Structure

```
IMage project/
│
├── vk.txt                          # Source ASCII art file (41 lines × 120 chars)
├── vk.py      # Main program with conditional logic
└── README.md                       # This file
```

## 🔍 How It Works

### The Challenge

Given an ASCII art file like this:
```
------------------------------------------@@@@@@@@@@@@@@@@@@@@@
-----------------------------------@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
```

### The Solution

Convert each line into conditional statements:

```python
for i in range(1, 42):  # 41 lines
    for j in range(1, 121):  # 120 columns
        
        if i == 1:
            if j <= 42:
                print("-", end="")
            elif j <= 84:
                print("@", end="")
            # ... more conditions
        
        elif i == 2:
            if j <= 35:
                print("-", end="")
            elif j <= 93:
                print("@", end="")
            # ... more conditions
    
    print()  # New line after each row
```

### Algorithm Breakdown

1. **Outer Loop (Rows)**: Iterates through each line (i = 1 to 41)
2. **Inner Loop (Columns)**: Iterates through each character position (j = 1 to 120)
3. **Conditional Logic**: For each (i, j) position, determine which character to print
4. **Character Transitions**: Identified by analyzing consecutive characters in source file

## 🛠️ Technical Details

### Character Set Used

The ASCII art uses 8 different characters:
- `-` : Background/spacing
- `@` : Main pattern element
- `#` : Shading element
- `*` : Detail element
- `+` : Fine detail
- `=` : Gradient element
- `%` : Texture element
- `:` : Highlight element

### Performance Metrics

- **Total Lines**: 41
- **Characters per Line**: 120
- **Total Characters**: 4,920
- **Conditional Statements**: ~300+ if-elif chains
- **Execution Time**: < 0.1 seconds

### Code Generation Process

The `vk.py` script:

1. Reads the source ASCII art file
2. Analyzes each line character by character
3. Identifies character transition points
4. Generates optimized if-elif chains
5. Writes the complete program with proper formatting

```python
# Simplified generation logic
for line_num, line in enumerate(lines, 1):
    prev_char = line[0]
    start = 1
    
    for i, char in enumerate(line[1:], 2):
        if char != prev_char:
            # Generate condition for prev_char from start to i-1
            prev_char = char
            start = i
```

## 📊 Examples

### Input (vk.txt - first 3 lines):
```
------------------------------------------@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@---------------------------------
-----------------------------------@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@--------------------------
---------------------------@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@-----------------------
```

### Output (vk.py execution):
```
------------------------------------------@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@---------------------------------
-----------------------------------@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@--------------------------
---------------------------@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@-----------------------
```

✅ **Perfect Match!**

This will:
- Execute `vk.py`
- Compare output with `vk.txt` line by line
- Report any mismatches with detailed position information

## 🎓 Learning Outcomes

This project demonstrates:

1. **Nested Loop Mastery**: Understanding multi-dimensional iteration
2. **Conditional Logic**: Building complex decision trees
3. **Pattern Recognition**: Analyzing and encoding visual patterns
4. **Code Generation**: Meta-programming concepts
5. **Algorithm Optimization**: Efficient conditional chains

## 🤝 Contributing

Contributions are welcome! Here are some ways you can contribute:

- Add support for colored ASCII art
- Optimize conditional logic generation
- Create alternative encoding methods
- Add more example ASCII art files
- Improve documentation

### Steps to Contribute

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Rajvardhan Mall**

## 🌟 Acknowledgments

- Inspired by classic programming challenges
- Thanks to the Python community for excellent documentation
- ASCII art pattern design community

## 📞 Contact

Have questions or suggestions? Feel free to:
- Open an issue
- Submit a pull request
- Contact me directly(rajvardhanmall@gmail.com)

---

⭐ **Star this repository if you find it helpful!** ⭐

**Made with ❤️ and pure Python conditionals**
