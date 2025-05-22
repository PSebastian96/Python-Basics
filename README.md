# 🐍 Python Reserved Keywords

These are words reserved by the Python language. They **cannot** be used as variable names, function names, or identifiers.

## 📋 Summary Table of Reserved Keywords

| **Category**           | **Keywords**                                                                 |
|------------------------|------------------------------------------------------------------------------|
| **Control Flow**       | `if`, `else`, `elif`, `while`, `for`, `break`, `continue`, `pass`            |
| **Boolean Logic**      | `True`, `False`, `not`, `and`, `or`                                          |
| **Functions**          | `def`, `return`, `lambda`, `yield`, `nonlocal`                               |
| **Exception Handling** | `try`, `except`, `finally`, `raise`, `assert`                                |
| **Classes & OOP**      | `class`, `self`, `super`, `is`                                               |
| **Variable Scope**     | `global`, `nonlocal`, `del`                                                  |
| **Imports/Modules**    | `import`, `from`, `as`                                                       |
| **Data Definitions**   | `None`, `in`                                                                 |
| **Async & Await**      | `async`, `await`                                                             |
| **Context Management** | `with`                                                                       |
| **Structural Matching**| `match`, `case`                                                              |

# 🎯 Python CLI Workflow for Projects

## 1. 📁 Create project directory  
✅ Always start your project in a clean, new folder.

> mkdir my-awesome-python-project

> cd my-awesome-python-project

## 2. 🧱 Create a virtual environment
✅ Keeps your project’s dependencies isolated.

> `python -m venv venv`

> `source venv/bin/activate        # macOS/Linux`

> `venv\Scripts\activate           # Windows`

## 3. 📄 Create your entry point (main.py)
✅ This is your app’s main file.

> `touch main.py`

## 4. 📚 Add Python files
Example: Creating a user model file.

> `touch app/models/user.py`

## 5. 📦 Install and manage dependencies
✅ Use pip and requirements.txt for dependencies.

Install a package:
> pip install `packagename`

Freeze dependencies:
> `pip freeze > requirements.txt`

Install from file:
> `pip install -r requirements.txt`

## 6. 🧪 Run your app
✅ Run your entry file directly.

> `python main.py`

## 7. 🚀 Build/Package your app (optional)
For CLI tools, use `setuptools` or `pyinstaller` to create an executable.

> `pip install pyinstaller`

> `pyinstaller --onefile main.py`

✅ This creates a single executable in the dist/ folder:
`./dist/main (Linux/macOS)` or `main.exe (Windows)`

## 8. 🧼 Clean structure sample

<img width="173" alt="image" src="https://github.com/user-attachments/assets/1294cb7e-9e3c-42c7-9ab3-2f3fe10254ee" />

# 💡 What does `if __name__ == "__main__"`: mean?

It's a way to tell Python:

> Only run this part of the code if you're running this file directly, not if it's imported.

> Python automatically creates a special variable called __name__ in every Python file.

> This variable tells Python how the file is being used.

## 📦 Example use case

📄 math_tools.py
``` 
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

# Demo or test code
if __name__ == "__main__":
    print(add(3, 5))        # 8
    print(subtract(10, 4))  # 6
```

📄 main_program.py
``` 
import math_tools

result = math_tools.add(100, 200)
print(result)

```

> When you run main_program.py, it does not run the test code in math_tools.py.

## 🔚 Summary
`__name__` is a special variable set by Python.

When a file is run directly, `__name__ is "__main__"` -> Use to control what runs when :

```
if __name__ == "__main__":
    # run test/demo code here
 ```

# 🗂️ Python Standard Library - Commonly Used Modules

## 🔤 Text and String Handling

| Module      | Purpose                                        |
|-------------|------------------------------------------------|
| `re`        | Regular expressions (searching/parsing text)   |
| `string`    | String constants and utilities                 |
| `textwrap`  | Wrap and format text output                    |
| `difflib`   | Compare sequences (diffs)                      |

---

## 🗃️ File and Directory Access

| Module      | Purpose                                        |
|-------------|------------------------------------------------|
| `os`        | Interact with the operating system, paths      |
| `os.path`   | Path operations                                |
| `shutil`    | High-level file operations (copy, move)        |
| `glob`      | Pattern matching on file names (`*.txt`)       |
| `pathlib`   | Modern object-oriented file path handling      |
| `tempfile`  | Create temporary files and directories         |

---

## 📤 Input/Output (I/O)

| Module      | Purpose                                        |
|-------------|------------------------------------------------|
| `sys`       | System-specific functions and variables        |
| `io`        | Tools for stream handling                      |
| `argparse`  | Command-line argument parsing                  |
| `logging`   | Built-in logging support                       |

---

## 📬 Networking and Internet

| Module              | Purpose                                  |
|---------------------|------------------------------------------|
| `http.server`       | Simple HTTP server                       |
| `socket`            | Low-level network interface              |
| `urllib`            | Fetching URLs (HTTP, FTP)                |
| `json`              | Reading/writing JSON                     |
| `xml.etree.ElementTree` | Simple XML parsing                  |

---

## 🧮 Data Handling and Math

| Module      | Purpose                                        |
|-------------|------------------------------------------------|
| `math`      | Basic math functions (sin, sqrt, etc.)         |
| `statistics`| Mean, median, mode, etc.                       |
| `decimal`   | Decimal floating point                         |
| `fractions` | Fractional numbers                             |
| `random`    | Pseudo-random numbers                          |

---

## 📊 Data Structures

| Module       | Purpose                                        |
|--------------|------------------------------------------------|
| `collections`| Extra data types (`Counter`, `defaultdict`)    |
| `heapq`      | Heap queue algorithms (priority queues)        |
| `array`      | Space-efficient numeric arrays                 |

---

## 🧪 Testing and Debugging

| Module      | Purpose                                        |
|-------------|------------------------------------------------|
| `unittest`  | Unit testing framework                         |
| `doctest`   | Test code snippets in docstrings               |
| `pdb`       | Python debugger                                |
| `traceback` | Extract, format, and print stack traces        |

---

## 🕓 Date and Time

| Module      | Purpose                                        |
|-------------|------------------------------------------------|
| `datetime`  | Date and time manipulation                     |
| `time`      | Time access and conversions                    |
| `calendar`  | Calendar-based utilities                       |

---

## 🔐 Security and Cryptography

| Module      | Purpose                                        |
|-------------|------------------------------------------------|
| `hashlib`   | Secure hashes (SHA, MD5, etc.)                 |
| `hmac`      | Keyed-hash message authentication              |
| `secrets`   | Cryptographically secure tokens                |

---

## 🧰 Utilities and Tools

| Module       | Purpose                                        |
|--------------|------------------------------------------------|
| `itertools`  | Fast looping tools                             |
| `functools`  | Higher-order functions like `lru_cache`        |
| `operator`   | Functional tools for operators (`itemgetter`)  |
| `enum`       | Enumeration support                            |
| `typing`     | Type hinting and annotations                   |
| `dataclasses`| Automatically create class boilerplate         |

---

## 🗃️ Serialization / Persistence

| Module      | Purpose                                        |
|-------------|------------------------------------------------|
| `json`      | Encode/decode JSON                             |
| `pickle`    | Serialize Python objects                       |
| `shelve`    | Simple persistent storage of objects           |
| `csv`       | Read/write CSV files                           |

---

## 📌 Tip

You can explore all standard modules with:

```
python help('modules')
```

