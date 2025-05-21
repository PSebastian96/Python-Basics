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
| **Structural Matching**| `match`, `case` (introduced in Python 3.10)                                  |

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
