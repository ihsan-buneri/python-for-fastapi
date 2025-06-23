## What is a Module in Python?

A module in Python is a file that contains Python code (functions, classes, variables, or even runnable code) and is used to organize and reuse code efficiently.

- A module is simply a .py file that can be imported and used in other Python programs.

- Modules help keep the code modular, readable, and maintainable.

- Python has built-in modules (like math, random, os) and also allows users to create custom modules.

### Types of Modules in Python

1. **Built-in Modules (Standard Library)**
   Pre-installed modules in Python.
   Example: math, random, os, sys

2. **User-Defined Modules (Custom Modules)**
   Any Python file (.py) you create can be used as a module.

3. **External Modules (Third-party Libraries)**
   Installed via pip (pip install module_name).
   Example: numpy, pandas, requests
   Example usage:

### Basic Import Syntax

- import module_name
  Brings in the module namespace.

```code
import math_utils

result = math_utils.add(2, 3)
```

- import module_name as alias
  Use an alias for brevity or to avoid name clashes.

```code
import math_utils as mu

result = mu.add(2, 3)
```

- Imports specific attributes into your local namespace.

```code
from module_name import name1, name2
from math_utils import add, subtract
result = add(5, 6)

```

- Imports all public names.

```code
from module_name import *
from math_utils import *
result = add(1, 2)
```

### Packages: Organizing Modules into Folders

A package is a directory with an \_ \_init\_\_.py file (which can be empty) that tells Python to treat it as a package.

```text
project/
└── utils/
├── _ _init__.py
├── math_utils.py
└── string_utils.py
```

You can import from a package:

```code
from utils.math_utils import add
from utils import string_utils
```

Example Project Structure:

```text
myproject/
├── app/
│   ├── __init__.py
│   ├── main.py          # FastAPI entrypoint
│   ├── routers/
│   │   ├── __init__.py
│   │   └── users.py
│   ├── models/
│   │   ├── __init__.py
│   │   └── user.py
│   └── utils/
│       ├── __init__.py
│       └── hash.py
└── tests/
    ├── __init__.py
    └── test_users.py
```
