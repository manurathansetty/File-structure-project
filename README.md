# File Structures Project (C++)

A console-based fast-food ordering system in C++ that demonstrates flat-file storage techniques — built for a File Structures course.

![C++](https://img.shields.io/badge/C%2B%2B-00599C?logo=cplusplus&logoColor=white)

## What it is

A college File Structures course project exploring how data can be persisted and retrieved from plain text files without a database. The main program ("Peter's Jr. Fast Food") is a command-line ordering system where everything — customer accounts and order history — lives in pipe-delimited text files that are searched sequentially and appended to using `fstream`.

## Features

- **Sign-up and login** — customer records (`username|password|phone|address|`) are appended to `Customers.txt`; login validates credentials with a sequential scan and `strtok` field parsing
- **Menu ordering** — pizzas, burgers, sandwiches, rolls, and biryani, with flavour, size, and quantity selection
- **Bill generation** — computes the total and prints an order summary
- **Order persistence** — each order (`quantity|total|item|`) is appended to `Orders.txt`
- **Previous-order lookup** — retrieves a returning customer's past orders by scanning the orders file

## File-structure concepts used

- Delimited variable-length records in sequential text files
- Append-only writes (`ios::app`) and sequential search for retrieval
- Field tokenization with `strtok` on a `|` delimiter

## Repository layout

```
Final FS project/
├── Check1.cpp.txt        # Main program source (rename to .cpp to compile)
├── Check1.exe            # Pre-built Windows executable
├── Customers.txt         # Customer records data file
├── Orders.txt            # Order records data file
└── FS/                   # Supplementary course material
    └── FS/
        ├── newTell.cpp           # Indexed-file records demo (Turbo C++ style)
        └── FS--- final report .pdf
```

## Build and run

The code uses Windows-specific headers (`conio.h`, `process.h`) and `itoa`, so it targets Windows compilers (e.g. MinGW/Dev-C++):

```bash
# Rename the source and compile with MinGW
copy "Check1.cpp.txt" Check1.cpp
g++ Check1.cpp -o Check1.exe
Check1.exe
```

Run it from the `Final FS project` directory so the program can find `Customers.txt` and `Orders.txt`. A pre-built `Check1.exe` is also included.

---

Built by [Manu Rathan Setty](https://manurathansetty.github.io)
