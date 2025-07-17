# 🔤 clsString – A Comprehensive C++ String Manipulation Library

`clsString` is a powerful and feature-rich C++ utility class that provides extensive string manipulation capabilities. This library offers both static methods for one-time operations and instance methods for object-oriented string handling, making it perfect for text processing, data parsing, and string transformations in C++ applications.

---

## 📦 Features

* 📏 **String Length Operations** - Get string length with multiple approaches
* 🔠 **Case Manipulation** - Convert to uppercase, lowercase, or invert case
* 📊 **Character Counting** - Count specific characters, vowels, letters by type
* ✂️ **String Splitting** - Split strings by custom delimiters
* 🧹 **Trimming Operations** - Remove leading/trailing whitespace
* 🔗 **String Joining** - Join string arrays and vectors with delimiters
* 🔄 **Word Reversal** - Reverse word order in sentences
* 🔍 **Search & Replace** - Replace words with case-sensitive options
* 🧽 **Punctuation Removal** - Clean strings from punctuation marks
* 🎯 **Object-Oriented Design** - Both static and instance methods available

---

## 🚀 Quick Start

### Basic Usage

```cpp
#include "clsString.h"
#include <iostream>

int main() {
    // Using static methods
    std::string text = "Hello World Programming";
    std::cout << "Length: " << clsString::Length(text) << std::endl;
    std::cout << "Word Count: " << clsString::CountWords(text) << std::endl;
    std::cout << "Uppercase: " << clsString::UpperAllString(text) << std::endl;
    
    // Using instance methods
    clsString myString("hello world");
    myString.UpperFirstLetterOfEachWord();
    std::cout << "Result: " << myString.GetValue() << std::endl;
    
    return 0;
}
```

### Advanced Example

```cpp
#include "clsString.h"
#include <iostream>
#include <vector>

int main() {
    clsString processor("  Hello, World! How are you?  ");
    
    // Chain operations
    processor.Trim();
    processor.RemovePunctuations();
    processor.LowerAllString();
    
    // Split and analyze
    std::vector<std::string> words = processor.Split(" ");
    std::cout << "Words found: " << words.size() << std::endl;
    
    // Count vowels
    std::cout << "Vowels: " << processor.CountVowels() << std::endl;
    
    return 0;
}
```

---

## 🔧 Core Methods

### 📏 Length Operations

| Method | Description |
|--------|-------------|
| `Length(string)` | Returns the length of a string (static) |
| `Length()` | Returns the length of instance string |

### 🔠 Case Manipulation

| Method | Description |
|--------|-------------|
| `UpperFirstLetterOfEachWord(string)` | Capitalizes first letter of each word |
| `LowerFirstLetterOfEachWord(string)` | Lowercases first letter of each word |
| `UpperAllString(string)` | Converts entire string to uppercase |
| `LowerAllString(string)` | Converts entire string to lowercase |
| `InvertAllStringLetterCase(string)` | Inverts case of all characters |

### 📊 Counting Operations

| Method | Description |
|--------|-------------|
| `CountWords(string, delimiter)` | Counts words in string with custom delimiter |
| `CountLetters(string, type)` | Counts letters by type (Small/Capital/All) |
| `CountCapitalLetters(string)` | Counts uppercase letters |
| `CountSmallLetters(string)` | Counts lowercase letters |
| `CountSpecificLetter(string, char, matchCase)` | Counts specific character occurrences |
| `CountVowels(string)` | Counts vowel characters (a, e, i, o, u) |

### ✂️ String Manipulation

| Method | Description |
|--------|-------------|
| `Split(string, delimiter)` | Splits string into vector by delimiter |
| `TrimLeft(string)` | Removes leading whitespace |
| `TrimRight(string)` | Removes trailing whitespace |
| `Trim(string)` | Removes leading and trailing whitespace |
| `JoinString(vector, delimiter)` | Joins string vector with delimiter |
| `ReverseWordInString(string)` | Reverses word order in sentence |
| `ReplaceWord(string, find, replace, matchCase)` | Replaces words with case options |
| `RemovePunctuations(string)` | Removes punctuation characters |

### 🏷️ Utility Methods

| Method | Description |
|--------|-------------|
| `SetValue(string)` | Sets the instance string value |
| `GetValue()` | Gets the instance string value |
| `Value` | Property for getting/setting string value |
| `IsVowel(char)` | Checks if character is a vowel |

---

## 🎯 Enums

### `enWhatToCount`

```cpp
enum enWhatToCount {
    SmallLetters = 0,
    CapitalLetters = 1,
    All = 2
};
```

Used for specifying what type of letters to count in `CountLetters()` method.

---

## 💡 Usage Examples

### Text Processing Pipeline

```cpp
clsString processor("  HELLO, world! This is a TEST.  ");

// Clean and normalize
processor.Trim();
processor.RemovePunctuations();
processor.LowerAllString();
processor.UpperFirstLetterOfEachWord();

std::cout << processor.GetValue(); // "Hello World This Is A Test"
```

### Word Analysis

```cpp
std::string text = "Programming is fun and challenging";
clsString analyzer(text);

std::cout << "Total characters: " << analyzer.Length() << std::endl;
std::cout << "Word count: " << analyzer.CountWords() << std::endl;
std::cout << "Vowels: " << analyzer.CountVowels() << std::endl;
std::cout << "Capital letters: " << analyzer.CountCpaitalLetters() << std::endl;
```

### String Transformation

```cpp
clsString transformer("apple,banana,orange");
std::vector<std::string> fruits = transformer.Split(",");

// Process each fruit
for (auto& fruit : fruits) {
    clsString fruitProcessor(fruit);
    fruitProcessor.UpperFirstLetterOfEachWord();
    std::cout << fruitProcessor.GetValue() << " ";
}
```

---

## 📁 File Structure

```
📁 clsString_Library/
├── clsString.h       → Main header file with the string class
├── main.cpp          → Example usage and demonstration
├── README.md         → Project documentation

```

---

## ⚙️ Requirements

- **C++ Standard**: C++11 or later
- **Dependencies**: Standard C++ library (`<iostream>`, `<vector>`, `<algorithm>`, `<string>`)
- **Platform**: Cross-platform (Windows, Linux, macOS)

---

## 🔧 Installation

### Method 1: Include Header

```cpp
#include "clsString.h"
```

### Method 2: Clone Repository

```bash
git clone https://github.com/AbdelhamidSherif/clsString-Library.git
cd clsString-Library
```

### Method 3: Download Single File

Download `clsString.h` and include it in your project.

---

## 📚 Related Projects

### clsUtil
A comprehensive C++ utility library for randomization, encryption, and array operations.

🔗 [clsUtil GitHub Repository](https://github.com/AbdelhamidSherif/Project_Utility_Library)

### clsDate
A powerful C++ date manipulation library with arithmetic operations and formatting.

🔗 [clsDate GitHub Repository](https://github.com/AbdelhamidSherif/clsDate)

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 👨‍💻 Author

**Doctor Dev**  
📍 Egypt  
🧠 Software Engineer | C++ String Processing Specialist  
📧 [My Email](mailto:9abdelhamid080@gmail.com)  
🔗 [GitHub Profile](https://github.com/AbdelhamidSherif)

---

## ⭐ Show Your Support

If this library helped you, please consider giving it a star ⭐ on GitHub!

---

## 🔗 GitHub Repository

**Repository**: [clsString-Library](https://github.com/AbdelhamidSherif/clsString-Library)

---

*This C++ string library is designed for developers who need robust, efficient, and easy-to-use string manipulation capabilities. Perfect for text processing applications, data parsing, and string transformations.*
