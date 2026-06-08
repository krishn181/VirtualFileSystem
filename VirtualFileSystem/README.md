# Virtual File System (VFS)

A command-line based Virtual File System built using C++.  
This project simulates basic operating system file system functionalities such as creating files, creating directories, reading files, writing content, and listing directory contents.

The project is designed using Object-Oriented Programming concepts like inheritance, polymorphism, abstraction, and encapsulation.

---

# Features

- Create directories
- Create files
- List directory contents
- Write data into files
- Read file content
- Command-line interface
- Object-Oriented Design
- Smart pointer usage
- Modular architecture
- Command parser and command handler

---

# Technologies Used

- C++
- C++17
- STL (Standard Template Library)
- Smart Pointers (`std::shared_ptr`)
- CMake

---

# OOP Concepts Used

## Encapsulation
Each class manages its own data and behavior internally.

## Inheritance
`File` and `Directory` classes inherit from the base class `FileSystemComponent`.

## Polymorphism
Virtual functions are used to achieve runtime polymorphism.

## Abstraction
The internal implementation details are hidden behind interfaces.

---

# Project Structure

```bash
VirtualFileSystem/
│
├── include/
│   ├── FileSystemComponent.h
│   ├── File.h
│   ├── Directory.h
│   ├── FileSystem.h
│   ├── ParsedCommand.h
│   ├── CommandParser.h
│   └── CommandHandler.h
│
├── src/
│   ├── main.cpp
│   ├── FileSystemComponent.cpp
│   ├── File.cpp
│   ├── Directory.cpp
│   ├── FileSystem.cpp
│   ├── CommandParser.cpp
│   └── CommandHandler.cpp
│
├── CMakeLists.txt
│
└── README.md
```

---

# Class Overview

## FileSystemComponent

Abstract base class for all file system entities.

### Responsibilities
- Store common attributes
- Provide virtual methods
- Enable polymorphism

---

## File

Represents a file in the virtual file system.

### Responsibilities
- Store file content
- Read content
- Write content

---

## Directory

Represents a directory that can contain files and subdirectories.

### Responsibilities
- Store child components
- Add files/directories
- Display directory contents

---

## FileSystem

Acts as the main controller of the virtual file system.

### Responsibilities
- Manage root directory
- Handle file operations
- Handle directory operations

---

## CommandParser

Parses user input into command objects.

### Responsibilities
- Split command name
- Extract arguments

---

## CommandHandler

Executes parsed commands on the file system.

### Responsibilities
- Handle user commands
- Call appropriate file system methods

---

# Supported Commands

## Create Directory

```bash
mkdir <directory_name>
```

Example:

```bash
mkdir docs
```

---

## Create File

```bash
touch <file_name>
```

Example:

```bash
touch notes.txt
```

---

## List Directory Contents

```bash
ls
```

---

## Write Content to File

```bash
write <file_name> <content>
```

Example:

```bash
write notes.txt Hello Virtual File System
```

---

## Read File Content

```bash
cat <file_name>
```

Example:

```bash
cat notes.txt
```

---

## Exit Application

```bash
exit
```

---

# Example Execution

```bash
vfs> mkdir docs
Directory created

vfs> touch notes.txt
File created

vfs> write notes.txt Hello World
Written successfully

vfs> cat notes.txt
Hello World

vfs> ls
[DIR] docs
[FILE] notes.txt

vfs> exit
```

---

# Build Instructions

## Prerequisites

Make sure the following are installed:

- C++ Compiler (GCC / Clang / MSVC)
- CMake

---

# Clone Repository

```bash
git clone <your-repository-url>
```

---

# Navigate to Project

```bash
cd VirtualFileSystem
```

---

# Create Build Directory

```bash
mkdir build
cd build
```

---

# Generate Build Files

```bash
cmake ..
```

---

# Build Project

```bash
make
```

---

# Run Application

```bash
./VirtualFileSystem
```

---

# Design Principles Followed

- Single Responsibility Principle
- Separation of Concerns
- Modular Design
- Reusable Components
- Maintainable Code Structure

---

# Future Improvements

- Nested directory support
- Delete files and directories
- Change directory (`cd`)
- File permissions
- Persistent storage
- Save and load file system state
- Unit testing using Google Test
- Better error handling
- Path traversal support

---

# Learning Outcomes

This project helps in understanding:

- Object-Oriented Programming in C++
- Smart pointers
- Runtime polymorphism
- Virtual functions
- File system architecture
- CLI application design
- CMake build system
- Modular project structure

---

# Author

Krishnpal Singh

---

# License

This project is created for learning and educational purposes.
